---
title: '類型屬性 (延伸)  (VML) '
description: '類型屬性 (延伸)  (VML) '
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842503"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="0a841-103">類型屬性 (延伸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="0a841-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="0a841-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0a841-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0a841-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0a841-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0a841-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0a841-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0a841-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0a841-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0a841-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0a841-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0a841-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0a841-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0a841-110">定義形狀的拉伸方式。</span><span class="sxs-lookup"><span data-stu-id="0a841-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="0a841-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0a841-111">Read/write.</span></span> <span data-ttu-id="0a841-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="0a841-112">**String**.</span></span>

<span data-ttu-id="0a841-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="0a841-113">**Applies To**</span></span>

[<span data-ttu-id="0a841-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="0a841-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="0a841-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="0a841-115">**Tag Syntax**</span></span>

<span data-ttu-id="0a841-116"><o： *element* type = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0a841-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="0a841-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="0a841-117">**Script Syntax**</span></span>

<span data-ttu-id="0a841-118">*element* 。 type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0a841-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="0a841-119">*運算式* =*元素*。類型</span><span class="sxs-lookup"><span data-stu-id="0a841-119">*expression*=*element*.type</span></span>

<span data-ttu-id="0a841-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="0a841-120">**Remarks**</span></span>

<span data-ttu-id="0a841-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="0a841-121">Values include:</span></span>



| <span data-ttu-id="0a841-122">值</span><span class="sxs-lookup"><span data-stu-id="0a841-122">Value</span></span>       | <span data-ttu-id="0a841-123">描述</span><span class="sxs-lookup"><span data-stu-id="0a841-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a841-124">parallel</span><span class="sxs-lookup"><span data-stu-id="0a841-124">parallel</span></span>    | <span data-ttu-id="0a841-125">會轉譯延伸，讓投射的中心無限遠地離開;也就是，不像) 的透視圖投影， (的拉伸線不會會合。</span><span class="sxs-lookup"><span data-stu-id="0a841-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="0a841-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="0a841-126">Default.</span></span> |
| <span data-ttu-id="0a841-127">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="0a841-127">perspective</span></span> | <span data-ttu-id="0a841-128">拉伸會轉譯為投影中心，與未旋轉物件的沒影點相同。</span><span class="sxs-lookup"><span data-stu-id="0a841-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="0a841-129">**Microsoft Office Extensions 屬性**</span><span class="sxs-lookup"><span data-stu-id="0a841-129">**Microsoft Office Extensions Attribute**</span></span>

 

 