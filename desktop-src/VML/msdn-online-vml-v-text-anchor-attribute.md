---
title: VML V 文字錨點屬性
description: VML V 文字錨點屬性
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376017"
---
# <a name="vml-v-text-anchor-attribute"></a><span data-ttu-id="ff61d-103">VML V 文字錨點屬性</span><span class="sxs-lookup"><span data-stu-id="ff61d-103">VML V-Text-Anchor Attribute</span></span>

<span data-ttu-id="ff61d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ff61d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ff61d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ff61d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ff61d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ff61d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ff61d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ff61d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ff61d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ff61d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ff61d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ff61d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ff61d-110">定義文字方塊中文字的垂直錨定。</span><span class="sxs-lookup"><span data-stu-id="ff61d-110">Defines the vertical anchoring of text in a textbox.</span></span> <span data-ttu-id="ff61d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ff61d-111">Read/write.</span></span> <span data-ttu-id="ff61d-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="ff61d-112">**String**.</span></span>

<span data-ttu-id="ff61d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ff61d-113">**Applies To**</span></span>

[<span data-ttu-id="ff61d-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="ff61d-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="ff61d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ff61d-115">**Tag Syntax**</span></span>

<span data-ttu-id="ff61d-116"><v： *element* v-text-錨點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ff61d-116"><v: *element* v-text-anchor=" *expression* "></span></span>

<span data-ttu-id="ff61d-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="ff61d-117">**Remarks**</span></span>

<span data-ttu-id="ff61d-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="ff61d-118">Values include:</span></span>

-   <span data-ttu-id="ff61d-119">**top** (預設) </span><span class="sxs-lookup"><span data-stu-id="ff61d-119">**top** (default)</span></span>
-   <span data-ttu-id="ff61d-120">**中間**</span><span class="sxs-lookup"><span data-stu-id="ff61d-120">**middle**</span></span>
-   <span data-ttu-id="ff61d-121">**底部**</span><span class="sxs-lookup"><span data-stu-id="ff61d-121">**bottom**</span></span>
-   <span data-ttu-id="ff61d-122">**上至中央**</span><span class="sxs-lookup"><span data-stu-id="ff61d-122">**top-center**</span></span>
-   <span data-ttu-id="ff61d-123">**中間中心**</span><span class="sxs-lookup"><span data-stu-id="ff61d-123">**middle-center**</span></span>
-   <span data-ttu-id="ff61d-124">**下中心**</span><span class="sxs-lookup"><span data-stu-id="ff61d-124">**bottom-center**</span></span>
-   <span data-ttu-id="ff61d-125">**最上層基準**</span><span class="sxs-lookup"><span data-stu-id="ff61d-125">**top-baseline**</span></span>
-   <span data-ttu-id="ff61d-126">**下-基準**</span><span class="sxs-lookup"><span data-stu-id="ff61d-126">**bottom-baseline**</span></span>
-   <span data-ttu-id="ff61d-127">**最上層-基準**</span><span class="sxs-lookup"><span data-stu-id="ff61d-127">**top-center-baseline**</span></span>
-   <span data-ttu-id="ff61d-128">**下中心-基準**</span><span class="sxs-lookup"><span data-stu-id="ff61d-128">**bottom-center-baseline**</span></span>

<span data-ttu-id="ff61d-129">文字會錨定到文字方塊中的垂直位置，如屬性值所示。</span><span class="sxs-lookup"><span data-stu-id="ff61d-129">The text will be anchored to a vertical position in the textbox as indicated by the attribute value.</span></span> <span data-ttu-id="ff61d-130">只有當 [MSO 符合文字到圖形](msdn-online-vml-mso-fit-text-to-shape-attribute.md) 為 **False** 時，文字錨點的對齊才會變得很明顯。</span><span class="sxs-lookup"><span data-stu-id="ff61d-130">The alignment of a text anchor only becomes evident if [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) is **False**.</span></span> <span data-ttu-id="ff61d-131">這個屬性與 **垂直對齊** 樣式屬性不同，它是用於表意文字的語言。</span><span class="sxs-lookup"><span data-stu-id="ff61d-131">This attribute is different from the **Vertical-Align** Style attribute, which is used for ideographic languages.</span></span>

<span data-ttu-id="ff61d-132">Microsoft Office 會使用這個屬性將資料儲存在 Web 檔中，但不會在 Microsoft Internet Explorer 5 或更新版本中轉譯。</span><span class="sxs-lookup"><span data-stu-id="ff61d-132">This attribute is used by Microsoft Office to store data in Web documents but does not render in Microsoft Internet Explorer 5 or greater.</span></span>

<span data-ttu-id="ff61d-133">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ff61d-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="ff61d-134">**範例**</span><span class="sxs-lookup"><span data-stu-id="ff61d-134">**Example**</span></span>

<span data-ttu-id="ff61d-135">文字對齊文字方塊的底部。</span><span class="sxs-lookup"><span data-stu-id="ff61d-135">The text is aligned to the bottom of the textbox.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 