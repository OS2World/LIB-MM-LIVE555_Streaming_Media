INCLUDES = -Iinclude -I../groupsock/include
##### Change the following for your environment: 
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

USAGE_ENVIRONMENT_LIB = libUsageEnvironment.$(LIB_SUFFIX)
ALL = $(USAGE_ENVIRONMENT_LIB)
all:	$(ALL)

OBJS = UsageEnvironment.$(OBJ) HashTable.$(OBJ) strDup.$(OBJ)

$(USAGE_ENVIRONMENT_LIB): $(OBJS)
	$(LIBRARY_LINK)$@ $(LIBRARY_LINK_OPTS) $(OBJS)

.$(C).$(OBJ):
	$(C_COMPILER) -c $(C_FLAGS) $<       

.$(CPP).$(OBJ):
	$(CPLUSPLUS_COMPILER) -c $(CPLUSPLUS_FLAGS) $<

UsageEnvironment.$(CPP):	include/UsageEnvironment.hh
include/UsageEnvironment.hh:	include/UsageEnvironment_version.hh include/Boolean.hh include/strDup.hh
HashTable.$(CPP):		include/HashTable.hh
include/HashTable.hh:		include/Boolean.hh
strDup.$(CPP):			include/strDup.hh

clean:
	-rm -rf *.$(OBJ) $(ALL) core *.core *~ include/*~

##### Any additional, platform-specific rules come here:
