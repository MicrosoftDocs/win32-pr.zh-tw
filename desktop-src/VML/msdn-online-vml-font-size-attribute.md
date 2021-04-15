---
title: VML Font-Size 屬性
description: VML Font-Size 屬性
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463676"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="36e39-103">VML Font-Size 屬性</span><span class="sxs-lookup"><span data-stu-id="36e39-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="36e39-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="36e39-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36e39-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="36e39-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36e39-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="36e39-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36e39-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="36e39-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36e39-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="36e39-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36e39-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="36e39-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="36e39-110">定義字型的大小。</span><span class="sxs-lookup"><span data-stu-id="36e39-110">Defines the size of the font.</span></span> <span data-ttu-id="36e39-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36e39-111">Read/write.</span></span> <span data-ttu-id="36e39-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="36e39-112">**String**.</span></span>

<span data-ttu-id="36e39-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="36e39-113">**Applies To**</span></span>

[<span data-ttu-id="36e39-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="36e39-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="36e39-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="36e39-115">**Tag Syntax**</span></span>

<span data-ttu-id="36e39-116"><v： *element* style = "font-size： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="36e39-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="36e39-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="36e39-117">**Script Syntax**</span></span>

<span data-ttu-id="36e39-118"> fontsize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="36e39-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="36e39-119">*運算式* =\*\* fontsize</span><span class="sxs-lookup"><span data-stu-id="36e39-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="36e39-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="36e39-120">**Remarks**</span></span>

<span data-ttu-id="36e39-121">字型大小是以點定義。</span><span class="sxs-lookup"><span data-stu-id="36e39-121">The font size is defined in points.</span></span> <span data-ttu-id="36e39-122">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="36e39-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="36e39-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="36e39-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="36e39-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="36e39-124">**Example**</span></span>

<span data-ttu-id="36e39-125">字型大小為36點。</span><span class="sxs-lookup"><span data-stu-id="36e39-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 