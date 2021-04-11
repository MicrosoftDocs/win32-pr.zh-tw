---
description: TAPI 1.4 將數個 Api、訊息、常數和結構元素新增至1.3 規格。
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1。4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944205"
---
# <a name="tapi-14"></a><span data-ttu-id="9f547-103">TAPI 1。4</span><span class="sxs-lookup"><span data-stu-id="9f547-103">TAPI 1.4</span></span>

<span data-ttu-id="9f547-104">TAPI 1.4 將數個 Api、訊息、常數和結構元素新增至1.3 規格。</span><span class="sxs-lookup"><span data-stu-id="9f547-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="9f547-105">TAPI 1.4 僅支援16位的 Tsp。</span><span class="sxs-lookup"><span data-stu-id="9f547-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="9f547-106">但是，它允許開發32位應用程式，而不需要擔心16位 Windows 的限制。</span><span class="sxs-lookup"><span data-stu-id="9f547-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="9f547-107">TAPI 和 TSPI 標頭檔用來同時針對 TAPI 1.4 和 TAPI 2.x 開發應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f547-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="9f547-108">雖然這兩個規格之間的結構沒有許多變更，但對 API 的變更 (特別是 Unicode 支援) ，因此請務必注意，標頭會以不同的方式編譯，視 TAPI \_ 目前版本的常數而定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9f547-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="9f547-109">例如：</span><span class="sxs-lookup"><span data-stu-id="9f547-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="9f547-110">\_ \_ 應針對所有 tapi 應用程式定義 tapi 目前的版本。</span><span class="sxs-lookup"><span data-stu-id="9f547-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="9f547-111">雖然 TAPI 2.x 開發並非絕對必要，但未來可能需要進行變更。</span><span class="sxs-lookup"><span data-stu-id="9f547-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



