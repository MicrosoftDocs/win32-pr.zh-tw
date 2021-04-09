---
title: 色調效果
description: 這會影響來源影像的色彩，方法是將來源影像乘以指定的色彩。 它有單一輸入。
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934305"
---
# <a name="tint-effect"></a><span data-ttu-id="3e2c4-104">色調效果</span><span class="sxs-lookup"><span data-stu-id="3e2c4-104">Tint effect</span></span>

<span data-ttu-id="3e2c4-105">這會影響來源影像的色彩，方法是將來源影像乘以指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="3e2c4-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="3e2c4-106">它有單一輸入。</span><span class="sxs-lookup"><span data-stu-id="3e2c4-106">It has a single input.</span></span>

<span data-ttu-id="3e2c4-107">這項效果的 CLSID 是 CLSID \_ D2D1Tint。</span><span class="sxs-lookup"><span data-stu-id="3e2c4-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="3e2c4-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="3e2c4-108">Effect properties</span></span>



| <span data-ttu-id="3e2c4-109">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="3e2c4-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="3e2c4-110">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="3e2c4-110">Type and default value</span></span>                              | <span data-ttu-id="3e2c4-111">Description</span><span class="sxs-lookup"><span data-stu-id="3e2c4-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3e2c4-112">ColorD2D1 \_ 色調 \_ 的 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="3e2c4-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="3e2c4-113">D2D1 \_ VECTOR \_ 4F (1.0 f、1.0 f、1.0 f、1.0 f) </span><span class="sxs-lookup"><span data-stu-id="3e2c4-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="3e2c4-114">來源影像中的色彩會乘以此值。</span><span class="sxs-lookup"><span data-stu-id="3e2c4-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="3e2c4-115">ClampOutputD2D1 \_ 色調 \_ 的 \_ 夾具 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="3e2c4-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="3e2c4-116">BOOLFALSE</span><span class="sxs-lookup"><span data-stu-id="3e2c4-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="3e2c4-117">是否要將輸出值夾具至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="3e2c4-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3e2c4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e2c4-118">Requirements</span></span>



| <span data-ttu-id="3e2c4-119">需求</span><span class="sxs-lookup"><span data-stu-id="3e2c4-119">Requirement</span></span> | <span data-ttu-id="3e2c4-120">值</span><span class="sxs-lookup"><span data-stu-id="3e2c4-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="3e2c4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e2c4-121">Minimum supported client</span></span> | <span data-ttu-id="3e2c4-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e2c4-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3e2c4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e2c4-123">Minimum supported server</span></span> | <span data-ttu-id="3e2c4-124">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e2c4-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3e2c4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3e2c4-125">Header</span></span>                   | <span data-ttu-id="3e2c4-126">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="3e2c4-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="3e2c4-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e2c4-127">Library</span></span>                  | <span data-ttu-id="3e2c4-128">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="3e2c4-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="3e2c4-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e2c4-129">Related topics</span></span>

* [<span data-ttu-id="3e2c4-130">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="3e2c4-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
