include $(top_srcdir)/config/Rules.am

AUTOMAKE_OPTIONS = subdir-objects

VPATH = \
        $(top_srcdir)/module/zfs \
        $(top_srcdir)/module/zcommon \
		$(top_srcdir)/module/lua \
        $(top_srcdir)/lib/libzpool

AM_CFLAGS += $(DEBUG_STACKFLAGS) $(FRAME_LARGER_THAN)

DEFAULT_INCLUDES += \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/lib/libspl/include

lib_LTLIBRARIES = libzpool.la

USER_C = \
        kernel.c \
        taskq.c \
        util.c

KERNEL_C = \
	zfs_comutil.c \
	zfs_deleg.c \
	zfs_fletcher.c \
	zfs_fletcher_avx512.c \
	zfs_fletcher_intel.c \
	zfs_fletcher_sse.c \
	zfs_fletcher_superscalar.c \
	zfs_fletcher_superscalar4.c \
	zfs_namecheck.c \
	zfs_prop.c \
	zfs_uio.c \
	zpool_prop.c \
	zprop_common.c \
	abd.c \
	aggsum.c \
	arc.c \
	blkptr.c \
	bplist.c \
	bpobj.c \
	bptree.c \
	bqueue.c \
	cityhash.c \
	dbuf.c \
	dbuf_stats.c \
	ddt.c \
	ddt_zap.c \
	dmu.c \
	dmu_diff.c \
	dmu_object.c \
	dmu_objset.c \
	dmu_recv.c \
	dmu_send.c \
	dmu_traverse.c \
	dmu_tx.c \
	dmu_zfetch.c \
	dnode.c \
	dnode_sync.c \
	dsl_bookmark.c \
	dsl_dataset.c \
	dsl_deadlist.c \
	dsl_deleg.c \
	dsl_destroy.c \
	dsl_dir.c \
	dsl_crypt.c \
	dsl_pool.c \
	dsl_prop.c \
	dsl_scan.c \
	dsl_synctask.c \
	dsl_userhold.c \
	edonr_zfs.c \
	hkdf.c \
	fm.c \
	gzip.c \
	lzjb.c \
	lz4.c \
	metaslab.c \
	mmp.c \
	multilist.c \
	range_tree.c \
	refcount.c \
	rrwlock.c \
	sa.c \
	sha256.c \
	skein_zfs.c \
	spa.c \
	spa_boot.c \
	spa_checkpoint.c \
	spa_config.c \
	spa_errlog.c \
	spa_history.c \
	spa_misc.c \
	spa_stats.c \
	space_map.c \
	space_reftree.c \
	txg.c \
	uberblock.c \
	unique.c \
	vdev.c \
	vdev_cache.c \
	vdev_file.c \
	vdev_indirect.c \
	vdev_indirect_births.c \
	vdev_indirect_mapping.c \
	vdev_initialize.c \
	vdev_label.c \
	vdev_mirror.c \
	vdev_missing.c \
	vdev_queue.c \
	vdev_raidz.c \
	vdev_raidz_math_avx2.c \
	vdev_raidz_math_avx512bw.c \
	vdev_raidz_math_avx512f.c \
	vdev_raidz_math.c \
	vdev_raidz_math_scalar.c \
	vdev_raidz_math_sse2.c \
	vdev_raidz_math_ssse3.c \
	vdev_removal.c \
	vdev_root.c \
	vdev_trim.c \
	zap.c \
	zap_leaf.c \
	zap_micro.c \
	zcp.c \
	zcp_get.c \
	zcp_global.c \
	zcp_iter.c \
	zcp_synctask.c \
	zfeature.c \
	zfeature_common.c \
	zfs_byteswap.c \
	zfs_debug.c \
	zfs_fm.c \
	zfs_fuid.c \
	zfs_sa.c \
	zfs_znode.c \
	zil.c \
	zio.c \
	zio_checksum.c \
	zio_compress.c \
	zio_crypt.c \
	zio_inject.c \
	zle.c \
	zrlock.c \
	zthr.c

LUA_C = \
	lapi.c \
	lauxlib.c \
	lbaselib.c \
	lbitlib.c \
	lcode.c \
	lcompat.c \
	lcorolib.c \
	lctype.c \
	ldebug.c \
	ldo.c \
	ldump.c \
	lfunc.c \
	lgc.c \
	llex.c \
	lmem.c \
	lobject.c \
	lopcodes.c \
	lparser.c \
	lstate.c \
	lstring.c \
	lstrlib.c \
	ltable.c \
	ltablib.c \
	ltm.c \
	lundump.c \
	lvm.c \
	lzio.c

libzpool_la_SOURCES = \
	$(USER_C) \
	$(KERNEL_C) \
	$(LUA_C)

libzpool_la_LIBADD = \
	$(top_builddir)/lib/libunicode/libunicode.la \
	$(top_builddir)/lib/libuutil/libuutil.la \
	$(top_builddir)/lib/libnvpair/libnvpair.la \
	$(top_builddir)/lib/libicp/libicp.la

libzpool_la_LDFLAGS = -lz -version-info 1:1:0

EXTRA_DIST = $(USER_C)
