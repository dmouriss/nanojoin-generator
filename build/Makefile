C=/usr/bin/gcc
CFLAGS=-I
OBJECTS = bottomup/bu_extra.o bottomup/bu_mergepaths.o bottomup/bu_nanojoin.o bottomup/bu_operations.o \
	topdown/td_graphutils.o topdown/td_nanojoin.o topdown/td_operations.o topdown/td_patchAdjacency.o topdown/td_bitvector.o topdown/td_isomorphismcheck.o\
	tree/tree.o \
	nanojoin.o

bottomup/%.o: ../bottomup/%.c
	mkdir -p bottomup
	gcc -O3 -Wall -Wextra -c -o $@ $<

topdown/%.o: ../topdown/%.c
	mkdir -p topdown
	gcc -O3 -Wall -Wextra -c -o $@ $<

tree/%.o: ../tree/%.c
	mkdir -p tree
	gcc -O3 -Wall -Wextra -c -o $@ $<

%.o: ../%.c
	gcc -O3 -Wall -Wextra -c -o $@ $<

nanojoin.out: $(OBJECTS)
	gcc -O3 -Wall -Wextra -o $@ $^

clean:
	rm -fr bottomup/*.o
	rm -fr topdown/*.o
	rm -fr tree/*.o
	rm -f *.o
