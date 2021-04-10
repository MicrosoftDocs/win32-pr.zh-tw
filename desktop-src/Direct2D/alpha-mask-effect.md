---
title: Alpha 遮罩效果
description: 此效果會將 Alpha 遮罩套用至影像。 它有兩個輸入，名為 Destination 和 Mask。 目的地影像中的色彩值會乘以遮罩影像的 Alpha 色板。
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106560"
---
# <a name="alpha-mask-effect"></a><span data-ttu-id="e7a08-105">Alpha 遮罩效果</span><span class="sxs-lookup"><span data-stu-id="e7a08-105">Alpha mask effect</span></span>

<span data-ttu-id="e7a08-106">此效果會將 Alpha 遮罩套用至影像。</span><span class="sxs-lookup"><span data-stu-id="e7a08-106">This effect applies an alpha mask to an image.</span></span> <span data-ttu-id="e7a08-107">它有兩個輸入，名為 Destination 和 Mask。</span><span class="sxs-lookup"><span data-stu-id="e7a08-107">It has two inputs, named Destination and Mask.</span></span> <span data-ttu-id="e7a08-108">目的地影像中的色彩值會乘以遮罩影像的 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="e7a08-108">Color values in the Destination image are multiplied by the alpha channel of the Mask image.</span></span>

<span data-ttu-id="e7a08-109">這項效果的 CLSID 是 CLSID \_ D2D1AlphaMask。</span><span class="sxs-lookup"><span data-stu-id="e7a08-109">The CLSID for this effect is CLSID\_D2D1AlphaMask.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="e7a08-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="e7a08-110">Effect properties</span></span>

<span data-ttu-id="e7a08-111">此效果沒有任何作用中的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="e7a08-111">This effect has no effect-specific properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a08-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7a08-112">Requirements</span></span>



| <span data-ttu-id="e7a08-113">需求</span><span class="sxs-lookup"><span data-stu-id="e7a08-113">Requirement</span></span> | <span data-ttu-id="e7a08-114">值</span><span class="sxs-lookup"><span data-stu-id="e7a08-114">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e7a08-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7a08-115">Minimum supported client</span></span> | <span data-ttu-id="e7a08-116">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7a08-116">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7a08-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7a08-117">Minimum supported server</span></span> | <span data-ttu-id="e7a08-118">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7a08-118">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7a08-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e7a08-119">Header</span></span>                   | <span data-ttu-id="e7a08-120">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="e7a08-120">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e7a08-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7a08-121">Library</span></span>                  | <span data-ttu-id="e7a08-122">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="e7a08-122">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="e7a08-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7a08-123">Related topics</span></span>

* [<span data-ttu-id="e7a08-124">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="e7a08-124">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

