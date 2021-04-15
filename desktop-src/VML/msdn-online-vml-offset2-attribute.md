---
title: VML Offset2 屬性
description: VML Offset2 屬性
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508091"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="4d086-103">VML Offset2 屬性</span><span class="sxs-lookup"><span data-stu-id="4d086-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="4d086-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4d086-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4d086-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4d086-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4d086-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4d086-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4d086-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4d086-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4d086-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4d086-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4d086-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4d086-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4d086-110">決定第二個位移。</span><span class="sxs-lookup"><span data-stu-id="4d086-110">Determines a second offset.</span></span> <span data-ttu-id="4d086-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4d086-111">Read/write.</span></span> <span data-ttu-id="4d086-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="4d086-112">**VgVector2D**.</span></span>

<span data-ttu-id="4d086-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4d086-113">**Applies To**</span></span>

[<span data-ttu-id="4d086-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="4d086-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="4d086-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4d086-115">**Tag Syntax**</span></span>

<span data-ttu-id="4d086-116"><v： *element* offset2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4d086-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="4d086-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4d086-117">**Script Syntax**</span></span>

<span data-ttu-id="4d086-118"> offset2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4d086-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="4d086-119">*運算式* =\*\* offset2</span><span class="sxs-lookup"><span data-stu-id="4d086-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="4d086-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4d086-120">**Remarks**</span></span>

<span data-ttu-id="4d086-121">X 值的第二個位移預設值為0，而 y 值的預設值為0。</span><span class="sxs-lookup"><span data-stu-id="4d086-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="4d086-122">值可以是絕對測量值，或是 shape 的小數值。</span><span class="sxs-lookup"><span data-stu-id="4d086-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="4d086-123">如果是小數，則值的範圍是從50% 到-50%。</span><span class="sxs-lookup"><span data-stu-id="4d086-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="4d086-124">使用第二個位移來建立特殊的陰影效果。</span><span class="sxs-lookup"><span data-stu-id="4d086-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="4d086-125">如需第二個位移的詳細資訊，請參閱 [Type](type-attribute--shadow--vml.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4d086-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="4d086-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="4d086-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="4d086-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="4d086-127">**Example**</span></span>

<span data-ttu-id="4d086-128">為圖形建立雙重陰影。</span><span class="sxs-lookup"><span data-stu-id="4d086-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 