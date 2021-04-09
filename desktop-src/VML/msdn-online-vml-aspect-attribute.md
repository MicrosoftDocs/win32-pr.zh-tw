---
title: VML 外觀屬性
description: VML 外觀屬性
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682616"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="cf507-103">VML 外觀屬性</span><span class="sxs-lookup"><span data-stu-id="cf507-103">VML Aspect Attribute</span></span>

<span data-ttu-id="cf507-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="cf507-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cf507-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="cf507-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cf507-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="cf507-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cf507-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="cf507-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cf507-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="cf507-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cf507-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="cf507-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cf507-110">指定如何保留填滿影像的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="cf507-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="cf507-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cf507-111">Read/write.</span></span> <span data-ttu-id="cf507-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="cf507-112">**String**.</span></span>

<span data-ttu-id="cf507-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="cf507-113">**Applies To**</span></span>

[<span data-ttu-id="cf507-114">填滿</span><span class="sxs-lookup"><span data-stu-id="cf507-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="cf507-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="cf507-115">**Tag Syntax**</span></span>

<span data-ttu-id="cf507-116"><v： *element* 方位 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cf507-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="cf507-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="cf507-117">**Script Syntax**</span></span>

<span data-ttu-id="cf507-118">*元素* 。外觀 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cf507-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="cf507-119">*運算式* =*元素*。外觀</span><span class="sxs-lookup"><span data-stu-id="cf507-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="cf507-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="cf507-120">**Remarks**</span></span>

<span data-ttu-id="cf507-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="cf507-121">Values include:</span></span>



| <span data-ttu-id="cf507-122">值</span><span class="sxs-lookup"><span data-stu-id="cf507-122">Value</span></span>   | <span data-ttu-id="cf507-123">描述</span><span class="sxs-lookup"><span data-stu-id="cf507-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="cf507-124">ignore</span><span class="sxs-lookup"><span data-stu-id="cf507-124">ignore</span></span>  | <span data-ttu-id="cf507-125">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="cf507-125">Ignore aspect issues.</span></span> <span data-ttu-id="cf507-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="cf507-126">Default.</span></span>        |
| <span data-ttu-id="cf507-127">至少</span><span class="sxs-lookup"><span data-stu-id="cf507-127">atleast</span></span> | <span data-ttu-id="cf507-128">影像的大小至少會和 **大小** 一樣大。</span><span class="sxs-lookup"><span data-stu-id="cf507-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="cf507-129">有</span><span class="sxs-lookup"><span data-stu-id="cf507-129">atmost</span></span>  | <span data-ttu-id="cf507-130">影像的大小不會大於 **大小**。</span><span class="sxs-lookup"><span data-stu-id="cf507-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="cf507-131">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="cf507-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="cf507-132">**範例**</span><span class="sxs-lookup"><span data-stu-id="cf507-132">**Example**</span></span>

<span data-ttu-id="cf507-133">組成填滿的影像大於或等於10點的10點大小。</span><span class="sxs-lookup"><span data-stu-id="cf507-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 