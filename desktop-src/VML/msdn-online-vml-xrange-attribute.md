---
title: VML XRange 屬性
description: VML XRange 屬性
ms.assetid: c2881fd6-08b2-4ec8-b4fd-b271a049da09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f206afce0744ad7a83b30a7eac6de5590b3ea49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001282"
---
# <a name="vml-xrange-attribute"></a><span data-ttu-id="7cfe2-103">VML XRange 屬性</span><span class="sxs-lookup"><span data-stu-id="7cfe2-103">VML XRange Attribute</span></span>

<span data-ttu-id="7cfe2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7cfe2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7cfe2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7cfe2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7cfe2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7cfe2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7cfe2-110">定義控制碼的 thexrange。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-110">Defines thexrange of a handle.</span></span> <span data-ttu-id="7cfe2-111">讀取/寫入 **VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="7cfe2-112">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7cfe2-112">**Applies To**</span></span>

<span data-ttu-id="7cfe2-113">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="7cfe2-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="7cfe2-114">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7cfe2-114">**Tag Syntax**</span></span>

<span data-ttu-id="7cfe2-115"><v： *element* xrange = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7cfe2-115"><v: *element* xrange=" *expression* "></span></span>

<span data-ttu-id="7cfe2-116">**備註**</span><span class="sxs-lookup"><span data-stu-id="7cfe2-116">**Remarks**</span></span>

<span data-ttu-id="7cfe2-117">最小值和最大值是針對 x 方向的控制碼所定義。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-117">A minimum and maximum value is defined for the handle in the x direction.</span></span> <span data-ttu-id="7cfe2-118">每個值都可以是常數或公式。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-118">Each value can be a constant or a formula.</span></span> <span data-ttu-id="7cfe2-119">如果未定義某個值，則可以移動控點，而不會有此方向的限制。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-119">If a value is not defined, the handle can be moved without limit in this direction.</span></span> <span data-ttu-id="7cfe2-120">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="7cfe2-120">The default value is 0,0.</span></span>

<span data-ttu-id="7cfe2-121">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7cfe2-121">*VML Standard Attribute*</span></span>

 

 