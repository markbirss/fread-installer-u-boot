#
# (C) Copyright 2000-2007
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
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.	See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston,
# MA 02111-1307 USA
#

include $(TOPDIR)/config.mk

LIB	:= $(obj)libspi.a

COBJS-$(CONFIG_ATMEL_DATAFLASH_SPI) += atmel_dataflash_spi.o
COBJS-$(CONFIG_ATMEL_SPI) += atmel_spi.o
COBJS-$(CONFIG_BFIN_SPI) += bfin_spi.o
COBJS-$(CONFIG_CF_SPI) += cf_spi.o
COBJS-$(CONFIG_KIRKWOOD_SPI) += kirkwood_spi.o
COBJS-$(CONFIG_MPC52XX_SPI) += mpc52xx_spi.o
COBJS-$(CONFIG_MPC8XXX_SPI) += mpc8xxx_spi.o
COBJS-$(CONFIG_MXC_SPI) += mxc_spi.o
COBJS-$(CONFIG_SOFT_SPI) += soft_spi.o
COBJS-$(CONFIG_IMX_SPI) += imx_spi.o
COBJS-$(CONFIG_IMX_ECSPI) += imx_ecspi.o
COBJS-$(CONFIG_IMX_CSPI) += imx_cspi.o
COBJS-$(CONFIG_IMX_SPI_PMIC) += imx_spi_pmic.o
COBJS-$(CONFIG_IMX_SPI_CPLD) += imx_spi_cpld.o
COBJS-$(CONFIG_MX50_CSPI) += mx50_cspi.o

COBJS	:= $(COBJS-y)
SRCS	:= $(COBJS:.o=.c)
OBJS	:= $(addprefix $(obj),$(COBJS))

all:	$(LIB)

$(LIB):	$(obj).depend $(OBJS)
	$(AR) $(ARFLAGS) $@ $(OBJS)

#########################################################################

# defines $(obj).depend target
include $(SRCTREE)/rules.mk

sinclude $(obj).depend

#########################################################################
