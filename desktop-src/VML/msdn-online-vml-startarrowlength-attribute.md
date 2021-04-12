---
title: VML StartArrowLength 屬性
description: VML StartArrowLength 屬性
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375853"
---
# <a name="vml-startarrowlength-attribute"></a><span data-ttu-id="2c6fe-103">VML StartArrowLength 屬性</span><span class="sxs-lookup"><span data-stu-id="2c6fe-103">VML StartArrowLength Attribute</span></span>

<span data-ttu-id="2c6fe-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2c6fe-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2c6fe-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2c6fe-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2c6fe-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2c6fe-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2c6fe-110">定義線條開頭的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-110">Defines the arrowhead length for the start of a line.</span></span> <span data-ttu-id="2c6fe-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2c6fe-111">Read/write.</span></span> <span data-ttu-id="2c6fe-112">**VgArrowheadLength**。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="2c6fe-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="2c6fe-113">**Applies To**</span></span>

[<span data-ttu-id="2c6fe-114">中風</span><span class="sxs-lookup"><span data-stu-id="2c6fe-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="2c6fe-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="2c6fe-115">**Tag Syntax**</span></span>

<span data-ttu-id="2c6fe-116"><v： *element* startarrowlength = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2c6fe-116"><v: *element* startarrowlength=" *expression* "></span></span>

<span data-ttu-id="2c6fe-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="2c6fe-117">**Script Syntax**</span></span>

<span data-ttu-id="2c6fe-118"> startarrowlength = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2c6fe-118">*element* .startarrowlength="*expression*"</span></span>

<span data-ttu-id="2c6fe-119">*運算式* =\*\* startarrowlength</span><span class="sxs-lookup"><span data-stu-id="2c6fe-119">*expression*=*element*.startarrowlength</span></span>

<span data-ttu-id="2c6fe-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="2c6fe-120">**Remarks**</span></span>

<span data-ttu-id="2c6fe-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="2c6fe-121">Values include:</span></span>

-   <span data-ttu-id="2c6fe-122">Short</span><span class="sxs-lookup"><span data-stu-id="2c6fe-122">Short</span></span>
-   <span data-ttu-id="2c6fe-123">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="2c6fe-123">Medium (default)</span></span>
-   <span data-ttu-id="2c6fe-124">long</span><span class="sxs-lookup"><span data-stu-id="2c6fe-124">Long</span></span>

<span data-ttu-id="2c6fe-125">VML 標準屬性</span><span class="sxs-lookup"><span data-stu-id="2c6fe-125">VML Standard Attribute</span></span>

<span data-ttu-id="2c6fe-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="2c6fe-126">**Example**</span></span>

<span data-ttu-id="2c6fe-127">在筆劃的開頭，以簡短的傳統箭頭繪製線條。</span><span class="sxs-lookup"><span data-stu-id="2c6fe-127">A line is drawn with a short classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 