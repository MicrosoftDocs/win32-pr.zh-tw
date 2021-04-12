---
title: 交叉淡出效果
description: 此效果結合了兩個影像，方法是從輸入影像新增加權圖元。 它有兩個輸入，名為 [目的地] 和 [來源]。
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508543"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="c7481-104">交叉淡出效果</span><span class="sxs-lookup"><span data-stu-id="c7481-104">Cross-fade effect</span></span>

<span data-ttu-id="c7481-105">此效果結合了兩個影像，方法是從輸入影像新增加權圖元。</span><span class="sxs-lookup"><span data-stu-id="c7481-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="c7481-106">它有兩個輸入，名為 [目的地] 和 [來源]。</span><span class="sxs-lookup"><span data-stu-id="c7481-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="c7481-107">交叉淡化公式是 **輸出 = 權數 \* 目的地 + (1 權數) \* 來源**。</span><span class="sxs-lookup"><span data-stu-id="c7481-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="c7481-108">這項效果的 CLSID 是 CLSID \_ D2D1CrossFade。</span><span class="sxs-lookup"><span data-stu-id="c7481-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c7481-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="c7481-109">Effect properties</span></span>

| <span data-ttu-id="c7481-110">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="c7481-110">Display name and index enumeration</span></span>             | <span data-ttu-id="c7481-111">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="c7481-111">Type and default value</span></span> | <span data-ttu-id="c7481-112">Description</span><span class="sxs-lookup"><span data-stu-id="c7481-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7481-113">WeightD2D1 \_ CROSSFADE 的值 \_ \_ 加權</span><span class="sxs-lookup"><span data-stu-id="c7481-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="c7481-114">FLOAT 0.5 f</span><span class="sxs-lookup"><span data-stu-id="c7481-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="c7481-115">要對來源影像的色彩值與目的影像進行權衡的程度。</span><span class="sxs-lookup"><span data-stu-id="c7481-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="c7481-116">最小值為 0.0 f (以獨佔方式使用目的影像來判斷輸出) ，最大值為 1.0 f (以獨佔方式使用來源映射來判斷輸出) 。</span><span class="sxs-lookup"><span data-stu-id="c7481-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c7481-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7481-117">Requirements</span></span>



| <span data-ttu-id="c7481-118">需求</span><span class="sxs-lookup"><span data-stu-id="c7481-118">Requirement</span></span> | <span data-ttu-id="c7481-119">值</span><span class="sxs-lookup"><span data-stu-id="c7481-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c7481-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7481-120">Minimum supported client</span></span> | <span data-ttu-id="c7481-121">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7481-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c7481-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7481-122">Minimum supported server</span></span> | <span data-ttu-id="c7481-123">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7481-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c7481-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c7481-124">Header</span></span>                   | <span data-ttu-id="c7481-125">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="c7481-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c7481-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7481-126">Library</span></span>                  | <span data-ttu-id="c7481-127">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="c7481-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="c7481-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7481-128">Related topics</span></span>

* [<span data-ttu-id="c7481-129">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="c7481-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
