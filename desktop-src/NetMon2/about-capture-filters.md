---
description: 捕捉篩選器是 NPP 應用程式的元素，會指示網路監視器驅動程式 (Nmnt.sys) 要保留的網路資料框架以及要忽略的畫面格。
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: 關於 Capture 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987518"
---
# <a name="about-capture-filters"></a><span data-ttu-id="28996-103">關於 Capture 篩選</span><span class="sxs-lookup"><span data-stu-id="28996-103">About Capture Filters</span></span>

<span data-ttu-id="28996-104">捕捉篩選器是 NPP 應用程式的元素，會指示網路監視器驅動程式 (Nmnt.sys) 要保留的網路資料框架以及要忽略的畫面格。</span><span class="sxs-lookup"><span data-stu-id="28996-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="28996-105">設定捕獲篩選器的優點是提高效率。</span><span class="sxs-lookup"><span data-stu-id="28996-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="28996-106">您不需要檢查已捕獲的框架;網路監視器驅動程式會進行檢查。</span><span class="sxs-lookup"><span data-stu-id="28996-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="28996-107">這種方法可消除畫面格複製，以提供記憶體使用優勢。</span><span class="sxs-lookup"><span data-stu-id="28996-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="28996-108">Capture 篩選結構</span><span class="sxs-lookup"><span data-stu-id="28996-108">Capture Filter Structure</span></span>

<span data-ttu-id="28996-109">Capture 篩選器包含三個元素：</span><span class="sxs-lookup"><span data-stu-id="28996-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="28996-110">Etype/SAP 設定</span><span class="sxs-lookup"><span data-stu-id="28996-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="28996-111">位址</span><span class="sxs-lookup"><span data-stu-id="28996-111">Address</span></span>
-   <span data-ttu-id="28996-112">模式比對</span><span class="sxs-lookup"><span data-stu-id="28996-112">Pattern match</span></span>

<span data-ttu-id="28996-113">這些專案一起會以邏輯方式評估在 NPP 應用程式作業期間要包含或排除的畫面格。</span><span class="sxs-lookup"><span data-stu-id="28996-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="28996-114">「捕捉」篩選器會對 NPP 應用程式提供複雜的框架元素與排除專案。</span><span class="sxs-lookup"><span data-stu-id="28996-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="28996-115">網路監視器透過 [**CAPTUREFILTER**](the-capturefilter-structure.md)傳遞至 NPP 的資料結構來執行 capture 篩選器，然後在開始時傳遞到網路監視器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="28996-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="28996-116">如需 NPP 作業和 BLOB 功能的詳細資訊，請參閱 [網路封包提供者](network-packet-providers.md) 和 [網路監視器 blob](network-monitor-blobs.md)。</span><span class="sxs-lookup"><span data-stu-id="28996-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



