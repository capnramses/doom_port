################################################################
#
# $Id:$
#
# $Log:$
#
CC=  gcc  # gcc or g++

# define for SNDSERV added by Anton
# define for ANTON added to rewrite display code
# m32 flag added by Anton
#CFLAGS=-g -Wall -m32 -DNORMALUNIX -DLINUX -DSNDSERV -DANTON # -DUSEASM
CFLAGS=-g -Wall -m32 -DNORMALUNIX -DLINUX -DSNDSERV -DANTON -DGLFW -DUSEASM
#LDFLAGS=-L/usr/X11R6/lib -L/usr/lib/i386-linux-gnu/
LDFLAGS=-L/usr/lib32/nvidia-331-updates/ -L/usr/lib/i386-linux-gnu/
LIBS= -lGL -lX11 -lXxf86vm -lXrandr -lpthread -lXi -lnsl -lm
#LIBS= -lnsl -lm
#
# add this for GL -lGL -lX11 -lXxf86vm -lXrandr -lpthread -lXi
#

#
# uncomment for GL
#
STATICS= ../../antons_opengl_tutorials_book/common/linux_i386/libGLEW.a ../../antons_opengl_tutorials_book/common/linux_i386/libglfw3.a


# subdirectory for objects
O=linux

# not too sophisticated dependency
OBJS=				\
		$(O)/doomdef.o		\
		$(O)/doomstat.o		\
		$(O)/dstrings.o		\
		$(O)/i_system.o		\
		$(O)/i_sound.o		\
		$(O)/i_video.o		\
		$(O)/i_net.o			\
		$(O)/tables.o			\
		$(O)/f_finale.o		\
		$(O)/f_wipe.o 		\
		$(O)/d_main.o			\
		$(O)/d_net.o			\
		$(O)/d_items.o		\
		$(O)/g_game.o			\
		$(O)/m_menu.o			\
		$(O)/m_misc.o			\
		$(O)/m_argv.o  		\
		$(O)/m_bbox.o			\
		$(O)/m_fixed.o		\
		$(O)/m_swap.o			\
		$(O)/m_cheat.o		\
		$(O)/m_random.o		\
		$(O)/am_map.o			\
		$(O)/p_ceilng.o		\
		$(O)/p_doors.o		\
		$(O)/p_enemy.o		\
		$(O)/p_floor.o		\
		$(O)/p_inter.o		\
		$(O)/p_lights.o		\
		$(O)/p_map.o			\
		$(O)/p_maputl.o		\
		$(O)/p_plats.o		\
		$(O)/p_pspr.o			\
		$(O)/p_setup.o		\
		$(O)/p_sight.o		\
		$(O)/p_spec.o			\
		$(O)/p_switch.o		\
		$(O)/p_mobj.o			\
		$(O)/p_telept.o		\
		$(O)/p_tick.o			\
		$(O)/p_saveg.o		\
		$(O)/p_user.o			\
		$(O)/r_bsp.o			\
		$(O)/r_data.o			\
		$(O)/r_draw.o			\
		$(O)/r_main.o			\
		$(O)/r_plane.o		\
		$(O)/r_segs.o			\
		$(O)/r_sky.o			\
		$(O)/r_things.o		\
		$(O)/w_wad.o			\
		$(O)/wi_stuff.o		\
		$(O)/v_video.o		\
		$(O)/st_lib.o			\
		$(O)/st_stuff.o		\
		$(O)/hu_stuff.o		\
		$(O)/hu_lib.o			\
		$(O)/s_sound.o		\
		$(O)/z_zone.o			\
		$(O)/info.o				\
		$(O)/sounds.o

all:	doom

clean:
	rm -f *.o *~ *.flc
	rm -f linux/*

doom:	$(OBJS) $(O)/i_main.o
	$(CC) $(CFLAGS) $(LDFLAGS) $(OBJS) $(STATICS) $(O)/i_main.o \
	-o doom $(LIBS)

$(O)/%.o:	%.c
	$(CC) $(CFLAGS) -c $< -o $@ -I anton/include
	
#	$(CC) $(CFLAGS) $(LDFLAGS) $(OBJS) $(O)/i_main.o \
#############################################################
#
#############################################################
