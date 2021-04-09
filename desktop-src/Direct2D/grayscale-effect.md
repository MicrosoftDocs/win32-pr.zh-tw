---
title: 灰階效果
description: 將影像轉換為灰色。
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686025"
---
# <a name="grayscale-effect"></a><span data-ttu-id="2eb02-103">灰階效果</span><span class="sxs-lookup"><span data-stu-id="2eb02-103">Grayscale effect</span></span>

<span data-ttu-id="2eb02-104">將影像轉換為灰色。</span><span class="sxs-lookup"><span data-stu-id="2eb02-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="2eb02-105">灰階使用下列矩陣，將色彩矩陣效果轉換成灰階：</span><span class="sxs-lookup"><span data-stu-id="2eb02-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![轉換矩陣](images/grayscale-effect-matrix.png)

<span data-ttu-id="2eb02-107">這項效果的 CLSID 是 CLSID \_ D2D1Grayscale。</span><span class="sxs-lookup"><span data-stu-id="2eb02-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="2eb02-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="2eb02-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="2eb02-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="2eb02-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="2eb02-110">需求</span><span class="sxs-lookup"><span data-stu-id="2eb02-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2eb02-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="2eb02-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2eb02-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="2eb02-112">Example image</span></span>

![效果輸出的範例](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="2eb02-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="2eb02-114">Effect properties</span></span>

<span data-ttu-id="2eb02-115">此效果沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="2eb02-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb02-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eb02-116">Requirements</span></span>



| <span data-ttu-id="2eb02-117">需求</span><span class="sxs-lookup"><span data-stu-id="2eb02-117">Requirement</span></span> | <span data-ttu-id="2eb02-118">值</span><span class="sxs-lookup"><span data-stu-id="2eb02-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="2eb02-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eb02-119">Minimum supported client</span></span> | <span data-ttu-id="2eb02-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb02-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2eb02-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eb02-121">Minimum supported server</span></span> | <span data-ttu-id="2eb02-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb02-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2eb02-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2eb02-123">Header</span></span>                   | <span data-ttu-id="2eb02-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="2eb02-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="2eb02-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="2eb02-125">Library</span></span>                  | <span data-ttu-id="2eb02-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="2eb02-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="2eb02-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="2eb02-127">Related topics</span></span>

* [<span data-ttu-id="2eb02-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="2eb02-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
