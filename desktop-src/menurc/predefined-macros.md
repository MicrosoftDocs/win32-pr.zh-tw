---
title: 預先定義的巨集
description: RC 不支援 (\_ \_ DATE \_ \_ 、 \_ \_ FILE \_ \_ 、 \_ \_ LINE \_ \_ 、 \_ \_ STDC \_ \_ 、 \_ \_ TIME \_ \_ 、 \_ \_ TIMESTAMP \_ \_) 的 ANSI C 預先定義宏。 因此，您不能將這些宏包含在要包含在資源腳本中的標頭檔中。
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092254"
---
# <a name="predefined-macros"></a><span data-ttu-id="a9e3e-104">預先定義的巨集</span><span class="sxs-lookup"><span data-stu-id="a9e3e-104">Predefined Macros</span></span>

<span data-ttu-id="a9e3e-105">RC 不支援 (**\_ \_ DATE \_ \_**、 **\_ \_ FILE \_ 、LINE \_** **\_ \_ 、STDC \_ 、 \_** **\_ \_ TIME \_ 、 \_** **\_ \_ TIMESTAMP \_) 的 ANSI C 預先定義宏 \_** 。 **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9e3e-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="a9e3e-106">因此，您不能將這些宏包含在要包含在資源腳本中的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="a9e3e-107">RC 會定義叫 \_ 用的 rc，此功能可讓您根據編譯器是您的 C 編譯器或 RC 編譯器，有條件地編譯部分標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="a9e3e-108">這點很重要，因為 RC 編譯器只支援 C 編譯器所支援的語句子集。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="a9e3e-109">若要使用 RC 編譯器有條件地編譯您的程式碼，請括住 RC 無法使用 ifndef RC （叫用） \# \_ 和 **\# endif** 編譯的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="a9e3e-110">下列範例取自 SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="a9e3e-111">它會示範如何建立可有條件地編譯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a9e3e-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




