---
description: 下列函式可用於筆刷。
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: " (Windows GDI) 的筆刷函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512924"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="8bc82-103"> (Windows GDI) 的筆刷函數</span><span class="sxs-lookup"><span data-stu-id="8bc82-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="8bc82-104">下列函式可用於筆刷。</span><span class="sxs-lookup"><span data-stu-id="8bc82-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="8bc82-105">函式</span><span class="sxs-lookup"><span data-stu-id="8bc82-105">Function</span></span>                                                   | <span data-ttu-id="8bc82-106">描述</span><span class="sxs-lookup"><span data-stu-id="8bc82-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="8bc82-107">**CreateBrushIndirect**</span><span class="sxs-lookup"><span data-stu-id="8bc82-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="8bc82-108">使用指定的樣式、色彩和模式建立筆刷</span><span class="sxs-lookup"><span data-stu-id="8bc82-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="8bc82-109">**CreateDIBPatternBrushPt**</span><span class="sxs-lookup"><span data-stu-id="8bc82-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="8bc82-110">使用 DIB 的模式建立筆刷</span><span class="sxs-lookup"><span data-stu-id="8bc82-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="8bc82-111">**CreateHatchBrush**</span><span class="sxs-lookup"><span data-stu-id="8bc82-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="8bc82-112">使用影線圖樣和色彩建立筆刷</span><span class="sxs-lookup"><span data-stu-id="8bc82-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="8bc82-113">**CreatePatternBrush**</span><span class="sxs-lookup"><span data-stu-id="8bc82-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="8bc82-114">使用點陣圖模式建立筆刷</span><span class="sxs-lookup"><span data-stu-id="8bc82-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="8bc82-115">**CreateSolidBrush**</span><span class="sxs-lookup"><span data-stu-id="8bc82-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="8bc82-116">以純色建立筆刷</span><span class="sxs-lookup"><span data-stu-id="8bc82-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="8bc82-117">**GetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="8bc82-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="8bc82-118">取得裝置內容的筆刷來源</span><span class="sxs-lookup"><span data-stu-id="8bc82-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="8bc82-119">**GetSysColorBrush**</span><span class="sxs-lookup"><span data-stu-id="8bc82-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="8bc82-120">取得對應至色彩索引之筆刷的控制碼</span><span class="sxs-lookup"><span data-stu-id="8bc82-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="8bc82-121">**PatBlt**</span><span class="sxs-lookup"><span data-stu-id="8bc82-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="8bc82-122">繪製矩形</span><span class="sxs-lookup"><span data-stu-id="8bc82-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="8bc82-123">**SetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="8bc82-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="8bc82-124">設定裝置內容的筆刷來源</span><span class="sxs-lookup"><span data-stu-id="8bc82-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="8bc82-125">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="8bc82-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="8bc82-126">設定目前的裝置內容筆刷色彩。</span><span class="sxs-lookup"><span data-stu-id="8bc82-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="8bc82-127">過時的函式</span><span class="sxs-lookup"><span data-stu-id="8bc82-127">Obsolete Functions</span></span>

<span data-ttu-id="8bc82-128">下列函式僅提供給 Windows 的16位版本相容。</span><span class="sxs-lookup"><span data-stu-id="8bc82-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="8bc82-129">**CreateDIBPatternBrush**</span><span class="sxs-lookup"><span data-stu-id="8bc82-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



