---
title: '來源屬性 (陰影)  (VML) '
description: '來源屬性 (陰影)  (VML) '
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683031"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="fc8b6-103">來源屬性 (陰影)  (VML) </span><span class="sxs-lookup"><span data-stu-id="fc8b6-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="fc8b6-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fc8b6-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fc8b6-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fc8b6-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fc8b6-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fc8b6-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fc8b6-110">定義陰影的中心。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-110">Defines the center of the shadow.</span></span> <span data-ttu-id="fc8b6-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fc8b6-111">Read/write.</span></span> <span data-ttu-id="fc8b6-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-112">**VgVector2D**.</span></span>

<span data-ttu-id="fc8b6-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="fc8b6-113">**Applies To**</span></span>

[<span data-ttu-id="fc8b6-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="fc8b6-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="fc8b6-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="fc8b6-115">**Tag Syntax**</span></span>

<span data-ttu-id="fc8b6-116"><v： *element* 原點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fc8b6-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="fc8b6-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="fc8b6-117">**Script Syntax**</span></span>

<span data-ttu-id="fc8b6-118">*element* 。源 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="fc8b6-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="fc8b6-119">*運算式* =*元素*。來源</span><span class="sxs-lookup"><span data-stu-id="fc8b6-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="fc8b6-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="fc8b6-120">**Remarks**</span></span>

<span data-ttu-id="fc8b6-121">圖形的一對小數值，範圍從50% 到-50%。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="fc8b6-122">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-122">The default value is 0,0.</span></span>

<span data-ttu-id="fc8b6-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="fc8b6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="fc8b6-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="fc8b6-124">**Example**</span></span>

<span data-ttu-id="fc8b6-125">陰影有一個原點，也就是圖形原點右邊的20% 到20%。</span><span class="sxs-lookup"><span data-stu-id="fc8b6-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 