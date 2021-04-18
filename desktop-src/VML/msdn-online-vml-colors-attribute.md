---
title: VML 色彩屬性
description: VML 色彩屬性
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508032"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="29678-103">VML 色彩屬性</span><span class="sxs-lookup"><span data-stu-id="29678-103">VML Colors Attribute</span></span>

<span data-ttu-id="29678-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="29678-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29678-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="29678-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29678-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="29678-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29678-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="29678-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29678-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="29678-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29678-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="29678-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29678-110">定義漸層填滿的多種色彩。</span><span class="sxs-lookup"><span data-stu-id="29678-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="29678-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="29678-111">Read/write.</span></span> <span data-ttu-id="29678-112">**IVgGradientColorArray**。</span><span class="sxs-lookup"><span data-stu-id="29678-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="29678-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="29678-113">**Applies To**</span></span>

[<span data-ttu-id="29678-114">填滿</span><span class="sxs-lookup"><span data-stu-id="29678-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="29678-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="29678-115">**Tag Syntax**</span></span>

<span data-ttu-id="29678-116"><v： *element* colors = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="29678-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="29678-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="29678-117">**Script Syntax**</span></span>

<span data-ttu-id="29678-118">*元素* 。 colors = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="29678-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="29678-119">*運算式* =*元素*。色彩</span><span class="sxs-lookup"><span data-stu-id="29678-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="29678-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="29678-120">**Remarks**</span></span>

<span data-ttu-id="29678-121">用來定義包含成對百分比值的陣列 ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) 和 Color ([VgColor](msdn-online-vml-ivgcolor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="29678-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="29678-122">陣列會使用陣列中的每個點來建立混合填滿，從 0% (開始，) 由 **色彩** 定義，並在 **Color2**) 所定義的 100% (結束。</span><span class="sxs-lookup"><span data-stu-id="29678-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="29678-123">您可以藉由將色彩值指派為百分比來定義中間色彩。</span><span class="sxs-lookup"><span data-stu-id="29678-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="29678-124">百分比和色彩組不會以逗號分隔，但配對會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="29678-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="29678-125">VML 標準屬性</span><span class="sxs-lookup"><span data-stu-id="29678-125">VML Standard Attribute</span></span>

<span data-ttu-id="29678-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="29678-126">**Example**</span></span>

<span data-ttu-id="29678-127">圖形具有由四種色彩組成的漸層填滿，開頭為紅色、混合成黃色、綠色和 finallyblue。</span><span class="sxs-lookup"><span data-stu-id="29678-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 