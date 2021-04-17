---
title: VML EndCap 屬性
description: VML EndCap 屬性
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316417"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="63348-103">VML EndCap 屬性</span><span class="sxs-lookup"><span data-stu-id="63348-103">VML EndCap Attribute</span></span>

<span data-ttu-id="63348-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="63348-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63348-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="63348-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63348-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="63348-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63348-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="63348-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63348-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="63348-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63348-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="63348-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63348-110">定義筆劃結尾的端點樣式。</span><span class="sxs-lookup"><span data-stu-id="63348-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="63348-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="63348-111">Read/write.</span></span> <span data-ttu-id="63348-112">**VgLineEndCapStyle**。</span><span class="sxs-lookup"><span data-stu-id="63348-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="63348-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="63348-113">**Applies To**</span></span>

[<span data-ttu-id="63348-114">中風</span><span class="sxs-lookup"><span data-stu-id="63348-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="63348-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="63348-115">**Tag Syntax**</span></span>

<span data-ttu-id="63348-116"><v： *element* endcap = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="63348-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="63348-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="63348-117">**Script Syntax**</span></span>

<span data-ttu-id="63348-118"> endcap = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="63348-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="63348-119">*運算式* =\*\* endcap</span><span class="sxs-lookup"><span data-stu-id="63348-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="63348-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="63348-120">**Remarks**</span></span>

<span data-ttu-id="63348-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="63348-121">Values include:</span></span>

-   <span data-ttu-id="63348-122">一般 (預設) </span><span class="sxs-lookup"><span data-stu-id="63348-122">Flat (default)</span></span>
-   <span data-ttu-id="63348-123">Square</span><span class="sxs-lookup"><span data-stu-id="63348-123">Square</span></span>
-   <span data-ttu-id="63348-124">Round</span><span class="sxs-lookup"><span data-stu-id="63348-124">Round</span></span>

<span data-ttu-id="63348-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="63348-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="63348-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="63348-126">**Example**</span></span>

<span data-ttu-id="63348-127">線條會以水準端點在筆劃的結尾繪製。</span><span class="sxs-lookup"><span data-stu-id="63348-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 