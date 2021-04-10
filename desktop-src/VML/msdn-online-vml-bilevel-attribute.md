---
title: VML Bilevel 屬性
description: VML Bilevel 屬性
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682610"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="435e7-103">VML Bilevel 屬性</span><span class="sxs-lookup"><span data-stu-id="435e7-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="435e7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="435e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="435e7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="435e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="435e7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="435e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="435e7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="435e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="435e7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="435e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="435e7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="435e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="435e7-110">判斷影像是否會以黑色和白色顯示。</span><span class="sxs-lookup"><span data-stu-id="435e7-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="435e7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="435e7-111">Read/write.</span></span> <span data-ttu-id="435e7-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="435e7-112">**VgTriState**.</span></span>

<span data-ttu-id="435e7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="435e7-113">**Applies To**</span></span>

[<span data-ttu-id="435e7-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="435e7-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="435e7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="435e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="435e7-116"><v： *element* bilevel = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="435e7-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="435e7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="435e7-117">**Script Syntax**</span></span>

<span data-ttu-id="435e7-118"> bilevel = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="435e7-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="435e7-119">*運算式* =\*\* bilevel</span><span class="sxs-lookup"><span data-stu-id="435e7-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="435e7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="435e7-120">**Remarks**</span></span>

<span data-ttu-id="435e7-121">若 **為 True**，則會使用兩種色彩來顯示影像 (黑色和白色) 。</span><span class="sxs-lookup"><span data-stu-id="435e7-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="435e7-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="435e7-122">The default is **False**.</span></span> <span data-ttu-id="435e7-123">這會建立類似于 posterization 的效果。</span><span class="sxs-lookup"><span data-stu-id="435e7-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="435e7-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="435e7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="435e7-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="435e7-125">**Example**</span></span>

<span data-ttu-id="435e7-126">影像只會以黑色和白色顯示。</span><span class="sxs-lookup"><span data-stu-id="435e7-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 