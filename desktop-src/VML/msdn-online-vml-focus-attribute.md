---
title: VML 焦點屬性
description: VML 焦點屬性
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024071"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="29627-103">VML 焦點屬性</span><span class="sxs-lookup"><span data-stu-id="29627-103">VML Focus Attribute</span></span>

<span data-ttu-id="29627-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="29627-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29627-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="29627-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29627-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="29627-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29627-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="29627-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29627-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="29627-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29627-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="29627-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29627-110">定義線性漸層填滿的中心。</span><span class="sxs-lookup"><span data-stu-id="29627-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="29627-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="29627-111">Read/write.</span></span> <span data-ttu-id="29627-112">**VgFraction**。</span><span class="sxs-lookup"><span data-stu-id="29627-112">**VgFraction**.</span></span>

<span data-ttu-id="29627-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="29627-113">**Applies To**</span></span>

[<span data-ttu-id="29627-114">填滿</span><span class="sxs-lookup"><span data-stu-id="29627-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="29627-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="29627-115">**Tag Syntax**</span></span>

<span data-ttu-id="29627-116"><v： *element* focus = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="29627-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="29627-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="29627-117">**Script Syntax**</span></span>

<span data-ttu-id="29627-118">*element* 。 focus = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="29627-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="29627-119">*運算式* =*元素*。焦點</span><span class="sxs-lookup"><span data-stu-id="29627-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="29627-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="29627-120">**Remarks**</span></span>

<span data-ttu-id="29627-121">定義 blend 的中心開始位置。</span><span class="sxs-lookup"><span data-stu-id="29627-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="29627-122">值的範圍從100% 到-100%。</span><span class="sxs-lookup"><span data-stu-id="29627-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="29627-123">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="29627-123">The default value is 0.</span></span> <span data-ttu-id="29627-124">值為 100% (或-100% ) 將會轉移焦點，讓 blend 的方向會反轉 (效果反轉 **色彩** 和 **Color2**) 。</span><span class="sxs-lookup"><span data-stu-id="29627-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="29627-125">50% 的值將會變更 blend，讓 **色彩** 在兩端，且 **Color2** 在中間。</span><span class="sxs-lookup"><span data-stu-id="29627-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="29627-126">值為-50% 將會變更 blend，讓 **Color2** 同時在結尾，而 **色彩** 則在中間。</span><span class="sxs-lookup"><span data-stu-id="29627-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="29627-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="29627-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="29627-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="29627-128">**Example**</span></span>

<span data-ttu-id="29627-129">填滿填滿的漸層焦點，如此紅色的 (**色彩**) 就會是圖形中央的一個寬線，而頂端和底部會是藍色 (**Color2**) 。</span><span class="sxs-lookup"><span data-stu-id="29627-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 