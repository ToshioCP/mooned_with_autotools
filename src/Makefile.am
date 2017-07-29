bin_PROGRAMS = mooned

dist_mooned_SOURCES = moonedapp.c moonedwin.c main.c moonedapp.h moonedwin.h
nodist_mooned_SOURCES = $(BUILT_SOURCES)

BUILT_SOURCES = resources.c

## configure.ac内のPKG_CHECK_MODULESでGTK用のGTK_CFLAGSとGTK_LIBSを生成済み
## すべてのCソースのコンパイルで使うのでAM_CFLAGS、AM_LDFLAGSに代入
## なお、個々のソースにのみ適用する場合は、moonedapp_CFLAGSの様に、（ソース名）_CFLAGSなどとする
AM_CFLAGS = $(GTK_CFLAGS)
AM_LDFLAGS = $(GTK_LIBS)

## mooned.gresource.xmlの記述からリソースの元ファイル(現時点ではmenu.uiとmoonedwin.ui)を拾い出してくる。
RESOURCES != $(GLIB_COMPILE_RESOURCES) --sourcedir=$(srcdir) --generate-dependencies $(srcdir)/mooned.gresource.xml

resources.c: mooned.gresource.xml $(RESOURCES)
	$(GLIB_COMPILE_RESOURCES) $(srcdir)/mooned.gresource.xml --target=$@ --sourcedir=$(srcdir) --generate-source

## ディストリビュート用のパッケージ生成時に追加すべきファイル
EXTRA_DIST = $(RESOURCES) mooned.gresource.xml

## make cleanで消去すべきファイル
CLEANFILES = resources.c

