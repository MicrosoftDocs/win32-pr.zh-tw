---
title: VML 反光屬性
description: VML 反光屬性
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315226"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="2cd7d-103">VML 反光屬性</span><span class="sxs-lookup"><span data-stu-id="2cd7d-103">VML Shininess Attribute</span></span>

<span data-ttu-id="2cd7d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2cd7d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2cd7d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2cd7d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2cd7d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2cd7d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2cd7d-110">定義在拉伸表面上反射光源的集中。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="2cd7d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2cd7d-111">Read/write.</span></span> <span data-ttu-id="2cd7d-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-112">**VgNumber**.</span></span>

<span data-ttu-id="2cd7d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="2cd7d-113">**Applies To**</span></span>

[<span data-ttu-id="2cd7d-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="2cd7d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="2cd7d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="2cd7d-115">**Tag Syntax**</span></span>

<span data-ttu-id="2cd7d-116"><o： *element* 反光 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2cd7d-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="2cd7d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="2cd7d-117">**Script Syntax**</span></span>

<span data-ttu-id="2cd7d-118">*element* 。反光 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2cd7d-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="2cd7d-119">*運算式* =*元素*。反光</span><span class="sxs-lookup"><span data-stu-id="2cd7d-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="2cd7d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="2cd7d-120">**Remarks**</span></span>

<span data-ttu-id="2cd7d-121">高值 (8-10) 會接近鏡像和低值的反光 (2-3) 會接近 speckled 的效果。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="2cd7d-122">4-7 的值是一般的。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="2cd7d-123">反射不會鏡像其他物件;只會反映精確的光源。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="2cd7d-124">預設值為 5。</span><span class="sxs-lookup"><span data-stu-id="2cd7d-124">Default value is 5.</span></span>

<span data-ttu-id="2cd7d-125">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="2cd7d-125">*Microsoft Office Extensions Attribute*</span></span>

 

 