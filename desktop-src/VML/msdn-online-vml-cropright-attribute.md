---
title: VML CropRight 屬性
description: VML CropRight 屬性
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463193"
---
# <a name="vml-cropright-attribute"></a><span data-ttu-id="90d59-103">VML CropRight 屬性</span><span class="sxs-lookup"><span data-stu-id="90d59-103">VML CropRight Attribute</span></span>

<span data-ttu-id="90d59-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="90d59-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="90d59-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="90d59-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="90d59-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="90d59-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="90d59-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="90d59-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="90d59-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="90d59-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="90d59-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="90d59-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="90d59-110">定義從右邊移除圖片的百分比。</span><span class="sxs-lookup"><span data-stu-id="90d59-110">Defines the percentage of picture removal from the right side.</span></span> <span data-ttu-id="90d59-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="90d59-111">Read/write.</span></span> <span data-ttu-id="90d59-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="90d59-112">**VgNumber**.</span></span>

<span data-ttu-id="90d59-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="90d59-113">**Applies To**</span></span>

[<span data-ttu-id="90d59-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="90d59-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="90d59-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="90d59-115">**Tag Syntax**</span></span>

<span data-ttu-id="90d59-116"><v： *element* cropright = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="90d59-116"><v: *element* cropright=" *expression* "></span></span>

<span data-ttu-id="90d59-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="90d59-117">**Script Syntax**</span></span>

<span data-ttu-id="90d59-118"> cropright = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="90d59-118">*element* .cropright="*expression*"</span></span>

<span data-ttu-id="90d59-119">*運算式* =\*\* cropright</span><span class="sxs-lookup"><span data-stu-id="90d59-119">*expression*=*element*.cropright</span></span>

<span data-ttu-id="90d59-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="90d59-120">**Remarks**</span></span>

<span data-ttu-id="90d59-121">裁剪量的範圍可以從-1.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="90d59-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="90d59-122">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="90d59-122">The default value is 0.</span></span> <span data-ttu-id="90d59-123">請注意，值1不會顯示任何圖片。</span><span class="sxs-lookup"><span data-stu-id="90d59-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="90d59-124">負數值會導致圖片從正在裁剪的邊緣中擠壓， (圖片和裁剪邊緣之間的空格會以圖形) 填滿色彩填滿。</span><span class="sxs-lookup"><span data-stu-id="90d59-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="90d59-125">小於1的正值會導致剩餘的圖片伸展，以符合圖形。</span><span class="sxs-lookup"><span data-stu-id="90d59-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="90d59-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="90d59-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="90d59-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="90d59-127">**Example**</span></span>

<span data-ttu-id="90d59-128">圖片將會從右邊算出20% 的寬度來擠壓。</span><span class="sxs-lookup"><span data-stu-id="90d59-128">The picture will be squeezed from the right side by 20% of the width.</span></span> <span data-ttu-id="90d59-129">圖片與右邊緣之間的空白空間將會以圖形的填滿色彩填滿。</span><span class="sxs-lookup"><span data-stu-id="90d59-129">The empty space between the picture and the right edge will be filled by the fill color of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 