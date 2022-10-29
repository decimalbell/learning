# tokyocabinet

## 0.2.9

### 编译
``` shell
$ ./configure --disable-shared
#================================================================
# Configuring Tokyo Cabinet version 0.2.9 (no-shared).
#================================================================
checking for gcc... gcc
checking for C compiler default output file name... a.out
checking whether the C compiler works... yes
checking whether we are cross compiling... no
checking for suffix of executables...
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ANSI C... none needed
checking whether byte ordering is bigendian... no
checking for main in -lc... yes
checking for main in -lm... yes
checking for main in -lpthread... yes
checking for main in -lz... yes
configure: creating ./config.status
config.status: creating Makefile
#================================================================
# Ready to make.
#================================================================
```

``` shell
$ make
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tcutil.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
tcutil.c:44:42: warning: all paths through this function will call itself [-Winfinite-recursion]
void *tccalloc(size_t nmemb, size_t size){
                                         ^
1 warning generated.
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tchdb.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 myconf.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
ar rv libtokyocabinet.a tcutil.o tchdb.o myconf.o
ar: creating archive libtokyocabinet.a
a - tcutil.o
a - tchdb.o
a - myconf.o
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tcutest.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
LD_RUN_PATH=/lib:/usr/lib:/usr/local/lib:/Users/junlongxie/lib:/usr/local/lib:/usr/local/lib:. gcc -std=c99 -Wall -fPIC -fsigned-char -O2 -o tcutest tcutest.o -L. -L/usr/local/lib -L/Users/junlongxie/lib -L/usr/local/lib -ltokyocabinet -lz -lpthread -lm -lc
ld: warning: directory not found for option '-L/Users/junlongxie/lib'
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tcucodec.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
LD_RUN_PATH=/lib:/usr/lib:/usr/local/lib:/Users/junlongxie/lib:/usr/local/lib:/usr/local/lib:. gcc -std=c99 -Wall -fPIC -fsigned-char -O2 -o tcucodec tcucodec.o -L. -L/usr/local/lib -L/Users/junlongxie/lib -L/usr/local/lib -ltokyocabinet -lz -lpthread -lm -lc
ld: warning: directory not found for option '-L/Users/junlongxie/lib'
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tchtest.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
LD_RUN_PATH=/lib:/usr/lib:/usr/local/lib:/Users/junlongxie/lib:/usr/local/lib:/usr/local/lib:. gcc -std=c99 -Wall -fPIC -fsigned-char -O2 -o tchtest tchtest.o -L. -L/usr/local/lib -L/Users/junlongxie/lib -L/usr/local/lib -ltokyocabinet -lz -lpthread -lm -lc
ld: warning: directory not found for option '-L/Users/junlongxie/lib'
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tchmgr.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
LD_RUN_PATH=/lib:/usr/lib:/usr/local/lib:/Users/junlongxie/lib:/usr/local/lib:/usr/local/lib:. gcc -std=c99 -Wall -fPIC -fsigned-char -O2 -o tchmgr tchmgr.o -L. -L/usr/local/lib -L/Users/junlongxie/lib -L/usr/local/lib -ltokyocabinet -lz -lpthread -lm -lc
ld: warning: directory not found for option '-L/Users/junlongxie/lib'

#================================================================
# Ready to install.
#================================================================
```

### 测试
``` shell
$ ./tchtest write ./1000.hdb 1000
<Writing Test>
  path=./1000.hdb  rnum=1000  bnum=-1  apow=-1  fpow=-1  opts=0  omode=0  as=0

......................... (00000100)
......................... (00000200)
......................... (00000300)
......................... (00000400)
......................... (00000500)
......................... (00000600)
......................... (00000700)
......................... (00000800)
......................... (00000900)
......................... (00001000)
record number: 1000
size: 101824
time: 0.005
ok

```

### 问题
#### 编译动态链接库失败

``` shell
$ ./configure
#================================================================
# Configuring Tokyo Cabinet version 0.2.9.
#================================================================
checking for gcc... gcc
checking for C compiler default output file name... a.out
checking whether the C compiler works... yes
checking whether we are cross compiling... no
checking for suffix of executables...
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ANSI C... none needed
checking whether byte ordering is bigendian... no
checking for main in -lc... yes
checking for main in -lm... yes
checking for main in -lpthread... yes
checking for main in -lz... yes
configure: creating ./config.status
config.status: creating Makefile
#================================================================
# Ready to make.
#================================================================
```

``` shell
$ make
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tcutil.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
tcutil.c:44:42: warning: all paths through this function will call itself [-Winfinite-recursion]
void *tccalloc(size_t nmemb, size_t size){
                                         ^
1 warning generated.
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 tchdb.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
gcc -c -I. -I/usr/local/include -L/Users/junlongxie/include -L/usr/local/include -DNDEBUG -D_GNU_SOURCE=1 -D_TC_PREFIX="\"/usr/local\"" -D_TC_INCLUDEDIR="\"/usr/local/include\"" -D_TC_LIBDIR="\"/usr/local/lib\"" -D_TC_BINDIR="\"/usr/local/bin\"" -D_TC_LIBEXECDIR="\"/usr/local/libexec\"" -std=c99 -Wall -fPIC -fsigned-char -O2 myconf.c
clang: warning: argument unused during compilation: '-L/Users/junlongxie/include' [-Wunused-command-line-argument]
clang: warning: argument unused during compilation: '-L/usr/local/include' [-Wunused-command-line-argument]
ar rv libtokyocabinet.a tcutil.o tchdb.o myconf.o
ar: creating archive libtokyocabinet.a
a - tcutil.o
a - tchdb.o
a - myconf.o
gcc -shared -Wl,-soname,libtokyocabinet.so.1 -o libtokyocabinet.so.1.3.0 tcutil.o tchdb.o myconf.o \
	  -L. -L/usr/local/lib -L/Users/junlongxie/lib -L/usr/local/lib -lz -lpthread -lm -lc
ld: warning: directory not found for option '-L/Users/junlongxie/lib'
ld: unknown option: -soname
clang: error: linker command failed with exit code 1 (use -v to see invocation)
make: *** [libtokyocabinet.so.1.3.0] Error 1
```

``` shell
$ git status
On branch 0.2.9
Your branch is up to date with 'origin/0.2.9'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	Makefile
	config.log
	config.status
	libtokyocabinet.a
	myconf.o
	tchdb.o
	tcutil.o

nothing added to commit but untracked files present (use "git add" to track)
```