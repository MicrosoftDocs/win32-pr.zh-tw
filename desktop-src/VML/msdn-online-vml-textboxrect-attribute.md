---
title: VML TextBoxRect 屬性
description: VML TextBoxRect 屬性
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023544"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="36ddf-103">VML TextBoxRect 屬性</span><span class="sxs-lookup"><span data-stu-id="36ddf-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="36ddf-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="36ddf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36ddf-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="36ddf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36ddf-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="36ddf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36ddf-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="36ddf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36ddf-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="36ddf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36ddf-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="36ddf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="36ddf-110">定義圖形內的一或多個文字方塊。</span><span class="sxs-lookup"><span data-stu-id="36ddf-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="36ddf-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36ddf-111">Read/write.</span></span> <span data-ttu-id="36ddf-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="36ddf-112">**String**.</span></span>

<span data-ttu-id="36ddf-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="36ddf-113">**Applies To**</span></span>

[<span data-ttu-id="36ddf-114">路徑</span><span class="sxs-lookup"><span data-stu-id="36ddf-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="36ddf-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="36ddf-115">**Tag Syntax**</span></span>

<span data-ttu-id="36ddf-116"><v： *element* textboxrect = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="36ddf-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="36ddf-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="36ddf-117">**Script Syntax**</span></span>

<span data-ttu-id="36ddf-118"> textboxrect = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="36ddf-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="36ddf-119">*運算式* =\*\* textboxrect</span><span class="sxs-lookup"><span data-stu-id="36ddf-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="36ddf-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="36ddf-120">**Remarks**</span></span>

<span data-ttu-id="36ddf-121">Textbox 是由一或多組數位所定義，其中指定的 (順序) 矩形的左邊、頂端、右邊和底部點。</span><span class="sxs-lookup"><span data-stu-id="36ddf-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="36ddf-122">多個集合會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="36ddf-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="36ddf-123">預設值是與包含矩形相同的維度值。</span><span class="sxs-lookup"><span data-stu-id="36ddf-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="36ddf-124">如果定義了一個以上的 textbox，定義每個文字方塊的逗點分隔四組會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="36ddf-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="36ddf-125">文字方塊通常會在圖形上以1、2、3或6個矩形的組合來提供。</span><span class="sxs-lookup"><span data-stu-id="36ddf-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="36ddf-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="36ddf-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="36ddf-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="36ddf-127">**Example**</span></span>

<span data-ttu-id="36ddf-128">依95單位定義95單位的文字方塊會定義並放置在圖形左上角的5個單位。</span><span class="sxs-lookup"><span data-stu-id="36ddf-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 