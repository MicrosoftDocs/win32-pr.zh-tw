---
title: VML ImageSize 屬性
description: VML ImageSize 屬性
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682554"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="e7f3b-103">VML ImageSize 屬性</span><span class="sxs-lookup"><span data-stu-id="e7f3b-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="e7f3b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e7f3b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e7f3b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e7f3b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e7f3b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e7f3b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e7f3b-110">定義筆觸影像的大小。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="e7f3b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e7f3b-111">Read/write.</span></span> <span data-ttu-id="e7f3b-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-112">**VgVector2D**.</span></span>

<span data-ttu-id="e7f3b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="e7f3b-113">**Applies To**</span></span>

[<span data-ttu-id="e7f3b-114">中風</span><span class="sxs-lookup"><span data-stu-id="e7f3b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e7f3b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="e7f3b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e7f3b-116"><v： *element* imagesize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e7f3b-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="e7f3b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="e7f3b-117">**Script Syntax**</span></span>

<span data-ttu-id="e7f3b-118"> imagesize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e7f3b-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="e7f3b-119">*運算式* =\*\* imagesize</span><span class="sxs-lookup"><span data-stu-id="e7f3b-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="e7f3b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="e7f3b-120">**Remarks**</span></span>

<span data-ttu-id="e7f3b-121">預設值是影像的大小。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-121">Default is the size of the image.</span></span>

<span data-ttu-id="e7f3b-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="e7f3b-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="e7f3b-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="e7f3b-123">**Example**</span></span>

<span data-ttu-id="e7f3b-124">筆劃影像會是10到10的點大小。</span><span class="sxs-lookup"><span data-stu-id="e7f3b-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 