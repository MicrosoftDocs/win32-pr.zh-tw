---
title: VML FillColor 屬性
description: VML FillColor 屬性
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969728"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="8ee75-103">VML FillColor 屬性</span><span class="sxs-lookup"><span data-stu-id="8ee75-103">VML FillColor Attribute</span></span>

<span data-ttu-id="8ee75-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8ee75-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8ee75-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8ee75-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8ee75-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8ee75-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8ee75-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8ee75-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8ee75-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8ee75-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8ee75-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8ee75-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8ee75-110">定義填滿形狀封閉路徑的筆刷色彩。</span><span class="sxs-lookup"><span data-stu-id="8ee75-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="8ee75-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ee75-111">Read/write.</span></span> <span data-ttu-id="8ee75-112">[IVgColor](msdn-online-vml-ivgcolor.md) 。</span><span class="sxs-lookup"><span data-stu-id="8ee75-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="8ee75-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8ee75-113">**Applies To**</span></span>

[<span data-ttu-id="8ee75-114">形狀</span><span class="sxs-lookup"><span data-stu-id="8ee75-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8ee75-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8ee75-115">**Tag Syntax**</span></span>

<span data-ttu-id="8ee75-116"><v： *element* fillcolor = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8ee75-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="8ee75-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8ee75-117">**Script Syntax**</span></span>

<span data-ttu-id="8ee75-118"> fillcolor = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8ee75-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="8ee75-119">*運算式* =\*\* fillcolor</span><span class="sxs-lookup"><span data-stu-id="8ee75-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="8ee75-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8ee75-120">**Remarks**</span></span>

<span data-ttu-id="8ee75-121">**FillColor** 值會從 **Fill** 元素的 **Color** 屬性複製而來。</span><span class="sxs-lookup"><span data-stu-id="8ee75-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="8ee75-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="8ee75-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="8ee75-123">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="8ee75-123">**See Also**</span></span>

<span data-ttu-id="8ee75-124">[Shape](shape-element--vml.md)、 [Fill](msdn-online-vml-fill-element.md)、 [IVgColor](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="8ee75-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="8ee75-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="8ee75-125">**Example**</span></span>

<span data-ttu-id="8ee75-126">矩形的填滿色彩為紅色。</span><span class="sxs-lookup"><span data-stu-id="8ee75-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="8ee75-127">[FillColor 屬性範例](/previous-versions/bb229668(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8ee75-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="8ee75-128"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="8ee75-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 