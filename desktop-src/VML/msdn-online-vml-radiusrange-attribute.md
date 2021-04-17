---
title: VML RadiusRange 屬性
description: VML RadiusRange 屬性
ms.assetid: bff2b185-7683-4994-9104-09a7579f963d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085ccfbcfe39c9ac3ea47350deebc6c5c59e0fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463261"
---
# <a name="vml-radiusrange-attribute"></a><span data-ttu-id="103e9-103">VML RadiusRange 屬性</span><span class="sxs-lookup"><span data-stu-id="103e9-103">VML RadiusRange Attribute</span></span>

<span data-ttu-id="103e9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="103e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="103e9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="103e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="103e9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="103e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="103e9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="103e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="103e9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="103e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="103e9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="103e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="103e9-110">定義極座標控點的範圍。</span><span class="sxs-lookup"><span data-stu-id="103e9-110">Defines the range of a polar handle.</span></span> <span data-ttu-id="103e9-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103e9-111">Read/write.</span></span> <span data-ttu-id="103e9-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="103e9-112">**VgVector2D**.</span></span>

<span data-ttu-id="103e9-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="103e9-113">**Applies To**</span></span>

<span data-ttu-id="103e9-114">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="103e9-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="103e9-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="103e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="103e9-116"><v： *element* radiusrange = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="103e9-116"><v: *element* radiusrange=" *expression* "></span></span>

<span data-ttu-id="103e9-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="103e9-117">**Remarks**</span></span>

<span data-ttu-id="103e9-118">定義星形控制碼的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="103e9-118">A minimum and maximum value is defined for a radial handle.</span></span> <span data-ttu-id="103e9-119">每個值都可以是常數或公式。</span><span class="sxs-lookup"><span data-stu-id="103e9-119">Each value can be a constant or a formula.</span></span> <span data-ttu-id="103e9-120">如果未定義某個值，則可以在星形方向中移動控點，而不受限制。</span><span class="sxs-lookup"><span data-stu-id="103e9-120">If a value is not defined, the handle can be moved without limit in the radial direction.</span></span> <span data-ttu-id="103e9-121">這個屬性只適用于極座標控點。</span><span class="sxs-lookup"><span data-stu-id="103e9-121">This attribute applies only to polar adjust handles.</span></span> <span data-ttu-id="103e9-122">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="103e9-122">The default value is 0,0.</span></span>

<span data-ttu-id="103e9-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="103e9-123">*VML Standard Attribute*</span></span>

 

 