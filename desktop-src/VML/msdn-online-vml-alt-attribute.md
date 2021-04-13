---
title: VML Alt 屬性
description: VML Alt 屬性
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186083"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="d530d-103">VML Alt 屬性</span><span class="sxs-lookup"><span data-stu-id="d530d-103">VML Alt Attribute</span></span>

<span data-ttu-id="d530d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d530d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d530d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d530d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d530d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d530d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d530d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d530d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d530d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d530d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d530d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d530d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d530d-110">定義要顯示的替代文字，而不是圖形。</span><span class="sxs-lookup"><span data-stu-id="d530d-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="d530d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d530d-111">Read/write.</span></span> <span data-ttu-id="d530d-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="d530d-112">**String**.</span></span>

<span data-ttu-id="d530d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d530d-113">**Applies To**</span></span>

[<span data-ttu-id="d530d-114">形狀</span><span class="sxs-lookup"><span data-stu-id="d530d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d530d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d530d-115">**Tag Syntax**</span></span>

<span data-ttu-id="d530d-116"><v： *element* alt = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d530d-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="d530d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="d530d-117">**Script Syntax**</span></span>

<span data-ttu-id="d530d-118">*element* 。 alt = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d530d-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="d530d-119">*運算式* =*元素*。 alt</span><span class="sxs-lookup"><span data-stu-id="d530d-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="d530d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="d530d-120">**Remarks**</span></span>

<span data-ttu-id="d530d-121">**Alt** 屬性類似于標準 HTML **Alt** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d530d-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="d530d-122">這個屬性會提供一種方式，讓瀏覽器將文字轉換成語音，以描述頁面上的圖形元素。</span><span class="sxs-lookup"><span data-stu-id="d530d-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="d530d-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="d530d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="d530d-124">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="d530d-124">**See Also**</span></span>

[<span data-ttu-id="d530d-125">形狀</span><span class="sxs-lookup"><span data-stu-id="d530d-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d530d-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="d530d-126">**Example**</span></span>

<span data-ttu-id="d530d-127">下列 **Alt** 元素將會在瀏覽器中顯示將網頁轉換成說話片語的「紅色矩形」片語。</span><span class="sxs-lookup"><span data-stu-id="d530d-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="d530d-128">[Alt 屬性範例](/previous-versions/bb229663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d530d-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="d530d-129"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="d530d-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 