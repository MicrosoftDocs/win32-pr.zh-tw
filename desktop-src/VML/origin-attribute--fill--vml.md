---
title: '原始屬性 (填滿)  (的 VML) '
description: '原始屬性 (填滿)  (的 VML) '
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382769"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="eedd3-103">原始屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="eedd3-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="eedd3-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eedd3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eedd3-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eedd3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eedd3-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eedd3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eedd3-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eedd3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eedd3-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eedd3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eedd3-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eedd3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eedd3-110">定義填滿影像的中心。</span><span class="sxs-lookup"><span data-stu-id="eedd3-110">Defines the center of a fill image.</span></span> <span data-ttu-id="eedd3-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eedd3-111">Read/write.</span></span> <span data-ttu-id="eedd3-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="eedd3-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="eedd3-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eedd3-113">**Applies To**</span></span>

[<span data-ttu-id="eedd3-114">填滿</span><span class="sxs-lookup"><span data-stu-id="eedd3-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="eedd3-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eedd3-115">**Tag Syntax**</span></span>

<span data-ttu-id="eedd3-116"><v： *element* 原點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eedd3-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="eedd3-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eedd3-117">**Script Syntax**</span></span>

<span data-ttu-id="eedd3-118">*element* 。源 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eedd3-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="eedd3-119">*運算式* =*元素*。來源</span><span class="sxs-lookup"><span data-stu-id="eedd3-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="eedd3-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eedd3-120">**Remarks**</span></span>

<span data-ttu-id="eedd3-121">指定相對於影像左上角的點;此點會被視為影像的來源。</span><span class="sxs-lookup"><span data-stu-id="eedd3-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="eedd3-122">預設值是影像的中心。</span><span class="sxs-lookup"><span data-stu-id="eedd3-122">Default is the center of the image.</span></span> <span data-ttu-id="eedd3-123">向量是影像寬度和高度的一小部分。</span><span class="sxs-lookup"><span data-stu-id="eedd3-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="eedd3-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="eedd3-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="eedd3-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="eedd3-125">**Example**</span></span>

<span data-ttu-id="eedd3-126">填滿的影像會向左移位至圖形寬度的點50%。</span><span class="sxs-lookup"><span data-stu-id="eedd3-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 