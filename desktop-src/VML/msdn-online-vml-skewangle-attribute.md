---
title: VML SkewAngle 屬性
description: VML SkewAngle 屬性
ms.assetid: f9dc55ed-913c-409e-a045-8f95c83aabcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04775ae1edb3b276e531b6703761c09ea137072
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092872"
---
# <a name="vml-skewangle-attribute"></a><span data-ttu-id="28094-103">VML SkewAngle 屬性</span><span class="sxs-lookup"><span data-stu-id="28094-103">VML SkewAngle Attribute</span></span>

<span data-ttu-id="28094-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="28094-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="28094-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="28094-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="28094-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="28094-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="28094-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="28094-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="28094-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="28094-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="28094-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="28094-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="28094-110">定義拉伸的扭曲量。</span><span class="sxs-lookup"><span data-stu-id="28094-110">Defines the amount of skew of an extrusion.</span></span> <span data-ttu-id="28094-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="28094-111">Read/write.</span></span> <span data-ttu-id="28094-112">**VgAngle**。</span><span class="sxs-lookup"><span data-stu-id="28094-112">**VgAngle**.</span></span>

<span data-ttu-id="28094-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="28094-113">**Applies To**</span></span>

[<span data-ttu-id="28094-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="28094-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="28094-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="28094-115">**Tag Syntax**</span></span>

<span data-ttu-id="28094-116"><o： *element* skewangle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="28094-116"><o: *element* skewangle=" *expression* "></span></span>

<span data-ttu-id="28094-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="28094-117">**Script Syntax**</span></span>

<span data-ttu-id="28094-118"> skewangle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="28094-118">*element* .skewangle="*expression*"</span></span>

<span data-ttu-id="28094-119">*運算式* =\*\* skewangle</span><span class="sxs-lookup"><span data-stu-id="28094-119">*expression*=*element*.skewangle</span></span>

<span data-ttu-id="28094-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="28094-120">**Remarks**</span></span>

<span data-ttu-id="28094-121">只有當 [延伸 [類型](type-attribute--extrusion--vml.md) ] 屬性值為 [ *平行*] 時，才會套用至 [延伸]。</span><span class="sxs-lookup"><span data-stu-id="28094-121">Applies to an extrusion only if the extrusion [Type](type-attribute--extrusion--vml.md) attribute value is *parallel*.</span></span> <span data-ttu-id="28094-122">預設值為45度。</span><span class="sxs-lookup"><span data-stu-id="28094-122">Default value is 45 degrees.</span></span>

<span data-ttu-id="28094-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="28094-123">*Microsoft Office Extensions Attribute*</span></span>

 

 