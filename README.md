# gsoc
The directory KEXEC_CMA contains the patch set of KEXEC crash kernel memory reservation using CMA (Contiguous Memory Allocator). There is also instruction of how to use the patch.This patch enable us to reserve memory for use of crash kernel in run time instead of boot time. This is five patch patchset. This patch is also submitted to linux kernel community. The link of the patch in lkml mailing list given below:

https://lkml.org/lkml/2016/8/12/263

** This patch is made on linux kernel v4.4.11.

But, instead of a properly working patch it may not always successful to reserve memory. Because CMA sometime fails.

There is a alternative approach called GCMA (Guaranteed contiguous memory allocator) which guarantees the success of allocation. There was a RFC patch on this approach made against kernel v3.18. The folder KEXEC_GCMA contains a same patch ported to linux kernel v3.18. To use this patch with GCMA you have to turn on the following kernel configuration
options

CONFIG_GCMA=y

CONFIG_GCMA_DEFAULT=y


The link to GCMA patch repository is given below:

https://github.com/sjp38/linux.gcma/tree/gcma/rfc/v2


***This is the link to blog posts related to gsoc.

http://ronithalder.blogspot.in/