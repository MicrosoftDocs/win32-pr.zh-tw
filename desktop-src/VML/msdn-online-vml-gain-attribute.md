---
title: VML 增益屬性
description: VML 增益屬性
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376024"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="3838b-103">VML 增益屬性</span><span class="sxs-lookup"><span data-stu-id="3838b-103">VML Gain Attribute</span></span>

<span data-ttu-id="3838b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="3838b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3838b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="3838b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3838b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="3838b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3838b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="3838b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3838b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="3838b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3838b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="3838b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3838b-110">定義影像中所有色彩的濃度。</span><span class="sxs-lookup"><span data-stu-id="3838b-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="3838b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3838b-111">Read/write.</span></span> <span data-ttu-id="3838b-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="3838b-112">**VgNumber**.</span></span>

<span data-ttu-id="3838b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="3838b-113">**Applies To**</span></span>

[<span data-ttu-id="3838b-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="3838b-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="3838b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="3838b-115">**Tag Syntax**</span></span>

<span data-ttu-id="3838b-116"><v： *element* 增益 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3838b-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="3838b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="3838b-117">**Script Syntax**</span></span>

<span data-ttu-id="3838b-118">*element* . 增益 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3838b-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="3838b-119">*運算式* =*元素*。增益</span><span class="sxs-lookup"><span data-stu-id="3838b-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="3838b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="3838b-120">**Remarks**</span></span>

<span data-ttu-id="3838b-121">這個屬性會定義白色色彩的明暗程度，並影響所有其他色彩。</span><span class="sxs-lookup"><span data-stu-id="3838b-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="3838b-122">值的範圍是從0到無限大。</span><span class="sxs-lookup"><span data-stu-id="3838b-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="3838b-123">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="3838b-123">The default value is 1.0.</span></span> <span data-ttu-id="3838b-124">值為0時，不會顯示任何影像。</span><span class="sxs-lookup"><span data-stu-id="3838b-124">A value of 0 displays no image.</span></span> <span data-ttu-id="3838b-125">大於1的值會將圖片和小於1的值淡化，使圖片看似 grayer。</span><span class="sxs-lookup"><span data-stu-id="3838b-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="3838b-126">這個屬性可以用來建立有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="3838b-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="3838b-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="3838b-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="3838b-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="3838b-128">**Example**</span></span>

<span data-ttu-id="3838b-129">影像將會顯示為灰色的所有色彩採用趨勢。</span><span class="sxs-lookup"><span data-stu-id="3838b-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 