---
title: VML ViewpointOrigin 屬性
description: VML ViewpointOrigin 屬性
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463280"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="b546b-103">VML ViewpointOrigin 屬性</span><span class="sxs-lookup"><span data-stu-id="b546b-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="b546b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b546b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b546b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b546b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b546b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b546b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b546b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b546b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b546b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b546b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b546b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b546b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b546b-110">定義圖形周框方塊內的觀點原點。</span><span class="sxs-lookup"><span data-stu-id="b546b-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="b546b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b546b-111">Read/write.</span></span> <span data-ttu-id="b546b-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="b546b-112">**VgVector2D**.</span></span>

<span data-ttu-id="b546b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b546b-113">**Applies To**</span></span>

[<span data-ttu-id="b546b-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="b546b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b546b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b546b-115">**Tag Syntax**</span></span>

<span data-ttu-id="b546b-116"><o： *element* viewpointorigin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b546b-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="b546b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b546b-117">**Script Syntax**</span></span>

<span data-ttu-id="b546b-118"> viewpointorigin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b546b-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="b546b-119">*運算式* =\*\* viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="b546b-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="b546b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b546b-120">**Remarks**</span></span>

<span data-ttu-id="b546b-121">根據原始圖形的 x 和 y 值來定義觀點。</span><span class="sxs-lookup"><span data-stu-id="b546b-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="b546b-122">X 和 y 值的範圍是從0.5 到-0.5 (50% 到圖形座標原點) 的50%。</span><span class="sxs-lookup"><span data-stu-id="b546b-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="b546b-123">預設值為0，0。</span><span class="sxs-lookup"><span data-stu-id="b546b-123">The default is 0,0.</span></span>

<span data-ttu-id="b546b-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="b546b-124">*Microsoft Office Extensions Attribute*</span></span>

 

 