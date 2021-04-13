---
title: VML CropLeft 屬性
description: VML CropLeft 屬性
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186009"
---
# <a name="vml-cropleft-attribute"></a><span data-ttu-id="6fb20-103">VML CropLeft 屬性</span><span class="sxs-lookup"><span data-stu-id="6fb20-103">VML CropLeft Attribute</span></span>

<span data-ttu-id="6fb20-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="6fb20-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6fb20-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="6fb20-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6fb20-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="6fb20-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6fb20-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="6fb20-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6fb20-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="6fb20-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6fb20-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="6fb20-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6fb20-110">定義從左側移除圖片的百分比。</span><span class="sxs-lookup"><span data-stu-id="6fb20-110">Defines the percentage of picture removal from the left side.</span></span> <span data-ttu-id="6fb20-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6fb20-111">Read/write.</span></span> <span data-ttu-id="6fb20-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="6fb20-112">**VgNumber**.</span></span>

<span data-ttu-id="6fb20-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="6fb20-113">**Applies To**</span></span>

[<span data-ttu-id="6fb20-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="6fb20-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="6fb20-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="6fb20-115">**Tag Syntax**</span></span>

<span data-ttu-id="6fb20-116"><v： *element* cropleft = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6fb20-116"><v: *element* cropleft=" *expression* "></span></span>

<span data-ttu-id="6fb20-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="6fb20-117">**Script Syntax**</span></span>

<span data-ttu-id="6fb20-118"> cropleft = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6fb20-118">*element* .cropleft="*expression*"</span></span>

<span data-ttu-id="6fb20-119">*運算式* =\*\* cropleft</span><span class="sxs-lookup"><span data-stu-id="6fb20-119">*expression*=*element*.cropleft</span></span>

<span data-ttu-id="6fb20-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="6fb20-120">**Remarks**</span></span>

<span data-ttu-id="6fb20-121">裁剪量的範圍可以從-1.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="6fb20-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="6fb20-122">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="6fb20-122">The default value is 0.</span></span> <span data-ttu-id="6fb20-123">請注意，值1不會顯示任何圖片。</span><span class="sxs-lookup"><span data-stu-id="6fb20-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="6fb20-124">負數值會導致圖片從正在裁剪的邊緣中擠壓， (圖片和裁剪邊緣之間的空格會以圖形) 填滿色彩填滿。</span><span class="sxs-lookup"><span data-stu-id="6fb20-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="6fb20-125">小於1的正值會導致剩餘的圖片伸展，以符合圖形。</span><span class="sxs-lookup"><span data-stu-id="6fb20-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="6fb20-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="6fb20-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="6fb20-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="6fb20-127">**Example**</span></span>

<span data-ttu-id="6fb20-128">左邊將會移除20% 的圖片，而剩餘的圖片將會伸展以符合圖形。</span><span class="sxs-lookup"><span data-stu-id="6fb20-128">20% of the picture will be removed on the left side and the remaining picture will be stretched to fit the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 