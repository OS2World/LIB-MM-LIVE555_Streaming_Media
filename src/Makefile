COMPILE_OPTS =         $(INCLUDES) -I. -O -DSOCKLEN_T=int -DXLOCALE_NOT_USED -DUSE_GETHOSTBYNAME=1
C =                    c
C_COMPILER =           $(CC)
C_FLAGS =              $(COMPILE_OPTS) 
CPP =                  cpp
CPLUSPLUS_COMPILER =   $(CXX)
CPLUSPLUS_FLAGS =      $(COMPILE_OPTS) -Wall -Wno-deprecated 
OBJ =                  o
LINK =                 $(CXX) -o 
LINK_OPTS =            -L.
CONSOLE_LINK_OPTS =    $(LINK_OPTS)
LIBRARY_LINK =         ar cr 
LIBRARY_LINK_OPTS =    
LIB_SUFFIX =                   a
LIBS_FOR_CONSOLE_APPLICATION = 
LIBS_FOR_GUI_APPLICATION = 
EXE = .exe
##### End of variables to change

LIVEMEDIA_DIR = liveMedia
GROUPSOCK_DIR = groupsock
USAGE_ENVIRONMENT_DIR = UsageEnvironment
BASIC_USAGE_ENVIRONMENT_DIR = BasicUsageEnvironment

TESTPROGS_DIR = testProgs

MEDIA_SERVER_DIR = mediaServer

all:
	cd $(LIVEMEDIA_DIR) ; $(MAKE)
	cd $(GROUPSOCK_DIR) ; $(MAKE)
	cd $(USAGE_ENVIRONMENT_DIR) ; $(MAKE)
	cd $(BASIC_USAGE_ENVIRONMENT_DIR) ; $(MAKE)
	cd $(TESTPROGS_DIR) ; $(MAKE)
	cd $(MEDIA_SERVER_DIR) ; $(MAKE)

clean:
	cd $(LIVEMEDIA_DIR) ; $(MAKE) clean
	cd $(GROUPSOCK_DIR) ; $(MAKE) clean
	cd $(USAGE_ENVIRONMENT_DIR) ; $(MAKE) clean
	cd $(BASIC_USAGE_ENVIRONMENT_DIR) ; $(MAKE) clean
	cd $(TESTPROGS_DIR) ; $(MAKE) clean
	cd $(MEDIA_SERVER_DIR) ; $(MAKE) clean
