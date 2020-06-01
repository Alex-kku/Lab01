## Laboratory work I

<a href="https://yandex.ru/efir/?stream_id=vsVJzkz4i9-s"><img src="https://raw.githubusercontent.com/tp-labs/lab01/master/preview.png" width="640"/></a>

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=Alex-kku
$ export GIST_TOKEN=4c55c871704490261a18d0f60946dff1b514b132
$ alias edit=subl
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace 
$ pwd /home/baha/Alex-kku/workspace
$ cd ..
$ pwd /home/baha/Alex-kku
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz 
18:43:07--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.23.46, 104.20.22.46, 2606:4700:10::6814:162e, ...
Подключение к nodejs.org (nodejs.org)|104.20.23.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: «node-v6.11.5-linux-x64.tar.xz»

node-v6.11.5-linux-x64.tar 100%[=====================================>]   8,92M  5,28MB/s    за 1,7s    

2020-06-01 18:43:09 (5,28 MB/s) - «node-v6.11.5-linux-x64.tar.xz» сохранён [9356460/9356460]

$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/baha/Alex-kku/workspace/node/bin
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ sudo apt  install gist
```

```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

[x] 1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
[x] 2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
[x] 3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
[x] 4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
[x] 5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`). 
[x] 6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
[x] 7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
[x] 8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
[x] 9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
[x] 10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
[x] 11. Найдите *топ10* самых "тяжёлых".

# Homework
```sh
1)
$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
--2020-06-01 19:47:44--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
Распознаётся sourceforge.net (sourceforge.net)… 216.105.38.13
Подключение к sourceforge.net (sourceforge.net)|216.105.38.13|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/ [переход]
--2020-06-01 19:47:45--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/
Подключение к sourceforge.net (sourceforge.net)|216.105.38.13|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download [переход]
--2020-06-01 19:47:46--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download
Подключение к sourceforge.net (sourceforge.net)|216.105.38.13|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?r=&ts=1591030067&use_mirror=netix [переход]
--2020-06-01 19:47:47--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?r=&ts=1591030067&use_mirror=netix
Распознаётся downloads.sourceforge.net (downloads.sourceforge.net)… 216.105.38.13
Подключение к downloads.sourceforge.net (downloads.sourceforge.net)|216.105.38.13|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://netix.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz [переход]
--2020-06-01 19:47:48--  https://netix.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz
Распознаётся netix.dl.sourceforge.net (netix.dl.sourceforge.net)… 87.121.121.2
Подключение к netix.dl.sourceforge.net (netix.dl.sourceforge.net)|87.121.121.2|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 111710205 (107M) [application/x-gzip]
Сохранение в: «boost_1_69_0.tar.gz»

boost_1_69_0.tar.gz 100%[===================>] 106,53M  1,16MB/s    за 76s     

2020-06-01 19:49:04 (1,41 MB/s) - «boost_1_69_0.tar.gz» сохранён [111710205/111710205]

2)
$ tar -xf boost_1_69_0.tar.gz 
$ cd boost_1_69_0 
$ pwd
/home/baha/boost_1_69_0

3)
$ ls -f . | wc -l
20

4)
$ find . -type f | wc -l
61191

5)
$ find . -type f -name '*.h' | wc -l
296 # количество заголовочных файлов
$ find . -type f -name '*.cpp' | wc -l
13774 # количество файлов с расширением `.cpp`
$ find . -type f '!' -name '*.cpp' -a '!' -name '*.cpp' | wc -l
47417 # количествоостальных файлов

6)
$ find . -type f -name 'any.hpp' 
./boost/hana/fwd/any.hpp
./boost/hana/any.hpp
./boost/any.hpp
./boost/spirit/home/support/algorithm/any.hpp
./boost/type_erasure/any.hpp
./boost/fusion/algorithm/query/detail/any.hpp
./boost/fusion/algorithm/query/any.hpp
./boost/fusion/include/any.hpp
./boost/proto/detail/any.hpp
./boost/xpressive/detail/utility/any.hpp

7)
$ find . -type f -exec grep -iH "boost::asio" {} \; # выводятся все файлы,где упоминается последовательность boost::asio

8)
$ ./boost.sh
$ ./b2 —prefix=<DEST>

9)
$ find . -name "*.so.*"
$ find . -name "*.so.*" -exec mv {} ../boost-libs \;

10)
$ find . type -f -exec du -h {} +;
100K ./libboost_stacktrace_basic.a
2,4M ./libboost_wave.dylib
7,8M ./libboost_math_tr1.a
5,4M ./libboost_python27.a 164K ./libboost_thread.dylib 100K ./libboost_math_c99f.dylib
480K ./libboost_$
1,9M ./libboost_math_c99f.a
1,8M ./libboost_math_c99l.a
1,3M ./libboost_iostreams.a
1,1M ./libboost_thread.a
7,3M ./libboost_program_options.a
188K ./libboost_iostreams.dylib
300K ./libboost_coroutine.a
276K ./libboost_timer.a
412K ./libboost_wserialization.dylib 940K ./libboost_contract.a
172K ./libboost_contract.dylib 892K ./libboost_numpy27.a
740K ./libboost_type_erasure.a
21M ./libboost_log_setup.a
16K ./libboost_atomic.a
208K ./libboost_random.a
104K ./libboost_prg_exec_monitor.dylib 528K ./libboost_date_time.a
648K ./libboost_graph.dylib
828K ./libboost_locale.dylib

11)
$ find . type -f -exec du -h {} +|sort -rh | head -n 10
28M ./libboost_wave.a
21M ./libboost_log_setup.a
20M ./libboost_log.a
16M ./libboost_test_exec_monitor.a
15M ./libboost_unit_test_framework.a
9,1M ./libboost_locale.a
8,9M ./libboost_regex.a
8,1M ./libboost_math_tr1f.a
7,8M ./libboost_math_tr1.a
7,7M ./libboost_math_tr1l.a
```
```sh
Copyright (c) 2015-2020 The ISC Authors
```
