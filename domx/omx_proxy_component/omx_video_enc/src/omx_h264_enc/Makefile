# ======================================================================
#   Copyright (C) 2010 Texas Instruments Incorporated
#
#   All rights reserved. Property of Texas Instruments Incorporated.
#   Restricted rights to use, duplicate or disclose this code are
#   granted through contract.
#
#   The program may not be used without the written permission
#   of Texas Instruments Incorporated or against the terms and conditions
#   stipulated in the agreement under which this program has been
#   supplied.
# ====================================================================
#
#  ----------------------------------------------------------------------------
#  Revision History
#
#
#      REF=ORG
#      Original version.
#  ----------------------------------------------------------------------------



include $(PROJROOT)/make/start.mk

# Do not change above "include" line(s)

# Arguments to tools, will move to make system once finalized.

CFLAGS         =
CDEFS          =
ifeq ($(BUILD),udeb)
CDEFS          += DEBUG
endif
CDEFS          +=

EXEC_ARGS      =
ST_LIB_ARGS    =
SH_LIB_ARGS    =

# Define this macro if target runs in kernel mode
#__KERNEL__ = 1

# Target name and extension
# static library        (ST_LIB): filename.a
# shared library soname (SH_LIB): filename.so.maj_ver.min_ver
# executable            (EXEC)  : filename.out

TARGETNAME  = libOMX.TI.DUCATI1.VIDEO.H264E.so


# TARGETTYPE must be EXEC, ST_LIB or SH_LIB in upper case.

TARGETTYPE  = SH_LIB

# install directory relative to the HOSTTARGET directory
HOSTRELEASE = lib

# install directory relative to the root filesystem
ROOTFSRELEASE = lib

# Folders in which gmake will run before building current target

SUBMODULES  = \

# Filename must not begin with '.', '/' or '\'

SOURCES     = \
src/omx_proxy_h264enc.c \



# Search path for include files

INCLUDES    = \
    $(PROJROOT)/omx_core/inc \
    $(PROJROOT)/mm_osal/inc \
    $(PROJROOT)/domx \
    $(PROJROOT)/domx/omx_rpc/inc \


# Libraries needed for linking.

ST_LIBS        =
#mm_osal domx
SH_LIBS        = domx omx_core mm_osal
#pthread rt utils procmgr ipc rcm notify
#SH_LIBS        += sysmgr sysmemmgr


# Search path for library (and linker command) files.
# Current folder and target folder are included by default.

LIBINCLUDES = $(PROJROOT)/mm_osal \
              $(PROJROOT)/domx \
              $(PROJROOT)/omx_core


# Do not change below "include" line(s)

include $(PROJROOT)/make/build.mk
