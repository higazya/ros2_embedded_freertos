#######################################################
#
# Makefile for DDS chat application using lwIP network stack.
#
#######################################################

ALT_NUM = 0
ALT_STR =
#ALT_NUM = 1
#ALT_STR = -DALT1
#ALT_NUM = 2
#ALT_STR = -DALT2

EXECUTABLE = chat${ALT_NUM}

## ToDo modify this route for a relative one
BASE_DDS       = /home/victor/Dropbox/OSRF/ros2_embedded/dds/src

RTPS       = ${BASE_DDS}/rtps
TRANS      = ${BASE_DDS}/trans
DISC       = ${BASE_DDS}/disc
CACHE      = ${BASE_DDS}/cache
DCPS       = ${BASE_DDS}/dcps
DDS        = ${BASE_DDS}/dds
CO         = ${BASE_DDS}/co
DBG        = ${BASE_DDS}/dbg
DYNIP	   = ${BASE_DDS}/dynip
TYPE       = ${BASE_DDS}/xtypes
SQL        = ${BASE_DDS}/sql
SECURITY   = ${BASE_DDS}/security
NSEC	   = ${BASE_DDS}/nsec

## ToDo modify this route for a relative one
SECP       = /home/victor/Dropbox/OSRF/ros2_embedded/dds/plugins/secplug
NSECP      = /home/victor/Dropbox/OSRF/ros2_embedded/dds/plugins/nsecplug/

dds_CSRCS  = ${DDS}/dds.c ${DDS}/domain.c ${DDS}/locator.c ${DDS}/guid.c \
             ${DDS}/dds_seq.c ${DDS}/uqos.c ${DDS}/guard.c

type_CSRCS = ${TYPE}/xtypecode.c ${TYPE}/xtypes.c ${TYPE}/xdata.c \
             ${TYPE}/xcdr.c ${TYPE}/tsm.c ${TYPE}/pl_cdr.c ${TYPE}/pid.c \
             ${TYPE}/xtopic.c ${TYPE}/builtin.c ${TYPE}/vtc.c

dcps_CSRCS = ${DCPS}/dcps_main.c ${DCPS}/dcps_dpfact.c ${DCPS}/dcps_part.c \
	     ${DCPS}/dcps_pub.c ${DCPS}/dcps_sub.c ${DCPS}/dcps_topic.c \
	     ${DCPS}/dcps_reader.c ${DCPS}/dcps_writer.c ${DCPS}/dcps_event.c \
	     ${DCPS}/dcps_waitset.c ${DCPS}/dcps_builtin.c ${DCPS}/dcps_qos.c \
	     ${DCPS}/dcps_entity.c ${DCPS}/dcps_dbg.c

cache_CSRCS= ${CACHE}/cache.c

disc_CSRCS = ${DISC}/disc_tc.c ${DISC}/disc_sub.c ${DISC}/disc_pub.c \
	     ${DISC}/disc_msg.c ${DISC}/disc_ep.c ${DISC}/disc_match.c \
	     ${DISC}/disc_sedp.c ${DISC}/disc_spdp.c ${DISC}/disc_main.c \
	     ${DISC}/disc_ctt.c ${DISC}/disc_psmp.c \
	     ${DISC}/disc_cdd.c

rtps_CSRCS = ${RTPS}/rtps_main.c ${RTPS}/rtps_mux.c ${RTPS}/rtps_msg.c \
	     ${RTPS}/rtps_slbw.c ${RTPS}/rtps_slbr.c ${RTPS}/rtps_slrw.c \
	     ${RTPS}/rtps_sfbr.c ${RTPS}/rtps_sfbw.c ${RTPS}/rtps_sfrr.c \
	     ${RTPS}/rtps_sfrw.c ${RTPS}/rtps_clist.c ${RTPS}/rtps_frag.c \
	     ${RTPS}/rtps_dbg.c ${RTPS}/rtps_trace.c ${RTPS}/rtps_ft.c \
	     ${RTPS}/rtps_fwd.c

trans_CSRCS= ${TRANS}/ip/rtps_ip.c ${TRANS}/ip/ri_udp.c ${TRANS}/ip/ri_dtls.c \
	     ${TRANS}/ip/ri_tcp.c ${TRANS}/ip/ri_tcp_sock.c ${TRANS}/ip/ri_tls.c

