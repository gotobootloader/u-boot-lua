#
# (C) Copyright 2000-2006
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# See file CREDITS for list of people who contributed to this
# project.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License as
# published by the Free Software Foundation; either version 2 of
# the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston,
# MA 02111-1307 USA
#

include $(TOPDIR)/config.mk

LIB	= $(obj)liblua.o

AOBJS	=
COBJS-y := lua.o
COBJS-y += lapi.o
COBJS-y += ldo.o
COBJS-y += lauxlib.o
COBJS-y += ldebug.o
COBJS-y += lfunc.o
COBJS-y += lgc.o
COBJS-y += lmem.o
COBJS-y += lobject.o
COBJS-y += lstate.o
COBJS-y += lstring.o
COBJS-y += ltable.o
COBJS-y += ltm.o
COBJS-n += lundump.o
COBJS-y += lvm.o
COBJS-y += lzio.o
COBJS-y += lcode.o
COBJS-y += llex.o
COBJS-y += lopcodes.o
COBJS-y += lparser.o
COBJS-y += linit.o
COBJS-y += lbaselib.o

SRCS	:= $(AOBJS:.o=.S) $(COBJS-y:.o=.c)
OBJS	:= $(addprefix $(obj),$(AOBJS) $(COBJS-y))

#CPPFLAGS +=

all:	$(LIB) $(AOBJS)

$(LIB):	$(obj).depend $(OBJS)
	$(call cmd_link_o_target, $(OBJS))


#########################################################################

# defines $(obj).depend target
include $(SRCTREE)/rules.mk

sinclude $(obj).depend

#########################################################################
