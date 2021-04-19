---
title: VML ArcSize 屬性
description: VML ArcSize 屬性
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106990893"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="f83e9-103">VML ArcSize 屬性</span><span class="sxs-lookup"><span data-stu-id="f83e9-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="f83e9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="f83e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f83e9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="f83e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f83e9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="f83e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f83e9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="f83e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f83e9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="f83e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f83e9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="f83e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f83e9-110">定義圓角矩形的圓度量。</span><span class="sxs-lookup"><span data-stu-id="f83e9-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="f83e9-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f83e9-111">Read/write.</span></span> <span data-ttu-id="f83e9-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="f83e9-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="f83e9-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="f83e9-113">**Applies To**</span></span>

[<span data-ttu-id="f83e9-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="f83e9-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="f83e9-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="f83e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="f83e9-116"><v： *element* arcsize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f83e9-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="f83e9-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="f83e9-117">**Script Syntax**</span></span>

<span data-ttu-id="f83e9-118"> arcSize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f83e9-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="f83e9-119">*運算式* =\*\* arcSize</span><span class="sxs-lookup"><span data-stu-id="f83e9-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="f83e9-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="f83e9-120">**Remarks**</span></span>

<span data-ttu-id="f83e9-121">將圓角矩形的圓角定義為矩形長度和寬度的一半寬度的百分比。</span><span class="sxs-lookup"><span data-stu-id="f83e9-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="f83e9-122">0% 的邊角，100% 會形成圓形角落。</span><span class="sxs-lookup"><span data-stu-id="f83e9-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="f83e9-123">**ArcSize** 值為1.0 的正方形會是一個圓形。</span><span class="sxs-lookup"><span data-stu-id="f83e9-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="f83e9-124">預設值為 0.2 (20% ) 。</span><span class="sxs-lookup"><span data-stu-id="f83e9-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="f83e9-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="f83e9-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="f83e9-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="f83e9-126">**Example**</span></span>

<span data-ttu-id="f83e9-127">圓角矩形會以緊密但圓角繪製。</span><span class="sxs-lookup"><span data-stu-id="f83e9-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 