co_CSRCS   = ${CO}/pool.c ${CO}/sys.c ${CO}/error.c ${CO}/ipc.c ${CO}/timer.c \
             ${CO}/sock.c ${CO}/skiplist.c ${CO}/str.c ${CO}/heap.c ${CO}/md5.c \
             ${CO}/db.c ${CO}/handle.c ${CO}/tty.c ${CO}/log.c ${CO}/ctrace.c \
             ${CO}/thread.c ${CO}/prof.c ${CO}/hash.c ${CO}/strseq.c \
             ${CO}/nmatch.c ${CO}/random.c ${CO}/ipfilter.c ${CO}/libx.c \
	     ${CO}/config.c ${CO}/cmdline.c

#sec_CSRCS  = ${SECURITY}/security.c
sec_CSRCS  = ${NSEC}/sec_main.c ${NSEC}/sec_id.c ${NSEC}/sec_perm.c \
	     ${NSEC}/sec_auth.c ${NSEC}/sec_access.c ${NSEC}/sec_crypto.c \
	     ${NSEC}/sec_cdata.c ${NSEC}/sec_logging.c ${NSEC}/sec_util.c \
	     ${NSEC}/sec_compat.c ${NSEC}/sec_a_std.c  ${NSEC}/sec_p_std.c \
	     ${NSEC}/sec_c_std.c ${NSEC}/sec_a_dtls.c ${NSEC}/sec_p_dtls.c

#splug_CSRCS= ${SECP}/msecplug.c ${SECP}/xmlparse.c ../security/engine_fs.c
#splug_CSRCS= ../../test/splug/p_main.c ../../test/splug/p_xml.c \
#	     ../security/engine_fs.c
splug_CSRCS= ${NSECP}/sp_auth.c ${NSECP}/sp_crypto.c \
	     ${NSECP}/sp_cert.c ${NSECP}/sp_cred.c \
	     ${NSECP}/sp_sys_cert.c ${NSECP}/sp_sys_crypto.c ${NSECP}/sp_main.c \
	     ${NSECP}/sp_access.c ${NSECP}/sp_xml.c ${NSECP}/sp_access_db.c \
	     ${NSECP}/sp_access_populate.c ${NSECP}/sp_sys_cert_none.c \
	     ${NSECP}/sp_sys.c

sql_CSRCS  = ${SQL}/scan.c ${SQL}/parse.c ${SQL}/bytecode.c

dynip_CSRCS= ${DYNIP}/di_main.c ${DYNIP}/di_linux.c

dbg_CSRCS  = ${DBG}/debug.c

SUBLIME_CHAT_ROUTE = /home/victor/Dropbox/OSRF/ros2_embedded/app/chat/

#  ${dynip_CSRCS} ${splug_CSRCS}
## ToDo modify this route for a relative one 
prog_CSRCS = ${SUBLIME_CHAT_ROUTE}main.c ${SUBLIME_CHAT_ROUTE}chat_msg.c ${dds_CSRCS} ${type_CSRCS} ${dcps_CSRCS} ${disc_CSRCS} \
             ${cache_CSRCS} ${dbg_CSRCS} ${sql_CSRCS}  ${co_CSRCS} ${sec_CSRCS} \
	     

#comment the following && don't define RTPS_USED to drop RTPS/Discovery
prog_CSRCS += ${rtps_CSRCS} ${trans_CSRCS}

