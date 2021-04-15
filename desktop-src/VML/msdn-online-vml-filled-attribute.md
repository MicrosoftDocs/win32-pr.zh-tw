---
title: VML 填滿屬性
description: VML 填滿屬性
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463680"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="b4de5-103">VML 填滿屬性</span><span class="sxs-lookup"><span data-stu-id="b4de5-103">VML Filled Attribute</span></span>

<span data-ttu-id="b4de5-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b4de5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b4de5-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b4de5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b4de5-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b4de5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b4de5-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b4de5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b4de5-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b4de5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b4de5-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b4de5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b4de5-110">判斷是否會填滿關閉的路徑。</span><span class="sxs-lookup"><span data-stu-id="b4de5-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="b4de5-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b4de5-111">Read/write.</span></span> <span data-ttu-id="b4de5-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="b4de5-112">**VgTriState**.</span></span>

<span data-ttu-id="b4de5-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b4de5-113">**Applies To**</span></span>

[<span data-ttu-id="b4de5-114">形狀</span><span class="sxs-lookup"><span data-stu-id="b4de5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b4de5-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b4de5-115">**Tag Syntax**</span></span>

<span data-ttu-id="b4de5-116"><v： *element* 填入 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b4de5-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="b4de5-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b4de5-117">**Script Syntax**</span></span>

<span data-ttu-id="b4de5-118">*元素* . 填滿 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b4de5-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="b4de5-119">*運算式* =*元素*。已填滿</span><span class="sxs-lookup"><span data-stu-id="b4de5-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="b4de5-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b4de5-120">**Remarks**</span></span>

<span data-ttu-id="b4de5-121">此值會從 [Fill](msdn-online-vml-fill-element.md)元素的 **On** 屬性複製。</span><span class="sxs-lookup"><span data-stu-id="b4de5-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="b4de5-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b4de5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="b4de5-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="b4de5-123">**Example**</span></span>

<span data-ttu-id="b4de5-124">圖形路徑會填滿。</span><span class="sxs-lookup"><span data-stu-id="b4de5-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="b4de5-125">[填滿屬性範例](/previous-versions/bb229669(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b4de5-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="b4de5-126"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="b4de5-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 