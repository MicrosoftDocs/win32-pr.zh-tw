---
title: VML ImageAspect 屬性
description: VML ImageAspect 屬性
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315616"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="30eea-103">VML ImageAspect 屬性</span><span class="sxs-lookup"><span data-stu-id="30eea-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="30eea-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="30eea-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="30eea-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="30eea-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="30eea-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="30eea-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="30eea-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="30eea-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="30eea-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="30eea-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="30eea-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="30eea-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="30eea-110">定義筆觸影像的外觀比例的保留方式。</span><span class="sxs-lookup"><span data-stu-id="30eea-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="30eea-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30eea-111">Read/write.</span></span> <span data-ttu-id="30eea-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="30eea-112">**String**.</span></span>

<span data-ttu-id="30eea-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="30eea-113">**Applies To**</span></span>

[<span data-ttu-id="30eea-114">中風</span><span class="sxs-lookup"><span data-stu-id="30eea-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="30eea-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="30eea-115">**Tag Syntax**</span></span>

<span data-ttu-id="30eea-116"><v：</span><span class="sxs-lookup"><span data-stu-id="30eea-116"><v:</span></span>

<span data-ttu-id="30eea-117">element *imageaspect = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="30eea-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="30eea-118">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="30eea-118">**Script Syntax**</span></span>

<span data-ttu-id="30eea-119">*imageaspect = "* expression *"*</span><span class="sxs-lookup"><span data-stu-id="30eea-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="30eea-120">expression *=* 元素 *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="30eea-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="30eea-121">**備註**</span><span class="sxs-lookup"><span data-stu-id="30eea-121">**Remarks**</span></span>

<span data-ttu-id="30eea-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="30eea-122">Values include:</span></span>



| <span data-ttu-id="30eea-123">值</span><span class="sxs-lookup"><span data-stu-id="30eea-123">Value</span></span>   | <span data-ttu-id="30eea-124">描述</span><span class="sxs-lookup"><span data-stu-id="30eea-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="30eea-125">忽略</span><span class="sxs-lookup"><span data-stu-id="30eea-125">Ignore</span></span>  | <span data-ttu-id="30eea-126">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="30eea-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="30eea-127">至少</span><span class="sxs-lookup"><span data-stu-id="30eea-127">AtLeast</span></span> | <span data-ttu-id="30eea-128">影像的大小至少與 **ImageSize** 相同。</span><span class="sxs-lookup"><span data-stu-id="30eea-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="30eea-129">有</span><span class="sxs-lookup"><span data-stu-id="30eea-129">AtMost</span></span>  | <span data-ttu-id="30eea-130">影像已不大於 **ImageSize**。</span><span class="sxs-lookup"><span data-stu-id="30eea-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="30eea-131">在每個案例中， **ImageSize** 屬性將會調整以保持影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="30eea-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="30eea-132">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="30eea-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="30eea-133">**範例**</span><span class="sxs-lookup"><span data-stu-id="30eea-133">**Example**</span></span>

<span data-ttu-id="30eea-134">筆劃影像的大小至少會和影像大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="30eea-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 