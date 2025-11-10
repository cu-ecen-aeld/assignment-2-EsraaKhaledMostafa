CC=/usr/bin/gcc
CFLAGS=-Wall -Werror
LDFLAGS=-B/usr/bin
TARGET=writer
OBJS=writer.o

# Cross-compilation support
CROSS_COMPILE?=

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CROSS_COMPILE)$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^

%.o: %.c
	$(CROSS_COMPILE)$(CC) $(CFLAGS) -c -o $@ $<

clean:
	rm -f $(OBJS) $(TARGET)
