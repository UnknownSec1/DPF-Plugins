#!/usr/bin/make -f
# Makefile for DISTRHO Plugins #
# ---------------------------- #
# Created by falkTX
#

# --------------------------------------------------------------
# Project name, used for binaries

NAME = AmplitudeImposer

# --------------------------------------------------------------
# Files to build

FILES_DSP = \
	DistrhoPluginAmplitudeImposer.cpp

FILES_UI  = \
	DistrhoArtworkAmplitudeImposer.cpp \
	DistrhoUIAmplitudeImposer.cpp

# --------------------------------------------------------------
# Do some magic

include ../../dpf/Makefile.plugins.mk

# --------------------------------------------------------------
# Enable all possible plugin types

ifeq ($(HAVE_JACK),true)
TARGETS += jack
endif

TARGETS += ladspa
TARGETS += vst

ifeq ($(HAVE_DGL),true)
ifeq ($(HAVE_LIBLO),true)
TARGETS += dssi
endif
endif

ifeq ($(HAVE_DGL),true)
TARGETS += lv2_sep
else
TARGETS += lv2_dsp
endif

all: $(TARGETS)

# --------------------------------------------------------------
