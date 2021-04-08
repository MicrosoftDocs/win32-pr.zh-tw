---
title: C/c + +-編譯器考慮
description: MIDL 編譯器必須與 C 編譯器和 C 預處理器交互操作。
ms.assetid: 3d91d0e4-3a47-4aa2-82d6-c3af11df3a78
keywords:
- MIDL 編譯器 MIDL，C-編譯器
- C-編譯器 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf6968951bbcbb423896f5609092054dfa65f4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021845"
---
# <a name="cc-compiler-considerations"></a><span data-ttu-id="32809-105">C/c + +-編譯器考慮</span><span class="sxs-lookup"><span data-stu-id="32809-105">C/C++-Compiler Considerations</span></span>

<span data-ttu-id="32809-106">MIDL 編譯器必須與 C 編譯器和 C 預處理器交互操作。</span><span class="sxs-lookup"><span data-stu-id="32809-106">The MIDL compiler must interoperate with the C compiler and C preprocessor.</span></span> <span data-ttu-id="32809-107">MIDL 在輸入時不接受 c + + 語法。</span><span class="sxs-lookup"><span data-stu-id="32809-107">MIDL does not accept C++ syntax on input.</span></span> <span data-ttu-id="32809-108">產生的 .h 檔案有介面的 C 樣式和 c + + 樣式定義。</span><span class="sxs-lookup"><span data-stu-id="32809-108">The generated .h file has both C-style and C++-style definitions for interfaces.</span></span> <span data-ttu-id="32809-109">下列主題描述 C 編譯器的需求。</span><span class="sxs-lookup"><span data-stu-id="32809-109">The following topics describe the requirements for the C compiler.</span></span>

-   [<span data-ttu-id="32809-110">C-編譯器封裝問題</span><span class="sxs-lookup"><span data-stu-id="32809-110">C-Compiler Packing Issues</span></span>](c-compiler-packing-issues.md)
-   [<span data-ttu-id="32809-111">C-Proxy/Stub 的編譯器定義</span><span class="sxs-lookup"><span data-stu-id="32809-111">C-Compiler Definitions for Proxy/Stubs</span></span>](c-compiler-definitions-for-proxy-stubs.md)

 

 




