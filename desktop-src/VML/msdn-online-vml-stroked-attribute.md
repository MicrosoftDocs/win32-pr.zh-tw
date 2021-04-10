---
title: VML 邊邊屬性
description: VML 邊邊屬性
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093232"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="32805-103">VML 邊邊屬性</span><span class="sxs-lookup"><span data-stu-id="32805-103">VML Stroked Attribute</span></span>

<span data-ttu-id="32805-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="32805-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32805-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="32805-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32805-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="32805-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32805-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="32805-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32805-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="32805-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32805-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="32805-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32805-110">定義是否要將路徑繪製。</span><span class="sxs-lookup"><span data-stu-id="32805-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="32805-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="32805-111">Read/write.</span></span> <span data-ttu-id="32805-112">[VgTriState](msdn-online-vml-vgtristate.md) 。</span><span class="sxs-lookup"><span data-stu-id="32805-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="32805-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="32805-113">**Applies To**</span></span>

[<span data-ttu-id="32805-114">形狀</span><span class="sxs-lookup"><span data-stu-id="32805-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="32805-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="32805-115">**Tag Syntax**</span></span>

<span data-ttu-id="32805-116"><v： *元素* 已邊邊 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="32805-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="32805-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="32805-117">**Script Syntax**</span></span>

<span data-ttu-id="32805-118">*元素* 。筆劃 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="32805-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="32805-119">*運算式* =*元素*。邊邊</span><span class="sxs-lookup"><span data-stu-id="32805-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="32805-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="32805-120">**Remarks**</span></span>

<span data-ttu-id="32805-121">此值會從 [Stroke](msdn-online-vml-stroke-element.md)元素的 **On** 屬性複製。</span><span class="sxs-lookup"><span data-stu-id="32805-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="32805-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="32805-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="32805-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="32805-123">**Example**</span></span>

<span data-ttu-id="32805-124">圖形路徑會進行筆劃。</span><span class="sxs-lookup"><span data-stu-id="32805-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="32805-125">[描邊屬性範例](/previous-versions/bb264094(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="32805-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="32805-126"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="32805-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 