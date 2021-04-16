---
title: VML 樣式屬性
description: VML 樣式屬性
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463189"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="b4551-103">VML 樣式屬性</span><span class="sxs-lookup"><span data-stu-id="b4551-103">VML Style Attribute</span></span>

<span data-ttu-id="b4551-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b4551-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b4551-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b4551-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b4551-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b4551-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b4551-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b4551-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b4551-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b4551-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b4551-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b4551-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b4551-110">定義框架的樣式。</span><span class="sxs-lookup"><span data-stu-id="b4551-110">Defines the style of the frame.</span></span> <span data-ttu-id="b4551-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b4551-111">Read/write.</span></span> <span data-ttu-id="b4551-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b4551-112">**String**.</span></span>

<span data-ttu-id="b4551-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b4551-113">**Applies To**</span></span>

[<span data-ttu-id="b4551-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="b4551-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="b4551-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b4551-115">**Tag Syntax**</span></span>

<span data-ttu-id="b4551-116"><v： *element* style = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b4551-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="b4551-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b4551-117">**Script Syntax**</span></span>

<span data-ttu-id="b4551-118">*元素* 。 style = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b4551-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="b4551-119">*運算式* =*element*。 style</span><span class="sxs-lookup"><span data-stu-id="b4551-119">*expression*=*element*.style</span></span>

<span data-ttu-id="b4551-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b4551-120">**Remarks**</span></span>

<span data-ttu-id="b4551-121">這個屬性會使用一般 CSS 樣式屬性來進行定位。</span><span class="sxs-lookup"><span data-stu-id="b4551-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="b4551-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b4551-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="b4551-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="b4551-123">**Example**</span></span>

<span data-ttu-id="b4551-124">樣式會定義框架的實際位置。</span><span class="sxs-lookup"><span data-stu-id="b4551-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 