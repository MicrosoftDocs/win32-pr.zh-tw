---
title: VML AlignShape 屬性
description: VML AlignShape 屬性
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316300"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="c3773-103">VML AlignShape 屬性</span><span class="sxs-lookup"><span data-stu-id="c3773-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="c3773-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="c3773-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c3773-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="c3773-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c3773-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="c3773-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c3773-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="c3773-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c3773-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="c3773-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c3773-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="c3773-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c3773-110">判斷影像是否要與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="c3773-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="c3773-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c3773-111">Read/write.</span></span> <span data-ttu-id="c3773-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="c3773-112">**VgTriState**.</span></span>

<span data-ttu-id="c3773-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="c3773-113">**Applies To**</span></span>

[<span data-ttu-id="c3773-114">填滿</span><span class="sxs-lookup"><span data-stu-id="c3773-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c3773-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="c3773-115">**Tag Syntax**</span></span>

<span data-ttu-id="c3773-116"><v： *element* alignshape = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c3773-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="c3773-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="c3773-117">**Script Syntax**</span></span>

<span data-ttu-id="c3773-118"> alignshape = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c3773-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="c3773-119">*運算式* =\*\* alignshape</span><span class="sxs-lookup"><span data-stu-id="c3773-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="c3773-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="c3773-120">**Remarks**</span></span>

<span data-ttu-id="c3773-121">若為 **True**，用來建立填滿的影像會與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="c3773-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="c3773-122">如果為 **False**，用來建立填滿的影像會與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="c3773-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="c3773-123">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="c3773-123">Default is **True**.</span></span>

<span data-ttu-id="c3773-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="c3773-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c3773-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="c3773-125">**Example**</span></span>

<span data-ttu-id="c3773-126">從 myimage.gif 建立的磚填滿影像會與視窗對齊，而不是圖形。雖然圖形是旋轉的，但影像並不是。</span><span class="sxs-lookup"><span data-stu-id="c3773-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 