---
title: VML LineStyle 屬性
description: VML LineStyle 屬性
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682389"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="dc9e9-103">VML LineStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="dc9e9-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="dc9e9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dc9e9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dc9e9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dc9e9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dc9e9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dc9e9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dc9e9-110">定義筆觸的線條樣式。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="dc9e9-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dc9e9-111">Read/write.</span></span> <span data-ttu-id="dc9e9-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-112">**String**.</span></span>

<span data-ttu-id="dc9e9-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="dc9e9-113">**Applies To**</span></span>

[<span data-ttu-id="dc9e9-114">中風</span><span class="sxs-lookup"><span data-stu-id="dc9e9-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="dc9e9-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="dc9e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="dc9e9-116"><v： *element* linestyle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dc9e9-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="dc9e9-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="dc9e9-117">**Script Syntax**</span></span>

<span data-ttu-id="dc9e9-118"> linestyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="dc9e9-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="dc9e9-119">*運算式* =\*\* linestyle</span><span class="sxs-lookup"><span data-stu-id="dc9e9-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="dc9e9-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="dc9e9-120">**Remarks**</span></span>

<span data-ttu-id="dc9e9-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="dc9e9-121">Values include:</span></span>

-   <span data-ttu-id="dc9e9-122">單一 (預設) </span><span class="sxs-lookup"><span data-stu-id="dc9e9-122">Single (default)</span></span>
-   <span data-ttu-id="dc9e9-123">ThinThin</span><span class="sxs-lookup"><span data-stu-id="dc9e9-123">ThinThin</span></span>
-   <span data-ttu-id="dc9e9-124">ThinThick</span><span class="sxs-lookup"><span data-stu-id="dc9e9-124">ThinThick</span></span>
-   <span data-ttu-id="dc9e9-125">ThickThin</span><span class="sxs-lookup"><span data-stu-id="dc9e9-125">ThickThin</span></span>
-   <span data-ttu-id="dc9e9-126">ThickBetweenThin</span><span class="sxs-lookup"><span data-stu-id="dc9e9-126">ThickBetweenThin</span></span>

<span data-ttu-id="dc9e9-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="dc9e9-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="dc9e9-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="dc9e9-128">**Example**</span></span>

<span data-ttu-id="dc9e9-129">以兩個細筆觸繪製雙線。</span><span class="sxs-lookup"><span data-stu-id="dc9e9-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 