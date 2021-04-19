---
title: 不透明度效果
description: 此效果會將輸入的 Alpha 色板乘以指定的不透明度值，以調整影像的不透明度。 它有單一輸入。
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969602"
---
# <a name="opacity-effect"></a><span data-ttu-id="28195-104">不透明度效果</span><span class="sxs-lookup"><span data-stu-id="28195-104">Opacity effect</span></span>

<span data-ttu-id="28195-105">此效果會將輸入的 Alpha 色板乘以指定的不透明度值，以調整影像的不透明度。</span><span class="sxs-lookup"><span data-stu-id="28195-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="28195-106">它有單一輸入。</span><span class="sxs-lookup"><span data-stu-id="28195-106">It has a single input.</span></span>

<span data-ttu-id="28195-107">這項效果的 CLSID 是 CLSID \_ D2D1Opacity。</span><span class="sxs-lookup"><span data-stu-id="28195-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="28195-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="28195-108">Effect properties</span></span>



| <span data-ttu-id="28195-109">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="28195-109">Display name and index enumeration</span></span>              | <span data-ttu-id="28195-110">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="28195-110">Type and default value</span></span> | <span data-ttu-id="28195-111">Description</span><span class="sxs-lookup"><span data-stu-id="28195-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28195-112">不透明度 \_ D2D1 不透明度的情況 \_ \_</span><span class="sxs-lookup"><span data-stu-id="28195-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="28195-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="28195-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="28195-114">輸入影像 Alpha 色板的乘數。</span><span class="sxs-lookup"><span data-stu-id="28195-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="28195-115">最小值為 0.0 f，最大值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="28195-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="28195-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="28195-116">Requirements</span></span>



| <span data-ttu-id="28195-117">需求</span><span class="sxs-lookup"><span data-stu-id="28195-117">Requirement</span></span> | <span data-ttu-id="28195-118">值</span><span class="sxs-lookup"><span data-stu-id="28195-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="28195-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28195-119">Minimum supported client</span></span> | <span data-ttu-id="28195-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28195-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="28195-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28195-121">Minimum supported server</span></span> | <span data-ttu-id="28195-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28195-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="28195-123">標頭</span><span class="sxs-lookup"><span data-stu-id="28195-123">Header</span></span>                   | <span data-ttu-id="28195-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="28195-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="28195-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="28195-125">Library</span></span>                  | <span data-ttu-id="28195-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="28195-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="28195-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="28195-127">Related topics</span></span>

* [<span data-ttu-id="28195-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="28195-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
