---
title: VML LightPosition2 屬性
description: VML LightPosition2 屬性
ms.assetid: 75ae4154-240f-4981-a527-d9e0a721e8b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5306be47bec8b72b6bafc49e404b3369ace19e50
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315310"
---
# <a name="vml-lightposition2-attribute"></a><span data-ttu-id="1724c-103">VML LightPosition2 屬性</span><span class="sxs-lookup"><span data-stu-id="1724c-103">VML LightPosition2 Attribute</span></span>

<span data-ttu-id="1724c-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="1724c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1724c-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="1724c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1724c-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="1724c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1724c-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="1724c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1724c-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="1724c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1724c-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="1724c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1724c-110">指定場景中次要光源的位置。</span><span class="sxs-lookup"><span data-stu-id="1724c-110">Specifies the position of the secondary light in a scene.</span></span> <span data-ttu-id="1724c-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1724c-111">Read/write.</span></span> <span data-ttu-id="1724c-112">**VgVector3D**。</span><span class="sxs-lookup"><span data-stu-id="1724c-112">**VgVector3D**.</span></span>

<span data-ttu-id="1724c-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="1724c-113">**Applies To**</span></span>

[<span data-ttu-id="1724c-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="1724c-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="1724c-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="1724c-115">**Tag Syntax**</span></span>

<span data-ttu-id="1724c-116"><o： *element* lightposition2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1724c-116"><o: *element* lightposition2=" *expression* "></span></span>

<span data-ttu-id="1724c-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="1724c-117">**Script Syntax**</span></span>

<span data-ttu-id="1724c-118"> lightposition2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1724c-118">*element* .lightposition2="*expression*"</span></span>

<span data-ttu-id="1724c-119">*運算式* =\*\* lightposition2</span><span class="sxs-lookup"><span data-stu-id="1724c-119">*expression*=*element*.lightposition2</span></span>

<span data-ttu-id="1724c-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="1724c-120">**Remarks**</span></span>

<span data-ttu-id="1724c-121">您可以使用此值來移動延伸的第二個燈光來源。</span><span class="sxs-lookup"><span data-stu-id="1724c-121">Use this value to move the second light source for an extrusion.</span></span> <span data-ttu-id="1724c-122">不同的位置將會淡化，或使每個區域的外觀變暗。</span><span class="sxs-lookup"><span data-stu-id="1724c-122">Different positions will lighten or darken each face of the extrusion.</span></span> <span data-ttu-id="1724c-123">預設值為-50000、0、10000。</span><span class="sxs-lookup"><span data-stu-id="1724c-123">The default value is -50000, 0, 10000.</span></span>

<span data-ttu-id="1724c-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="1724c-124">*Microsoft Office Extensions Attribute*</span></span>

 

 