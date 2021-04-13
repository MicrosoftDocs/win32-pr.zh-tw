---
title: 管理記憶體的物件
description: 一般來說，存根負責封裝和解除封裝資料、配置和釋放記憶體，以及將資料傳入和傳出記憶體。
ms.assetid: 9dea0fc0-d248-45b1-9a90-2155011c7e7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3e43b2ff3d1dd8abdacccfb133106bd38ef625
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300872"
---
# <a name="who-manages-memory"></a><span data-ttu-id="8c999-103">誰負責管理記憶體？</span><span class="sxs-lookup"><span data-stu-id="8c999-103">Who Manages Memory?</span></span>

<span data-ttu-id="8c999-104">一般來說，存根負責封裝和解除封裝資料、配置和釋放記憶體，以及將資料傳入和傳出記憶體。</span><span class="sxs-lookup"><span data-stu-id="8c999-104">Generally, the stubs are responsible for packaging and unpackaging data, allocating and freeing memory, and transferring the data to and from memory.</span></span> <span data-ttu-id="8c999-105">不過，在某些情況下，應用程式會負責配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="8c999-105">In some cases, however, the application is responsible for allocating and freeing memory.</span></span> <span data-ttu-id="8c999-106">下列主題將討論判斷哪個元件負責記憶體管理的因素：</span><span class="sxs-lookup"><span data-stu-id="8c999-106">The following topics discuss the factors that determine which component is responsible for memory management:</span></span>

-   [<span data-ttu-id="8c999-107">最上層和內嵌指標</span><span class="sxs-lookup"><span data-stu-id="8c999-107">Top-Level and Embedded Pointers</span></span>](top-level-and-embedded-pointers.md)
-   [<span data-ttu-id="8c999-108">套用至參數的方向屬性</span><span class="sxs-lookup"><span data-stu-id="8c999-108">Directional Attributes Applied to the Parameter</span></span>](directional-attributes-applied-to-the-parameter.md)
-   [<span data-ttu-id="8c999-109">長度、大小和方向屬性</span><span class="sxs-lookup"><span data-stu-id="8c999-109">Length, Size, and Directional Attributes</span></span>](length-size-and-directional-attributes.md)
-   [<span data-ttu-id="8c999-110">套用至參數的指標屬性</span><span class="sxs-lookup"><span data-stu-id="8c999-110">Pointer Attributes Applied to the Parameter</span></span>](pointer-attributes-applied-to-the-parameter.md)
-   [<span data-ttu-id="8c999-111">合併指標和方向屬性</span><span class="sxs-lookup"><span data-stu-id="8c999-111">Combining Pointer and Directional Attributes</span></span>](combining-pointer-and-directional-attributes.md)
-   [<span data-ttu-id="8c999-112">MCCP 緩衝區保護</span><span class="sxs-lookup"><span data-stu-id="8c999-112">MCCP Buffer Protection</span></span>](mccp-buffer-protection.md)
-   [<span data-ttu-id="8c999-113">函數傳回值</span><span class="sxs-lookup"><span data-stu-id="8c999-113">Function return values</span></span>](function-return-values.md)

 

 




