---
title: VML EndArrowLength 屬性
description: VML EndArrowLength 屬性
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965021"
---
# <a name="vml-endarrowlength-attribute"></a><span data-ttu-id="9af8f-103">VML EndArrowLength 屬性</span><span class="sxs-lookup"><span data-stu-id="9af8f-103">VML EndArrowLength Attribute</span></span>

<span data-ttu-id="9af8f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="9af8f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9af8f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="9af8f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9af8f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="9af8f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9af8f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="9af8f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9af8f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="9af8f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9af8f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="9af8f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9af8f-110">定義線條結尾的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="9af8f-110">Defines an arrowhead length for the end of a line.</span></span> <span data-ttu-id="9af8f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9af8f-111">Read/write.</span></span> <span data-ttu-id="9af8f-112">**VgArrowheadLength**。</span><span class="sxs-lookup"><span data-stu-id="9af8f-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="9af8f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="9af8f-113">**Applies To**</span></span>

[<span data-ttu-id="9af8f-114">中風</span><span class="sxs-lookup"><span data-stu-id="9af8f-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="9af8f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="9af8f-115">**Tag Syntax**</span></span>

<span data-ttu-id="9af8f-116"><v： *element* endarrowlength = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9af8f-116"><v: *element* endarrowlength=" *expression* "></span></span>

<span data-ttu-id="9af8f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="9af8f-117">**Script Syntax**</span></span>

<span data-ttu-id="9af8f-118"> endarrowlength = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9af8f-118">*element* .endarrowlength="*expression*"</span></span>

<span data-ttu-id="9af8f-119">*運算式* =\*\* endarrowlength</span><span class="sxs-lookup"><span data-stu-id="9af8f-119">*expression*=*element*.endarrowlength</span></span>

<span data-ttu-id="9af8f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="9af8f-120">**Remarks**</span></span>

<span data-ttu-id="9af8f-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="9af8f-121">Values include:</span></span>

-   <span data-ttu-id="9af8f-122">Short</span><span class="sxs-lookup"><span data-stu-id="9af8f-122">Short</span></span>
-   <span data-ttu-id="9af8f-123">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="9af8f-123">Medium (default)</span></span>
-   <span data-ttu-id="9af8f-124">long</span><span class="sxs-lookup"><span data-stu-id="9af8f-124">Long</span></span>

<span data-ttu-id="9af8f-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="9af8f-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="9af8f-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="9af8f-126">**Example**</span></span>

<span data-ttu-id="9af8f-127">在筆劃末端以簡短的傳統箭頭繪製線條。</span><span class="sxs-lookup"><span data-stu-id="9af8f-127">A line is drawn with a short classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 