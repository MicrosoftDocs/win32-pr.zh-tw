---
title: 驗證預處理器選項
description: MIDL 編譯器會隱含地叫用預處理器，而且不會顯示其預處理器參數。
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL 編譯器 MIDL，驗證預處理器選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a047980c9f2f9dc8deffdcf85de767e4dc8705
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840207"
---
# <a name="verifying-preprocessor-options"></a><span data-ttu-id="e6d12-104">驗證預處理器選項</span><span class="sxs-lookup"><span data-stu-id="e6d12-104">Verifying Preprocessor Options</span></span>

<span data-ttu-id="e6d12-105">MIDL 編譯器會隱含地叫用預處理器，而且不會顯示其預處理器參數。</span><span class="sxs-lookup"><span data-stu-id="e6d12-105">The MIDL compiler implicitly invokes the preprocessor and does not display its preprocessor switches.</span></span> <span data-ttu-id="e6d12-106">如果沒有 MIDL [**/cpp \_ opt**](-cpp-opt.md) 參數，預處理器命令列是由 midl 命令列中使用的所有 [**/I**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 參數所組成，以及 **/e** 和 [**/nologo**](-nologo.md) 參數所組成。</span><span class="sxs-lookup"><span data-stu-id="e6d12-106">In the absence of the MIDL [**/cpp\_opt**](-cpp-opt.md) switch, the preprocessor command line is composed of all the [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches used in the MIDL command line, as well as **/E** and [**/nologo**](-nologo.md) switches.</span></span> <span data-ttu-id="e6d12-107">若要查看傳遞給預處理器的參數，請使用編譯器的 [**/confirm**](-confirm.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="e6d12-107">To see the switches passed on to the preprocessor, use the compiler's [**/confirm**](-confirm.md) switch.</span></span>

<span data-ttu-id="e6d12-108">例如，下列程式程式碼</span><span class="sxs-lookup"><span data-stu-id="e6d12-108">For example, the following line</span></span>

<span data-ttu-id="e6d12-109">**midl.exe D \_ WIN32 \_ WINNT = 0x501-健全-DNTENV = 1-Id： \\ nt \\ public \\ Sdk \\ inc.-confirm-Oicf-env WIN32-out x86 stub**</span><span class="sxs-lookup"><span data-stu-id="e6d12-109">**midl.exe -D\_WIN32\_WINNT=0x501 -robust -DNTENV=1 -Id:\\nt\\public\\sdk\\inc -confirm -Oicf -env win32 -out x86 stub.idl**</span></span>

<span data-ttu-id="e6d12-110">產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="e6d12-110">produces the following output:</span></span>

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




