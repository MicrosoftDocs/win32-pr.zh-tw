---
title: VML ImageAlignShape 屬性
description: VML ImageAlignShape 屬性
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315619"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="5f618-103">VML ImageAlignShape 屬性</span><span class="sxs-lookup"><span data-stu-id="5f618-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="5f618-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="5f618-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f618-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="5f618-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f618-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="5f618-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f618-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="5f618-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f618-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="5f618-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f618-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="5f618-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f618-110">決定筆觸影像的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="5f618-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="5f618-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5f618-111">Read/write.</span></span> <span data-ttu-id="5f618-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="5f618-112">**VgTriState**.</span></span>

<span data-ttu-id="5f618-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="5f618-113">**Applies To**</span></span>

[<span data-ttu-id="5f618-114">中風</span><span class="sxs-lookup"><span data-stu-id="5f618-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5f618-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="5f618-115">**Tag Syntax**</span></span>

<span data-ttu-id="5f618-116"><v：</span><span class="sxs-lookup"><span data-stu-id="5f618-116"><v:</span></span>

<span data-ttu-id="5f618-117">element *imagealignshape = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="5f618-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="5f618-118">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="5f618-118">**Script Syntax**</span></span>

<span data-ttu-id="5f618-119">*imagealignshape = "* expression *"*</span><span class="sxs-lookup"><span data-stu-id="5f618-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="5f618-120">expression *=* 元素 *. imagealignshape*</span><span class="sxs-lookup"><span data-stu-id="5f618-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="5f618-121">**備註**</span><span class="sxs-lookup"><span data-stu-id="5f618-121">**Remarks**</span></span>

<span data-ttu-id="5f618-122">若 **為 True**，則會將影像與圖形對齊，否則會將影像與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="5f618-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="5f618-123">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="5f618-123">The default is **True**.</span></span>

<span data-ttu-id="5f618-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="5f618-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5f618-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="5f618-125">**Example**</span></span>

<span data-ttu-id="5f618-126">影像會與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="5f618-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 