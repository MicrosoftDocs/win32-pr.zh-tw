---
title: 驗證預處理器選項
description: MIDL 編譯器會隱含地叫用預處理器，而且不會顯示其預處理器參數。
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL 編譯器 MIDL，驗證預處理器選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9f5055623a44e88ed57b5ed0cadd0034c6962e160a081c7a55a9a51ca9e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382759"
---
# <a name="verifying-preprocessor-options"></a>驗證預處理器選項

MIDL 編譯器會隱含地叫用預處理器，而且不會顯示其預處理器參數。 如果沒有 MIDL [**/cpp \_ opt**](-cpp-opt.md) 參數，預處理器命令列是由 midl 命令列中使用的所有 [**/I**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 參數所組成，以及 **/e** 和 [**/nologo**](-nologo.md) 參數所組成。 若要查看傳遞給預處理器的參數，請使用編譯器的 [**/confirm**](-confirm.md) 參數。

例如，下列程式程式碼

**midl.exe D \_ WIN32 \_ WINNT = 0x501-健全-DNTENV = 1-Id： \\ nt \\ public \\ Sdk \\ inc.-confirm-Oicf-env WIN32-out x86 stub**

產生下列輸出：

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

 

 




