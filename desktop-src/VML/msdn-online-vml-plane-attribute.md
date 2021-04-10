---
title: VML 平面屬性
description: VML 平面屬性
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933339"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="b84c2-103">VML 平面屬性</span><span class="sxs-lookup"><span data-stu-id="b84c2-103">VML Plane Attribute</span></span>

<span data-ttu-id="b84c2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b84c2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b84c2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b84c2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b84c2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b84c2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b84c2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b84c2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b84c2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b84c2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b84c2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b84c2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b84c2-110">將平面指定為與視角的直角。</span><span class="sxs-lookup"><span data-stu-id="b84c2-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="b84c2-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b84c2-111">Read/write.</span></span> <span data-ttu-id="b84c2-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b84c2-112">**String**.</span></span>

<span data-ttu-id="b84c2-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b84c2-113">**Applies To**</span></span>

[<span data-ttu-id="b84c2-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="b84c2-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b84c2-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b84c2-115">**Tag Syntax**</span></span>

<span data-ttu-id="b84c2-116"><o： *element* 平面 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b84c2-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="b84c2-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b84c2-117">**Script Syntax**</span></span>

<span data-ttu-id="b84c2-118">*元素* 。平面 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b84c2-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="b84c2-119">*運算式* =*元素*。平面</span><span class="sxs-lookup"><span data-stu-id="b84c2-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="b84c2-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b84c2-120">**Remarks**</span></span>

<span data-ttu-id="b84c2-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="b84c2-121">Values include:</span></span>



| <span data-ttu-id="b84c2-122">值</span><span class="sxs-lookup"><span data-stu-id="b84c2-122">Value</span></span> | <span data-ttu-id="b84c2-123">描述</span><span class="sxs-lookup"><span data-stu-id="b84c2-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="b84c2-124">xy</span><span class="sxs-lookup"><span data-stu-id="b84c2-124">xy</span></span>    | <span data-ttu-id="b84c2-125">對 xy 平面而言，會以正向的角度進行。</span><span class="sxs-lookup"><span data-stu-id="b84c2-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="b84c2-126">預設</span><span class="sxs-lookup"><span data-stu-id="b84c2-126">Default</span></span> |
| <span data-ttu-id="b84c2-127">Zx</span><span class="sxs-lookup"><span data-stu-id="b84c2-127">zx</span></span>    | <span data-ttu-id="b84c2-128">Zx 平面的視角是以直角。</span><span class="sxs-lookup"><span data-stu-id="b84c2-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="b84c2-129">yz</span><span class="sxs-lookup"><span data-stu-id="b84c2-129">yz</span></span>    | <span data-ttu-id="b84c2-130">Yz 平面的視角是以直角。</span><span class="sxs-lookup"><span data-stu-id="b84c2-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="b84c2-131">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="b84c2-131">*Microsoft Office Extensions Attribute*</span></span>

 

 