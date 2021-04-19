---
title: VML JoinStyle 屬性
description: VML JoinStyle 屬性
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968908"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="603e2-103">VML JoinStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="603e2-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="603e2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="603e2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="603e2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="603e2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="603e2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="603e2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="603e2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="603e2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="603e2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="603e2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="603e2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="603e2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="603e2-110">定義折線的聯結樣式。</span><span class="sxs-lookup"><span data-stu-id="603e2-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="603e2-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="603e2-111">Read/write.</span></span> <span data-ttu-id="603e2-112">字串。</span><span class="sxs-lookup"><span data-stu-id="603e2-112">String.</span></span>

<span data-ttu-id="603e2-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="603e2-113">**Applies To**</span></span>

[<span data-ttu-id="603e2-114">中風</span><span class="sxs-lookup"><span data-stu-id="603e2-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="603e2-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="603e2-115">**Tag Syntax**</span></span>

<span data-ttu-id="603e2-116"><v： *element* joinstyle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="603e2-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="603e2-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="603e2-117">**Script Syntax**</span></span>

<span data-ttu-id="603e2-118"> joinstyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="603e2-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="603e2-119">*運算式* =\*\* joinstyle</span><span class="sxs-lookup"><span data-stu-id="603e2-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="603e2-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="603e2-120">**Remarks**</span></span>

<span data-ttu-id="603e2-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="603e2-121">Values include:</span></span>

-   <span data-ttu-id="603e2-122">四捨五入 (預設值) </span><span class="sxs-lookup"><span data-stu-id="603e2-122">round (default)</span></span>
-   <span data-ttu-id="603e2-123">錐</span><span class="sxs-lookup"><span data-stu-id="603e2-123">bevel</span></span>
-   <span data-ttu-id="603e2-124">長度</span><span class="sxs-lookup"><span data-stu-id="603e2-124">miter</span></span>

<span data-ttu-id="603e2-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="603e2-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="603e2-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="603e2-126">**Example**</span></span>

<span data-ttu-id="603e2-127">折線上的接點是斜邊。</span><span class="sxs-lookup"><span data-stu-id="603e2-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 