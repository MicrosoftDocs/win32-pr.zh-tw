---
title: 'Size 屬性 (填滿)  (的 VML) '
description: 'Size 屬性 (填滿)  (的 VML) '
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933302"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="c9ba7-103">Size 屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="c9ba7-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c9ba7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c9ba7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c9ba7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c9ba7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c9ba7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c9ba7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c9ba7-110">定義填滿影像的大小。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="c9ba7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9ba7-111">Read/write.</span></span> <span data-ttu-id="c9ba7-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="c9ba7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-113">**Applies To**</span></span>

[<span data-ttu-id="c9ba7-114">填滿</span><span class="sxs-lookup"><span data-stu-id="c9ba7-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c9ba7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-115">**Tag Syntax**</span></span>

<span data-ttu-id="c9ba7-116"><v： *element* size = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c9ba7-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="c9ba7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-117">**Script Syntax**</span></span>

<span data-ttu-id="c9ba7-118">*元素* 。 size = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="c9ba7-119">*運算式* =*元素*。大小</span><span class="sxs-lookup"><span data-stu-id="c9ba7-119">*expression*=*element*.size</span></span>

<span data-ttu-id="c9ba7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-120">**Remarks**</span></span>

<span data-ttu-id="c9ba7-121">預設值是原始影像的大小。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-121">The default is the size of the original image.</span></span> <span data-ttu-id="c9ba7-122">大於 shapewill 的大小會顯示放大但裁剪的影像版本。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="c9ba7-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="c9ba7-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c9ba7-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="c9ba7-124">**Example**</span></span>

<span data-ttu-id="c9ba7-125">即使影像的原始大小是 50 50 點，影像在填滿的中央會顯示為 10 10 10 的影像。</span><span class="sxs-lookup"><span data-stu-id="c9ba7-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 