prog_COBJS = ${prog_CSRCS:.c=.o}
prog_CHDRS = ${BASE_DDS}/include/*.h ../../api/headers/dds/*.h chat_msg.h

prog_OBJS  = ${prog_COBJS}

${EXECUTABLE}:	${prog_OBJS}
		gcc -o ${EXECUTABLE} ${prog_OBJS} ${LDFLAGS}

#######################################################
# Setup Compile Environment

# Cross compiler
#CROSS_COMPILE		=
CROSS_COMPILE		=arm-none-eabi-
CC       = $(CROSS_COMPILE)gcc


#/////
QEMU_STM32 ?= ../../../RTOS/qemu_stm32/arm-softmmu/qemu-system-arm
ARCH=CM3
VENDOR=ST
PLAT=STM32F4x7
CMSIS_LIB=../../rtos/CMSIS/STM32F4x7
STM32_LIB=../../rtos/STM32F4xx_StdPeriph_Driver
CMSIS_PLAT_SRC = $(CMSIS_LIB)/Device/ST/STM32F4xx/Source/Templates
FREERTOS_SRC = ../../rtos/FreeRTOS
FREERTOS_INC = $(FREERTOS_SRC)/include/                                       
FREERTOS_PORT_INC = $(FREERTOS_SRC)/portable/GCC/ARM_$(ARCH)/
#/////

INC_PATH = -I. -I${BASE_DDS}/include -I../../dds/api/headers/ \
		-I/usr/include/libxml2 -I../../dds/plugins/security/ \
		-I${NSECP}/ -I../../dds/qeo-c-import/openssl/outputNative/openssl/HOSTLINUX/Debug/src/openssl-1.0.1f/include/ \
		-I$(FREERTOS_INC) -I$(FREERTOS_PORT_INC)  \
		-I$(CMSIS_LIB)/Include \
		-I$(CMSIS_LIB)/Device/ST/STM32F4xx/Include \
		-I../../rtos/STM32F4xx_StdPeriph_Driver/inc \

#LIB_PATH =
LIB_PATH = -L../../dds/qeo-c-import/openssl/output/install/usr/local/lib
LIBS     = 

# -DLOG_FILE -DDDS_IPV6 -DDDS_TCP -DEXTRA_STATS -DMSECPLUG_WITH_SECXML -DDDS_TYPECODE
# -DDDS_DEBUG -DPTHREADS_USED -DDDS_NATIVE_SECURITY -DDDS_SECURITY
DEFINES  = -DFORCE_MALLOC -DTTY_NORMAL -DRTPS_USED -DCDD_USED   \
	        -DFREE_RTOS\
	   -DBIGDATA -DDDS_FORWARD   -DXTYPES_USED 

#-DDDS_BUILTINS -
#-DDDS_AUTO_LIVELINESS
#-DDDS_SECURITY
#-DDDS_IP_BCAST
#-DDDS_AUTO_LIVELINESS
#-DFORCE_MALLOC
#-DDDS_IP_BCAST
#-DLOG_FILE -DRTPS_TRACE -DRTPS_SEDP_TRACE
#-DDDS_NO_MCAST
#-DDDS_SERVER
#-DPROFILE 
#-DSTATIC_DISCOVERY
#-DCDD_USED
#-DLOG_FILE 
#-DRTPS_USED
#-DRTPS_TRACE 
#-DDDS_DEBUG 
#-DLOCK_TRACE
#-DCTRACE_USED
#-DDUMP_LOCATORS
#-DLOG_DOMAIN
#-DVALGRIND_USED
#-DDDS_STATUS
#-DFORCE_MALLOC
#-DFILT_VMWARE 

OPTTYPE  = -O0
# -fprofile-arcs -ftest-coverage

# -std=c99 # seems like C99 might be too much for the actual code to compile even in Linux
CFLAGS   = -Wall -Wextra -pedantic -Wno-long-long ${OPTTYPE} ${INC_PATH} ${DEFINES} ${ALT_STR} -g
LDFLAGS  = ${LIB_PATH} ${LIBS} -lnsl -lrt -lpthread -lssl -lcrypto -lxml2 -g
# -lgcov

all: ${EXECUTABLE}

#######################################################
# Rules for cleaning

clean:
	\rm -f ${prog_OBJS} ${EXECUTABLE} core.*

reallyclean: clean
	\rm -f .tdds_log_* ${BASE_DDS}/*/tags Makefile.bak tags

########################################################

# Object sizes

size:
	\size ${prog_OBJS} ${EXECUTABLE}

# coverage

coverage:
	cd ../api/coverage
	lcov -b ../../dcps --directory=../../.. --capture --output-file api.info

# Lint (if available)
LINT=/home/jvoe/bin/flint

lint:	${prog_CSRCS}
	\${LINT} std.lnt ${prog_CSRCS}

# Additional dependencies.

depend:
	\makedepend ${INC_PATH} ../*/*.[ch]
