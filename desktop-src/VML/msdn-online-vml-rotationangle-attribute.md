---
title: VML RotationAngle 屬性
description: VML RotationAngle 屬性
ms.assetid: d5432512-1ac2-497b-a415-cec3c1217120
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8af10704c74138192453894427f74003543510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967270"
---
# <a name="vml-rotationangle-attribute"></a><span data-ttu-id="0574b-103">VML RotationAngle 屬性</span><span class="sxs-lookup"><span data-stu-id="0574b-103">VML RotationAngle Attribute</span></span>

<span data-ttu-id="0574b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0574b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0574b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0574b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0574b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0574b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0574b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0574b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0574b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0574b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0574b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0574b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0574b-110">指定物件的 x 和 y 軸旋轉。</span><span class="sxs-lookup"><span data-stu-id="0574b-110">Specifies the rotation of the object about the x and y -axes.</span></span> <span data-ttu-id="0574b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0574b-111">Read/write.</span></span> <span data-ttu-id="0574b-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="0574b-112">**VgVector2D**.</span></span>

<span data-ttu-id="0574b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="0574b-113">**Applies To**</span></span>

[<span data-ttu-id="0574b-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="0574b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="0574b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="0574b-115">**Tag Syntax**</span></span>

<span data-ttu-id="0574b-116"><o： *element* rotationangle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0574b-116"><o: *element* rotationangle=" *expression* "></span></span>

<span data-ttu-id="0574b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="0574b-117">**Script Syntax**</span></span>

<span data-ttu-id="0574b-118"> rotationangle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0574b-118">*element* .rotationangle="*expression*"</span></span>

<span data-ttu-id="0574b-119">*運算式* =\*\* rotationangle</span><span class="sxs-lookup"><span data-stu-id="0574b-119">*expression*=*element*.rotationangle</span></span>

<span data-ttu-id="0574b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="0574b-120">**Remarks**</span></span>

<span data-ttu-id="0574b-121">物件的旋轉是由 y 軸的旋轉角度定義，後面接著 X 軸的旋轉角度。Z 軸角度是由圖形標準 HTML 樣式 **旋轉** 屬性的值所控制。</span><span class="sxs-lookup"><span data-stu-id="0574b-121">The rotation of the object is defined by a rotation angle about the y-axis followed by the rotation angle about the x-axis.The z-axis angle is controlled by the value of the shape's standard HTML Style **Rotation** attribute.</span></span> <span data-ttu-id="0574b-122">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="0574b-122">The default value is 0,0.</span></span>

<span data-ttu-id="0574b-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="0574b-123">*Microsoft Office Extensions Attribute*</span></span>

 

 