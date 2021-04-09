---
title: VML 類別屬性
description: VML 類別屬性
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933403"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="f044b-103">VML 類別屬性</span><span class="sxs-lookup"><span data-stu-id="f044b-103">VML Class Attribute</span></span>

<span data-ttu-id="f044b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="f044b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f044b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="f044b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f044b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="f044b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f044b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="f044b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f044b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="f044b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f044b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="f044b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f044b-110">參考 CSS 樣式的定義。</span><span class="sxs-lookup"><span data-stu-id="f044b-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="f044b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f044b-111">Read/write.</span></span> <span data-ttu-id="f044b-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="f044b-112">**String**.</span></span>

<span data-ttu-id="f044b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="f044b-113">**Applies To**</span></span>

[<span data-ttu-id="f044b-114">形狀</span><span class="sxs-lookup"><span data-stu-id="f044b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f044b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="f044b-115">**Tag Syntax**</span></span>

<span data-ttu-id="f044b-116"><v： *element* class = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f044b-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="f044b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="f044b-117">**Script Syntax**</span></span>

<span data-ttu-id="f044b-118">*element* 。 classname = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f044b-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="f044b-119">*運算式* =*元素*。 classname</span><span class="sxs-lookup"><span data-stu-id="f044b-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="f044b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="f044b-120">**Remarks**</span></span>

<span data-ttu-id="f044b-121">**類別** 屬性類似于 CSS 樣式表單所使用的標準 HTML **類別** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f044b-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="f044b-122">請注意，您可以使用 **classname** 來取代腳本的 **類別** 。</span><span class="sxs-lookup"><span data-stu-id="f044b-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="f044b-123">也請注意，若要撰寫腳本，只能讀取 **classname** ;變更 **classname** 的值並不會變更圖形的呈現。</span><span class="sxs-lookup"><span data-stu-id="f044b-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="f044b-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="f044b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f044b-125">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="f044b-125">**See Also**</span></span>

[<span data-ttu-id="f044b-126">形狀</span><span class="sxs-lookup"><span data-stu-id="f044b-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f044b-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="f044b-127">**Example**</span></span>

<span data-ttu-id="f044b-128">使用樣式建立 **寬度** 的類別</span><span class="sxs-lookup"><span data-stu-id="f044b-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="f044b-129">然後藉由包含樣式來參考寬度。</span><span class="sxs-lookup"><span data-stu-id="f044b-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="f044b-130">請注意，[寬度] andheight 並未在 **樣式** 屬性中定義，但會由樣式定義。</span><span class="sxs-lookup"><span data-stu-id="f044b-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="f044b-131">請注意， **類別** 僅適用于 CSS 型別屬性。</span><span class="sxs-lookup"><span data-stu-id="f044b-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 