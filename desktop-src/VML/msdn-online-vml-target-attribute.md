---
title: VML 目標屬性
description: VML 目標屬性
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106990890"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="7fcf1-103">VML 目標屬性</span><span class="sxs-lookup"><span data-stu-id="7fcf1-103">VML Target Attribute</span></span>

<span data-ttu-id="7fcf1-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7fcf1-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7fcf1-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7fcf1-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7fcf1-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7fcf1-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7fcf1-110">定義顯示 URL 的框架或視窗。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="7fcf1-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7fcf1-111">Read/write.</span></span> <span data-ttu-id="7fcf1-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-112">**String**.</span></span>

<span data-ttu-id="7fcf1-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7fcf1-113">**Applies To**</span></span>

[<span data-ttu-id="7fcf1-114">形狀</span><span class="sxs-lookup"><span data-stu-id="7fcf1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7fcf1-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7fcf1-115">**Tag Syntax**</span></span>

<span data-ttu-id="7fcf1-116"><v： *element* target = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7fcf1-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="7fcf1-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="7fcf1-117">**Remarks**</span></span>

<span data-ttu-id="7fcf1-118">**目標** 屬性類似于錨點的標準 HTML **目標** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="7fcf1-119">數值包括：</span><span class="sxs-lookup"><span data-stu-id="7fcf1-119">Values include:</span></span>



| <span data-ttu-id="7fcf1-120">值</span><span class="sxs-lookup"><span data-stu-id="7fcf1-120">Value</span></span>      | <span data-ttu-id="7fcf1-121">描述</span><span class="sxs-lookup"><span data-stu-id="7fcf1-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcf1-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="7fcf1-122">TargetName</span></span> | <span data-ttu-id="7fcf1-123">字串，包含要在其中載入檔的框架或視窗的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="7fcf1-124">\_空白</span><span class="sxs-lookup"><span data-stu-id="7fcf1-124">\_blank</span></span>    | <span data-ttu-id="7fcf1-125">指定將連結的檔載入至新的空白視窗。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="7fcf1-126">此視窗未命名。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="7fcf1-127">\_媒體</span><span class="sxs-lookup"><span data-stu-id="7fcf1-127">\_media</span></span>    | <span data-ttu-id="7fcf1-128">從適用于 Windows XP Service Pack 2 的 Internet Explorer 6， \_ 媒體屬性已淘汰且不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="7fcf1-129">第一次在 Internet Explorer 6 中提供，這個值指定連結的檔應該載入到 Media Bar 中。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="7fcf1-130">\_父母</span><span class="sxs-lookup"><span data-stu-id="7fcf1-130">\_parent</span></span>   | <span data-ttu-id="7fcf1-131">指定將連結的檔載入包含連結之檔的直屬父代。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="7fcf1-132">\_搜索</span><span class="sxs-lookup"><span data-stu-id="7fcf1-132">\_search</span></span>   | <span data-ttu-id="7fcf1-133">從適用于 Windows XP Service Pack 2 的 Internet Explorer 7，： \_ 搜尋屬性已過時，不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="7fcf1-134">第一次在 Internet Explorer 6 中提供，這個值指定連結的檔要載入瀏覽器的 [搜尋] 窗格中。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="7fcf1-135">\_自我</span><span class="sxs-lookup"><span data-stu-id="7fcf1-135">\_self</span></span>     | <span data-ttu-id="7fcf1-136">指定將連結的檔載入至已按一下連結的視窗中， (使用中視窗) 。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="7fcf1-137">\_top</span><span class="sxs-lookup"><span data-stu-id="7fcf1-137">\_top</span></span>      | <span data-ttu-id="7fcf1-138">指定將連結的檔載入最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="7fcf1-139">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7fcf1-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="7fcf1-140">**範例**</span><span class="sxs-lookup"><span data-stu-id="7fcf1-140">**Example**</span></span>

<span data-ttu-id="7fcf1-141">當您按下矩形時，瀏覽器會在同一個視窗中載入 Microsoft Corporation 首頁。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="7fcf1-142">[目標屬性範例](/previous-versions/bb264096(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7fcf1-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="7fcf1-143"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="7fcf1-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 