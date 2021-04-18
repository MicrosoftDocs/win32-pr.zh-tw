---
title: 形容詞屬性
description: 形容詞屬性
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966252"
---
# <a name="adj-attribute"></a><span data-ttu-id="7c8cd-103">形容詞屬性</span><span class="sxs-lookup"><span data-stu-id="7c8cd-103">Adj Attribute</span></span>

<span data-ttu-id="7c8cd-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7c8cd-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7c8cd-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7c8cd-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7c8cd-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7c8cd-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7c8cd-110">指定用來定義公式值的調整值。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="7c8cd-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7c8cd-111">Read/write.</span></span> <span data-ttu-id="7c8cd-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-112">**String**.</span></span>

<span data-ttu-id="7c8cd-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-113">**Applies To**</span></span>

[<span data-ttu-id="7c8cd-114">形狀</span><span class="sxs-lookup"><span data-stu-id="7c8cd-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7c8cd-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-115">**Tag Syntax**</span></span>

<span data-ttu-id="7c8cd-116"><v： *element* 形容詞 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7c8cd-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="7c8cd-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-117">**Script Syntax**</span></span>

<span data-ttu-id="7c8cd-118">*element* 。形容詞 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7c8cd-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="7c8cd-119">*運算式* =*元素*。形容詞</span><span class="sxs-lookup"><span data-stu-id="7c8cd-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="7c8cd-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-120">**Remarks**</span></span>

<span data-ttu-id="7c8cd-121">調整 **是用** 來提供公式的可調式點。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="7c8cd-122">如果用於標記中，則 **形容詞** 是以逗號分隔的字串，最多8個值。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="7c8cd-123">可能會省略部分值。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-123">Some values may be omitted.</span></span> <span data-ttu-id="7c8cd-124">例如，"0，1，2，，4，5，，7" 會是有效的字串，但第四個和第七個專案將不會有值 (從 0) 開始計算的專案。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="7c8cd-125">針對腳本， **形容詞** 會使用 [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="7c8cd-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="7c8cd-127">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-127">**See Also**</span></span>

[<span data-ttu-id="7c8cd-128">Formula</span><span class="sxs-lookup"><span data-stu-id="7c8cd-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="7c8cd-129">**範例**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-129">**Example**</span></span>

<span data-ttu-id="7c8cd-130">使用調整來建立簡單的正方形。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="7c8cd-131">首先，會建立 **形容詞** 字串來定義八個調整值。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="7c8cd-132">然後每個調整值都是由八個公式的其中一個所參考，其中每個調整值前面加數位記號 (\#) 符號。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="7c8cd-133">最後，會使用參考公式的字串來定義路徑，並以 "at" 正負號 ( @ ) 符號來前面加每個公式。</span><span class="sxs-lookup"><span data-stu-id="7c8cd-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="7c8cd-134"> (需要 Microsoft Internet Explorer 5 或更高版本的[形容詞屬性範例](/previous-versions/bb229662(v=vs.85))。 ) </span><span class="sxs-lookup"><span data-stu-id="7c8cd-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 