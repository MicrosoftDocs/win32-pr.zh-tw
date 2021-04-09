---
title: 'Offset 屬性 (Shadow)  (VML) '
description: 'Offset 屬性 (Shadow)  (VML) '
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933303"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="a8bd5-103">Offset 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="a8bd5-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="a8bd5-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a8bd5-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a8bd5-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a8bd5-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a8bd5-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a8bd5-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a8bd5-110">定義陰影延伸超過圖形的距離。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="a8bd5-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8bd5-111">Read/write.</span></span> <span data-ttu-id="a8bd5-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-112">**VgVector2D**.</span></span>

<span data-ttu-id="a8bd5-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-113">**Applies To**</span></span>

[<span data-ttu-id="a8bd5-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="a8bd5-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="a8bd5-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-115">**Tag Syntax**</span></span>

<span data-ttu-id="a8bd5-116"><v： *element* offset = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a8bd5-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="a8bd5-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-117">**Script Syntax**</span></span>

<span data-ttu-id="a8bd5-118">*element* 。 offset = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a8bd5-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="a8bd5-119">*運算式* =*element*。 offset</span><span class="sxs-lookup"><span data-stu-id="a8bd5-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="a8bd5-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-120">**Remarks**</span></span>

<span data-ttu-id="a8bd5-121">X 值的預設位移是2pt，y 值的預設值是2pt。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="a8bd5-122">值可以是絕對測量值，或是 shape 的小數值。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="a8bd5-123">如果是小數，則範圍從50% 到-50%。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="a8bd5-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a8bd5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a8bd5-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-125">**Example**</span></span>

<span data-ttu-id="a8bd5-126">圖形具有陰影，其位移為5點，而10指向右邊。</span><span class="sxs-lookup"><span data-stu-id="a8bd5-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 