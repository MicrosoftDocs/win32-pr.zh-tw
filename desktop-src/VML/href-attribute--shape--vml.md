---
title: 'HRef 屬性 (圖形)  (VML) '
description: 'HRef 屬性 (圖形)  (VML) '
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024002"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="bbfdf-103">HRef 屬性 (圖形)  (VML) </span><span class="sxs-lookup"><span data-stu-id="bbfdf-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="bbfdf-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bbfdf-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bbfdf-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bbfdf-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bbfdf-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bbfdf-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bbfdf-110">定義圖形的 URL。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-110">Defines a URL for a shape.</span></span> <span data-ttu-id="bbfdf-111">按一下圖形時，瀏覽器會載入 URL。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="bbfdf-112">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bbfdf-112">Read/write.</span></span> <span data-ttu-id="bbfdf-113">**字串**。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-113">**String**.</span></span>

<span data-ttu-id="bbfdf-114">**適用於**</span><span class="sxs-lookup"><span data-stu-id="bbfdf-114">**Applies To**</span></span>

[<span data-ttu-id="bbfdf-115">形狀</span><span class="sxs-lookup"><span data-stu-id="bbfdf-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bbfdf-116">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="bbfdf-116">**Tag Syntax**</span></span>

<span data-ttu-id="bbfdf-117"><v： *element* href = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bbfdf-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="bbfdf-118">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="bbfdf-118">**Script Syntax**</span></span>

<span data-ttu-id="bbfdf-119">*元素* 。 href = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="bbfdf-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="bbfdf-120">*運算式* =*元素* href</span><span class="sxs-lookup"><span data-stu-id="bbfdf-120">*expression*=*element*.href</span></span>

<span data-ttu-id="bbfdf-121">**備註**</span><span class="sxs-lookup"><span data-stu-id="bbfdf-121">**Remarks**</span></span>

<span data-ttu-id="bbfdf-122">**HRef** 屬性類似于錨點的標準 HTML **HRef** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="bbfdf-123">使用 **HRef** 可讓您輕鬆地在網頁上建立有趣的按鈕。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="bbfdf-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="bbfdf-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="bbfdf-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="bbfdf-125">**Example**</span></span>

<span data-ttu-id="bbfdf-126">按一下矩形時，瀏覽器會載入 Microsoft Corporation 首頁。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="bbfdf-127">[HRef 屬性範例](/previous-versions/bb229672(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bbfdf-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="bbfdf-128"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="bbfdf-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 