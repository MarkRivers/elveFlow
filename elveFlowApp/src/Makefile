TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

#=============================
# Build the IOC support library

DBD += elveFlowApp.dbd
DBD += elveFlowSupport.dbd

#=============================
# Build the IOC application

PROD_IOC_WIN32 += elveFlowAppV1
elveFlowAppV1_SRCS += drvElveFlowOB1
##PROD_IOC_WIN32 += measCompDemoAppV2
##measCompDemoAppV2_SRCS += drv1608G_V2
##PROD_IOC_WIN32 += measCompDemoAppV3
##measCompDemoAppV3_SRCS += drv1608G_V3
##PROD_IOC_WIN32 += measCompDemoAppV4
##measCompDemoAppV4_SRCS += drv1608G_V4
##PROD_IOC_WIN32 += measCompDemoAppV5
##measCompDemoAppV5_SRCS += drv1608G_V5
##PROD_IOC_WIN32 += measCompDemoApp
##measCompDemoApp_SRCS += drv1608G

PROD_SRCS += elveFlowApp_registerRecordDeviceDriver.cpp
PROD_SRCS += elveFlowAppMain.cpp
PROD_LIBS += asyn
ifeq (win32-x86, $(findstring win32-x86, $(T_A)))
PROD_LIBS += cbw_32
else ifeq (cygwin-x86, $(findstring cygwin-x86, $(T_A)))
PROD_LIBS += cbw_32
else ifeq (windows-x64, $(findstring windows-x64, $(T_A)))
PROD_LIBS += Elveflow64
endif
PROD_LIBS += $(EPICS_BASE_IOC_LIBS)


#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

