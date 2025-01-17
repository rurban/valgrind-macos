# Valgrind for macOS

This repository contains a version of Valgrind including a few patches to improve support for the macOS platform.

## Status

Valgrind now builds on macOS Mojave (tested on 10.14.4).

## Usage

In order to use this version, use the following command:

```
brew install --HEAD https://raw.githubusercontent.com/LouisBrunner/valgrind-macos/master/valgrind.rb
```

In case you already have Valgrind installed, you will need to either `unlink` it first or `reinstall` it.

## Tests

Here is the result of the test suite:

```
== 660 tests, 319 stderr failures, 66 stdout failures, 0 stderrB failures, 0 stdoutB failures, 32 post failures ==
memcheck/tests/accounting                (stderr)
memcheck/tests/amd64/insn-pmovmskb       (stderr)
memcheck/tests/amd64/sh-mem-vec128-plo-no (stderr)
memcheck/tests/amd64/sh-mem-vec128-plo-yes (stderr)
memcheck/tests/amd64/sh-mem-vec256-plo-no (stderr)
memcheck/tests/amd64/sh-mem-vec256-plo-yes (stderr)
memcheck/tests/badfree-2trace            (stderr)
memcheck/tests/badjump2                  (stderr)
memcheck/tests/big_blocks_freed_list     (stderr)
memcheck/tests/bug155125                 (stderr)
memcheck/tests/bug287260                 (stderr)
memcheck/tests/cdebug_zlib               (stderr)
memcheck/tests/cdebug_zlib_gnu           (stderr)
memcheck/tests/client-msg-as-xml         (stderr)
memcheck/tests/client-msg                (stderr)
memcheck/tests/clientperm                (stderr)
memcheck/tests/darwin/env                (stderr)
memcheck/tests/darwin/pth-supp           (stderr)
memcheck/tests/darwin/scalar             (stderr)
memcheck/tests/darwin/scalar_nocancel    (stderr)
memcheck/tests/deep-backtrace            (stderr)
memcheck/tests/demangle                  (stderr)
memcheck/tests/descr_belowsp             (stderr)
memcheck/tests/describe-block            (stderr)
memcheck/tests/err_disable4              (stderr)
memcheck/tests/execve2                   (stderr)
memcheck/tests/fprw                      (stderr)
memcheck/tests/gone_abrt_xml             (stderr)
memcheck/tests/inlinfo                   (stderr)
memcheck/tests/inlinfosupp               (stderr)
memcheck/tests/inlinfosuppobj            (stderr)
memcheck/tests/leak-autofreepool-0       (stderr)
memcheck/tests/leak-autofreepool-1       (stderr)
memcheck/tests/leak-autofreepool-2       (stderr)
memcheck/tests/leak-autofreepool-4       (stderr)
memcheck/tests/leak-autofreepool-5       (stderr)
memcheck/tests/leak-autofreepool-6       (stderr)
memcheck/tests/leak-cases-full           (stderr)
memcheck/tests/leak-cases-summary        (stderr)
memcheck/tests/leak-cycle                (stderr)
memcheck/tests/leak-delta                (stderr)
memcheck/tests/leak-tree                 (stderr)
memcheck/tests/leak_cpp_interior         (stderr)
memcheck/tests/lks                       (stderr)
memcheck/tests/long_namespace_xml        (stderr)
memcheck/tests/manuel1                   (stderr)
memcheck/tests/memalign_test             (stderr)
memcheck/tests/memcmptest                (stderr)
memcheck/tests/mempool                   (stderr)
memcheck/tests/mempool2                  (stderr)
memcheck/tests/mismatches                (stderr)
memcheck/tests/nanoleak2                 (stderr)
memcheck/tests/nanoleak_supp             (stderr)
memcheck/tests/origin1-yes               (stderr)
memcheck/tests/origin2-not-quite         (stderr)
memcheck/tests/origin3-no                (stderr)
memcheck/tests/origin4-many              (stderr)
memcheck/tests/origin5-bz2               (stderr)
memcheck/tests/origin6-fp                (stderr)
memcheck/tests/overlap                   (stderr)
memcheck/tests/pointer-trace             (stderr)
memcheck/tests/post-syscall              (stderr)
memcheck/tests/recursive-merge           (stderr)
memcheck/tests/sem                       (stderr)
memcheck/tests/static_malloc             (stderr)
memcheck/tests/supp1                     (stderr)
memcheck/tests/supp2                     (stderr)
memcheck/tests/supp_unknown              (stderr)
memcheck/tests/supponlyobj               (stderr)
memcheck/tests/test-plo-no               (stderr)
memcheck/tests/thread_alloca             (stderr)
memcheck/tests/threadname_xml            (stderr)
memcheck/tests/trivialleak               (stderr)
memcheck/tests/undef_malloc_args         (stderr)
memcheck/tests/varinfo1                  (stderr)
memcheck/tests/varinfo2                  (stderr)
memcheck/tests/varinfo3                  (stderr)
memcheck/tests/varinfo4                  (stderr)
memcheck/tests/varinfo5                  (stderr)
memcheck/tests/varinfo6                  (stderr)
memcheck/tests/vbit-test/vbit-test-sec   (stderr)
memcheck/tests/wrap6                     (stdout)
memcheck/tests/wrapmalloc                (stdout)
memcheck/tests/wrapmallocstatic          (stdout)
memcheck/tests/x86/bug152022             (stderr)
memcheck/tests/x86/espindola2            (stderr)
memcheck/tests/x86/fpeflags              (stderr)
memcheck/tests/x86/fprem                 (stdout)
memcheck/tests/x86/fprem                 (stderr)
memcheck/tests/x86/fxsave                (stdout)
memcheck/tests/x86/fxsave                (stderr)
memcheck/tests/x86/insn_basic            (stdout)
memcheck/tests/x86/insn_basic            (stderr)
memcheck/tests/x86/insn_cmov             (stdout)
memcheck/tests/x86/insn_cmov             (stderr)
memcheck/tests/x86/insn_fpu              (stdout)
memcheck/tests/x86/insn_fpu              (stderr)
memcheck/tests/x86/insn_mmx              (stdout)
memcheck/tests/x86/insn_mmx              (stderr)
memcheck/tests/x86/insn_mmxext           (stdout)
memcheck/tests/x86/insn_mmxext           (stderr)
memcheck/tests/x86/more_x86_fp           (stdout)
memcheck/tests/x86/more_x86_fp           (stderr)
memcheck/tests/x86/pushfpopf             (stdout)
memcheck/tests/x86/pushfpopf             (stderr)
memcheck/tests/x86/pushfw_x86            (stdout)
memcheck/tests/x86/pushfw_x86            (stderr)
memcheck/tests/x86/pushpopmem            (stdout)
memcheck/tests/x86/pushpopmem            (stderr)
memcheck/tests/x86/sh-mem-vec128-plo-no  (stderr)
memcheck/tests/x86/sh-mem-vec128-plo-yes (stderr)
memcheck/tests/x86/sse1_memory           (stdout)
memcheck/tests/x86/sse1_memory           (stderr)
memcheck/tests/x86/sse2_memory           (stdout)
memcheck/tests/x86/sse2_memory           (stderr)
memcheck/tests/x86/tronical              (stderr)
memcheck/tests/x86/xor-undef-x86         (stdout)
memcheck/tests/x86/xor-undef-x86         (stderr)
memcheck/tests/xml1                      (stderr)
cachegrind/tests/x86/fpu-28-108          (stderr)
helgrind/tests/annotate_hbefore          (stderr)
helgrind/tests/annotate_rwlock           (stderr)
helgrind/tests/annotate_smart_pointer    (stderr)
helgrind/tests/bug322621                 (stderr)
helgrind/tests/cond_timedwait_invalid    (stderr)
helgrind/tests/free_is_write             (stderr)
helgrind/tests/hg01_all_ok               (stderr)
helgrind/tests/hg02_deadlock             (stderr)
helgrind/tests/hg03_inherit              (stderr)
helgrind/tests/hg04_race                 (stderr)
helgrind/tests/hg05_race2                (stderr)
helgrind/tests/hg06_readshared           (stderr)
helgrind/tests/locked_vs_unlocked1_fwd   (stderr)
helgrind/tests/locked_vs_unlocked1_rev   (stderr)
helgrind/tests/locked_vs_unlocked2       (stderr)
helgrind/tests/locked_vs_unlocked3       (stderr)
helgrind/tests/pth_destroy_cond          (stderr)
helgrind/tests/rwlock_race               (stderr)
helgrind/tests/rwlock_test               (stderr)
helgrind/tests/tc01_simple_race          (stderr)
helgrind/tests/tc02_simple_tls           (stderr)
helgrind/tests/tc03_re_excl              (stderr)
helgrind/tests/tc04_free_lock            (stderr)
helgrind/tests/tc05_simple_race          (stderr)
helgrind/tests/tc06_two_races            (stderr)
helgrind/tests/tc06_two_races_xml        (stderr)
helgrind/tests/tc07_hbl1                 (stderr)
helgrind/tests/tc08_hbl2                 (stderr)
helgrind/tests/tc09_bad_unlock           (stderr)
helgrind/tests/tc10_rec_lock             (stderr)
helgrind/tests/tc11_XCHG                 (stderr)
helgrind/tests/tc12_rwl_trivial          (stderr)
helgrind/tests/tc13_laog1                (stderr)
helgrind/tests/tc14_laog_dinphils        (stderr)
helgrind/tests/tc15_laog_lockdel         (stderr)
helgrind/tests/tc16_byterace             (stderr)
helgrind/tests/tc17_sembar               (stderr)
helgrind/tests/tc18_semabuse             (stderr)
helgrind/tests/tc19_shadowmem            (stderr)
helgrind/tests/tc21_pthonce              (stderr)
helgrind/tests/tc23_bogus_condwait       (stderr)
helgrind/tests/tc24_nonzero_sem          (stderr)
drd/tests/annotate_barrier               (stderr)
drd/tests/annotate_barrier_xml           (stderr)
drd/tests/annotate_hb_err                (stderr)
drd/tests/annotate_hb_race               (stderr)
drd/tests/annotate_hbefore               (stderr)
drd/tests/annotate_ignore_read           (stderr)
drd/tests/annotate_ignore_rw             (stderr)
drd/tests/annotate_ignore_rw2            (stderr)
drd/tests/annotate_ignore_write          (stderr)
drd/tests/annotate_ignore_write2         (stderr)
drd/tests/annotate_order_1               (stderr)
drd/tests/annotate_order_2               (stderr)
drd/tests/annotate_order_3               (stderr)
drd/tests/annotate_publish_hg            (stderr)
drd/tests/annotate_rwlock                (stderr)
drd/tests/annotate_rwlock_hg             (stderr)
drd/tests/annotate_sem                   (stderr)
drd/tests/annotate_smart_pointer         (stderr)
drd/tests/annotate_smart_pointer2        (stderr)
drd/tests/annotate_spinlock              (stderr)
drd/tests/annotate_static                (stderr)
drd/tests/annotate_trace_memory          (stderr)
drd/tests/annotate_trace_memory_xml      (stderr)
drd/tests/atomic_var                     (stderr)
drd/tests/bug-235681                     (stderr)
drd/tests/circular_buffer                (stderr)
drd/tests/concurrent_close               (stderr)
drd/tests/custom_alloc                   (stderr)
drd/tests/custom_alloc_fiw               (stderr)
drd/tests/dlopen                         (stdout)
drd/tests/dlopen                         (stderr)
drd/tests/fork-parallel                  (stderr)
drd/tests/fork-serial                    (stderr)
drd/tests/fp_race                        (stderr)
drd/tests/fp_race2                       (stderr)
drd/tests/fp_race_xml                    (stderr)
drd/tests/free_is_write                  (stderr)
drd/tests/free_is_write2                 (stderr)
drd/tests/hg01_all_ok                    (stderr)
drd/tests/hg02_deadlock                  (stderr)
drd/tests/hg03_inherit                   (stderr)
drd/tests/hg04_race                      (stderr)
drd/tests/hg05_race2                     (stderr)
drd/tests/hg06_readshared                (stderr)
drd/tests/hold_lock_1                    (stderr)
drd/tests/hold_lock_2                    (stderr)
drd/tests/linuxthreads_det               (stderr)
drd/tests/memory_allocation              (stderr)
drd/tests/monitor_example                (stderr)
drd/tests/new_delete                     (stderr)
drd/tests/pth_broadcast                  (stderr)
drd/tests/pth_cancel_locked              (stderr)
drd/tests/pth_cleanup_handler            (stderr)
drd/tests/pth_cond_destroy_busy          (stderr)
drd/tests/pth_cond_race                  (stderr)
drd/tests/pth_cond_race2                 (stderr)
drd/tests/pth_cond_race3                 (stderr)
drd/tests/pth_create_chain               (stderr)
drd/tests/pth_detached                   (stderr)
drd/tests/pth_detached2                  (stderr)
drd/tests/pth_detached3                  (stderr)
drd/tests/pth_inconsistent_cond_wait     (stderr)
drd/tests/pth_mutex_reinit               (stderr)
drd/tests/pth_once                       (stderr)
drd/tests/pth_process_shared_mutex       (stderr)
drd/tests/pth_uninitialized_cond         (stderr)
drd/tests/read_and_free_race             (stderr)
drd/tests/recursive_mutex                (stderr)
drd/tests/rwlock_race                    (stderr)
drd/tests/rwlock_test                    (stderr)
drd/tests/rwlock_type_checking           (stderr)
drd/tests/sem_open                       (stderr)
drd/tests/sem_open2                      (stderr)
drd/tests/sem_open3                      (stderr)
drd/tests/sem_open_traced                (stderr)
drd/tests/sigalrm                        (stderr)
drd/tests/sigaltstack                    (stderr)
drd/tests/str_tester                     (stderr)
drd/tests/tc01_simple_race               (stderr)
drd/tests/tc02_simple_tls                (stderr)
drd/tests/tc03_re_excl                   (stderr)
drd/tests/tc04_free_lock                 (stderr)
drd/tests/tc05_simple_race               (stderr)
drd/tests/tc06_two_races                 (stderr)
drd/tests/tc07_hbl1                      (stdout)
drd/tests/tc07_hbl1                      (stderr)
drd/tests/tc08_hbl2                      (stdout)
drd/tests/tc08_hbl2                      (stderr)
drd/tests/tc09_bad_unlock                (stderr)
drd/tests/tc10_rec_lock                  (stderr)
drd/tests/tc11_XCHG                      (stdout)
drd/tests/tc11_XCHG                      (stderr)
drd/tests/tc12_rwl_trivial               (stderr)
drd/tests/tc13_laog1                     (stderr)
drd/tests/tc15_laog_lockdel              (stderr)
drd/tests/tc16_byterace                  (stderr)
drd/tests/tc17_sembar                    (stderr)
drd/tests/tc19_shadowmem                 (stderr)
drd/tests/tc21_pthonce                   (stdout)
drd/tests/tc21_pthonce                   (stderr)
drd/tests/tc23_bogus_condwait            (stderr)
drd/tests/threaded-fork-vcs              (stderr)
drd/tests/threaded-fork                  (stderr)
drd/tests/tls_threads                    (stderr)
drd/tests/trylock                        (stderr)
drd/tests/unit_bitmap                    (stderr)
drd/tests/unit_vc                        (stderr)
massif/tests/alloc-fns-A                 (post)
massif/tests/alloc-fns-B                 (post)
massif/tests/basic                       (post)
massif/tests/basic2                      (post)
massif/tests/big-alloc                   (post)
massif/tests/culling1                    (stderr)
massif/tests/culling2                    (stderr)
massif/tests/custom_alloc                (post)
massif/tests/deep-A                      (post)
massif/tests/deep-B                      (stderr)
massif/tests/deep-B                      (post)
massif/tests/deep-C                      (stderr)
massif/tests/deep-C                      (post)
massif/tests/deep-D                      (post)
massif/tests/ignored                     (post)
massif/tests/ignoring                    (post)
massif/tests/inlinfomalloc               (post)
massif/tests/insig                       (post)
massif/tests/long-names                  (post)
massif/tests/long-time                   (post)
massif/tests/mmapunmap                   (post)
massif/tests/new-cpp                     (post)
massif/tests/null                        (post)
massif/tests/one                         (post)
massif/tests/overloaded-new              (post)
massif/tests/pages_as_heap               (stderr)
massif/tests/peak                        (post)
massif/tests/peak2                       (stderr)
massif/tests/peak2                       (post)
massif/tests/realloc                     (stderr)
massif/tests/realloc                     (post)
massif/tests/thresholds_0_0              (post)
massif/tests/thresholds_0_10             (post)
massif/tests/thresholds_10_0             (post)
massif/tests/thresholds_10_10            (post)
massif/tests/thresholds_5_0              (post)
massif/tests/thresholds_5_10             (post)
massif/tests/zero1                       (post)
massif/tests/zero2                       (post)
dhat/tests/acc                           (stderr)
dhat/tests/basic                         (stderr)
dhat/tests/big                           (stderr)
dhat/tests/empty                         (stderr)
dhat/tests/sig                           (stderr)
dhat/tests/single                        (stderr)
none/tests/allexec32                     (stdout)
none/tests/allexec32                     (stderr)
none/tests/allexec64                     (stdout)
none/tests/allexec64                     (stderr)
none/tests/amd64/sse4-64                 (stdout)
none/tests/amd64-darwin/bug341419        (stderr)
none/tests/args                          (stdout)
none/tests/async-sigs                    (stderr)
none/tests/bug234814                     (stdout)
none/tests/bug234814                     (stderr)
none/tests/coolo_sigaction               (stdout)
none/tests/darwin/apple-main-arg         (stderr)
none/tests/faultstatus                   (stderr)
none/tests/fdleak_cmsg                   (stderr)
none/tests/ioctl_moans                   (stderr)
none/tests/mmap_fcntl_bug                (stderr)
none/tests/nocwd                         (stdout)
none/tests/nocwd                         (stderr)
none/tests/pth_2sig                      (stderr)
none/tests/pth_cancel1                   (stderr)
none/tests/pth_cancel2                   (stderr)
none/tests/pth_term_signal               (stderr)
none/tests/require-text-symbol-2         (stderr)
none/tests/scripts/shell                 (stderr)
none/tests/syscall-restart1              (stderr)
none/tests/syslog                        (stderr)
none/tests/x86/aad_aam                   (stdout)
none/tests/x86/aad_aam                   (stderr)
none/tests/x86/badseg                    (stdout)
none/tests/x86/badseg                    (stderr)
none/tests/x86/bt_everything             (stdout)
none/tests/x86/bt_everything             (stderr)
none/tests/x86/bt_literal                (stdout)
none/tests/x86/bt_literal                (stderr)
none/tests/x86/bug125959-x86             (stdout)
none/tests/x86/bug125959-x86             (stderr)
none/tests/x86/bug126147-x86             (stdout)
none/tests/x86/bug126147-x86             (stderr)
none/tests/x86/bug132813-x86             (stdout)
none/tests/x86/bug132813-x86             (stderr)
none/tests/x86/bug135421-x86             (stdout)
none/tests/x86/bug135421-x86             (stderr)
none/tests/x86/bug137714-x86             (stdout)
none/tests/x86/bug137714-x86             (stderr)
none/tests/x86/bug152818-x86             (stdout)
none/tests/x86/bug152818-x86             (stderr)
none/tests/x86/cet_nops                  (stdout)
none/tests/x86/cet_nops                  (stderr)
none/tests/x86/cmpxchg8b                 (stdout)
none/tests/x86/cmpxchg8b                 (stderr)
none/tests/x86/cpuid                     (stdout)
none/tests/x86/cpuid                     (stderr)
none/tests/x86/cse_fail                  (stdout)
none/tests/x86/cse_fail                  (stderr)
none/tests/x86/fcmovnu                   (stdout)
none/tests/x86/fcmovnu                   (stderr)
none/tests/x86/fpu_lazy_eflags           (stdout)
none/tests/x86/fpu_lazy_eflags           (stderr)
none/tests/x86/fxtract                   (stdout)
none/tests/x86/fxtract                   (stderr)
none/tests/x86/getseg                    (stdout)
none/tests/x86/getseg                    (stderr)
none/tests/x86/incdec_alt                (stdout)
none/tests/x86/incdec_alt                (stderr)
none/tests/x86/insn_basic                (stdout)
none/tests/x86/insn_basic                (stderr)
none/tests/x86/insn_cmov                 (stdout)
none/tests/x86/insn_cmov                 (stderr)
none/tests/x86/insn_fpu                  (stdout)
none/tests/x86/insn_fpu                  (stderr)
none/tests/x86/insn_mmx                  (stdout)
none/tests/x86/insn_mmx                  (stderr)
none/tests/x86/insn_mmxext               (stdout)
none/tests/x86/insn_mmxext               (stderr)
none/tests/x86/jcxz                      (stdout)
none/tests/x86/jcxz                      (stderr)
none/tests/x86/lahf                      (stdout)
none/tests/x86/lahf                      (stderr)
none/tests/x86/looper                    (stdout)
none/tests/x86/looper                    (stderr)
none/tests/x86/movbe                     (stdout)
none/tests/x86/movbe                     (stderr)
none/tests/x86/movx                      (stdout)
none/tests/x86/movx                      (stderr)
none/tests/x86/pushpopseg                (stdout)
none/tests/x86/pushpopseg                (stderr)
none/tests/x86/sbbmisc                   (stdout)
none/tests/x86/sbbmisc                   (stderr)
none/tests/x86/shift_ndep                (stdout)
none/tests/x86/shift_ndep                (stderr)
none/tests/x86/smc1                      (stdout)
none/tests/x86/smc1                      (stderr)
none/tests/x86/ssse3_misaligned          (stderr)
none/tests/x86/x86locked                 (stdout)
none/tests/x86/x86locked                 (stderr)
none/tests/x86/x87trigOOR                (stdout)
none/tests/x86/x87trigOOR                (stderr)
none/tests/x86/xadd                      (stdout)
none/tests/x86/xadd                      (stderr)
none/tests/x86-darwin/bug341419          (stderr)
none/tests/x86-darwin/bug350062          (stderr)
none/tests/x86-darwin/cet_nops_gs        (stdout)
none/tests/x86-darwin/cet_nops_gs        (stderr)
```

Some tests are blocking:

 - `none/tests`
   - `pselect_alarm`
   - `pth_term_signal`
