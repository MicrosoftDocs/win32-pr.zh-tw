---
title: PropertySheet 物件
description: PropertySheet 物件
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092250"
---
# <a name="the-propertysheet-object"></a><span data-ttu-id="f95a6-103">PropertySheet 物件</span><span class="sxs-lookup"><span data-stu-id="f95a6-103">The PropertySheet Object</span></span>

<span data-ttu-id="f95a6-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f95a6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f95a6-105">如果您想要操作 Microsoft Agent 屬性工作表的相對字元 (也稱為 [先進字元選項] 視窗) ， [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) 物件會提供數個可供您使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="f95a6-105">The [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) object provides several properties you can use if you want to manipulate the character relative to the Microsoft Agent property sheet (also known as the Advanced Character Options window).</span></span>

-   [<span data-ttu-id="f95a6-106">**高度**</span><span class="sxs-lookup"><span data-stu-id="f95a6-106">**Height**</span></span>](height-property-pso.md)
-   [<span data-ttu-id="f95a6-107">**離開**</span><span class="sxs-lookup"><span data-stu-id="f95a6-107">**Left**</span></span>](left-property-pso.md)
-   [<span data-ttu-id="f95a6-108">**頁面**</span><span class="sxs-lookup"><span data-stu-id="f95a6-108">**Page**</span></span>](page-property.md)
-   [<span data-ttu-id="f95a6-109">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f95a6-109">**Top**</span></span>](top-property-pso.md)
-   [<span data-ttu-id="f95a6-110">**可見**</span><span class="sxs-lookup"><span data-stu-id="f95a6-110">**Visible**</span></span>](visible-property.md)
-   [<span data-ttu-id="f95a6-111">**寬度**</span><span class="sxs-lookup"><span data-stu-id="f95a6-111">**Width**</span></span>](width-property-pso.md)

<span data-ttu-id="f95a6-112">如果您在顯示內容表之前查詢 [**高度**](height-property-pso.md)、 [**左方**](left-property-pso.md)、 [**頂端**](top-property-pso.md)和 [**寬度**](width-property-pso.md) 屬性，其值會以零 (0) 傳回。</span><span class="sxs-lookup"><span data-stu-id="f95a6-112">If you query [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md), and [**Width**](width-property-pso.md) properties before the property sheet has ever been shown, their values return as zero (0).</span></span> <span data-ttu-id="f95a6-113">一旦顯示之後，這些屬性會傳回視窗的最後一個位置和大小 (相對於您目前的螢幕解析度) 。</span><span class="sxs-lookup"><span data-stu-id="f95a6-113">Once shown, these properties return the last position and size of the window (relative to your current screen resolution).</span></span>

 

 




