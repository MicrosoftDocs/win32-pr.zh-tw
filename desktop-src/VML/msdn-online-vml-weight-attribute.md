---
title: VML 權數屬性
description: VML 權數屬性
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966249"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="1ad79-103">VML 權數屬性</span><span class="sxs-lookup"><span data-stu-id="1ad79-103">VML Weight Attribute</span></span>

<span data-ttu-id="1ad79-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="1ad79-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1ad79-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="1ad79-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1ad79-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="1ad79-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1ad79-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="1ad79-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1ad79-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="1ad79-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1ad79-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="1ad79-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1ad79-110">定義筆觸的粗細。</span><span class="sxs-lookup"><span data-stu-id="1ad79-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="1ad79-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1ad79-111">Read/write.</span></span> <span data-ttu-id="1ad79-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="1ad79-112">**String**.</span></span>

<span data-ttu-id="1ad79-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="1ad79-113">**Applies To**</span></span>

[<span data-ttu-id="1ad79-114">中風</span><span class="sxs-lookup"><span data-stu-id="1ad79-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="1ad79-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="1ad79-115">**Tag Syntax**</span></span>

<span data-ttu-id="1ad79-116"><v： *element* 權數 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1ad79-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="1ad79-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="1ad79-117">**Script Syntax**</span></span>

<span data-ttu-id="1ad79-118">*元素* 。權數 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1ad79-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="1ad79-119">*運算式* =*元素*。權數</span><span class="sxs-lookup"><span data-stu-id="1ad79-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="1ad79-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="1ad79-120">**Remarks**</span></span>

<span data-ttu-id="1ad79-121">這個屬性與 **Shape** 的 **StrokeWeight** 屬性相同，並會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="1ad79-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="1ad79-122">預設值為1點。</span><span class="sxs-lookup"><span data-stu-id="1ad79-122">The default value is 1 point.</span></span>

<span data-ttu-id="1ad79-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="1ad79-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1ad79-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="1ad79-124">**Example**</span></span>

<span data-ttu-id="1ad79-125">筆劃的粗細為5點，而不是2點。</span><span class="sxs-lookup"><span data-stu-id="1ad79-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 