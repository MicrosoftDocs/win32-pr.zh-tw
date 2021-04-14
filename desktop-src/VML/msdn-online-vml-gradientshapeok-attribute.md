---
title: VML GradientShapeOK 屬性
description: VML GradientShapeOK 屬性
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382673"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="23fa5-103">VML GradientShapeOK 屬性</span><span class="sxs-lookup"><span data-stu-id="23fa5-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="23fa5-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="23fa5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="23fa5-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="23fa5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="23fa5-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="23fa5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="23fa5-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="23fa5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="23fa5-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="23fa5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="23fa5-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="23fa5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="23fa5-110">判斷漸層路徑是否會由重複的同心圓路徑組成。</span><span class="sxs-lookup"><span data-stu-id="23fa5-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="23fa5-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23fa5-111">Read/write.</span></span> <span data-ttu-id="23fa5-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="23fa5-112">**VgTriState**.</span></span>

<span data-ttu-id="23fa5-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="23fa5-113">**Applies To**</span></span>

[<span data-ttu-id="23fa5-114">路徑</span><span class="sxs-lookup"><span data-stu-id="23fa5-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="23fa5-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="23fa5-115">**Tag Syntax**</span></span>

<span data-ttu-id="23fa5-116"><v： *element* gradientshapeok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="23fa5-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="23fa5-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="23fa5-117">**Script Syntax**</span></span>

<span data-ttu-id="23fa5-118"> gradientshapeok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="23fa5-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="23fa5-119">*運算式* =\*\* gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="23fa5-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="23fa5-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="23fa5-120">**Remarks**</span></span>

<span data-ttu-id="23fa5-121">若 **為 True**，則會使用路徑作為漸層的重複圖形來填滿路徑，並以同心圓漸層填滿。預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="23fa5-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="23fa5-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="23fa5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="23fa5-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="23fa5-123">**Example**</span></span>

<span data-ttu-id="23fa5-124">路徑將會填入由重複矩形組成的同心圓漸層填滿。</span><span class="sxs-lookup"><span data-stu-id="23fa5-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 