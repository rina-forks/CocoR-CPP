%.o: %.cpp
	$(CXX) -g -Wall -fno-rtti -fno-exceptions -fsanitize=address $(CFLAGS) $(CXXFLAGS) $^ -o $@ -c

Coco: Action.o BitArray.o CharClass.o CharSet.o Coco.o Comment.o DFA.o Generator.o HashTable.o Melted.o Node.o Parser.o ParserGen.o Position.o Scanner.o SortedList.o State.o StringBuilder.o Symbol.o Tab.o Target.o
	$(CXX) -g -Wall -fno-rtti -fno-exceptions -fsanitize=address $(CFLAGS) $(CXXFLAGS) $^ -o $@
	# g++ -g -Wall -fno-rtti -fno-exceptions  *.cpp -o Coco -fsanitize=address $(CFLAGS)
	#x86_64-w64-mingw32-g++ -g -Wall -fno-rtti -fno-exceptions  *.cpp -o Coco.exe $(CFLAGS)

clean:
	rm -f Coco *.o

install:
	ln -s /usr/lib/coco-cpp/Coco $(DESTDIR)/usr/bin/cococpp
	install -m 0755 Coco $(DESTDIR)/usr/lib/coco-cpp
	install -m 0644 *frame $(DESTDIR)/usr/share/coco-cpp

