---
title: VML LockRotationCenter 屬性
description: VML LockRotationCenter 屬性
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968513"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="3bef0-103">VML LockRotationCenter 屬性</span><span class="sxs-lookup"><span data-stu-id="3bef0-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="3bef0-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="3bef0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3bef0-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="3bef0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3bef0-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="3bef0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3bef0-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="3bef0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3bef0-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="3bef0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3bef0-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="3bef0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3bef0-110">判斷 [RotationAngle](msdn-online-vml-rotationangle-attribute.md) 屬性是否指定了拉伸物件的旋轉。</span><span class="sxs-lookup"><span data-stu-id="3bef0-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="3bef0-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3bef0-111">Read/write.</span></span> <span data-ttu-id="3bef0-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="3bef0-112">**VgTriState**.</span></span>

<span data-ttu-id="3bef0-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="3bef0-113">**Applies To**</span></span>

[<span data-ttu-id="3bef0-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="3bef0-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="3bef0-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="3bef0-115">**Tag Syntax**</span></span>

<span data-ttu-id="3bef0-116"><o： *element* lockrotationcenter = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3bef0-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="3bef0-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="3bef0-117">**Script Syntax**</span></span>

<span data-ttu-id="3bef0-118"> lockrotationcenter = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3bef0-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="3bef0-119">*運算式* =\*\* lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="3bef0-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="3bef0-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="3bef0-120">**Remarks**</span></span>

<span data-ttu-id="3bef0-121">如果 **為 False**，則表示旋轉是由 [方向](msdn-online-vml-orientation-attribute.md) 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="3bef0-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="3bef0-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="3bef0-122">The default is **True**.</span></span>

<span data-ttu-id="3bef0-123">請注意：</span><span class="sxs-lookup"><span data-stu-id="3bef0-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="3bef0-124">就如同：</span><span class="sxs-lookup"><span data-stu-id="3bef0-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="3bef0-125">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="3bef0-125">*Microsoft Office Extensions Attribute*</span></span>

 

 