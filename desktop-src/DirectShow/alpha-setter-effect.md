---
description: Alpha Setter 效果
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Alpha Setter 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687863"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="96bdb-103">Alpha Setter 效果</span><span class="sxs-lookup"><span data-stu-id="96bdb-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="96bdb-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="96bdb-104">\[Deprecated.</span></span> <span data-ttu-id="96bdb-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="96bdb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96bdb-106">Alpha Setter 效果會設定影片影像上的 Alpha 位。</span><span class="sxs-lookup"><span data-stu-id="96bdb-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="96bdb-107">類別識別碼 (CLSID) ： {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="96bdb-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="96bdb-108">CLSID 變數名稱： CLSID \_ DxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="96bdb-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="96bdb-109">易記名稱： "DxtAlphaSetter"</span><span class="sxs-lookup"><span data-stu-id="96bdb-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="96bdb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96bdb-110">Properties</span></span>



| <span data-ttu-id="96bdb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="96bdb-111">Property</span></span>  | <span data-ttu-id="96bdb-112">類型</span><span class="sxs-lookup"><span data-stu-id="96bdb-112">Type</span></span>   | <span data-ttu-id="96bdb-113">預設</span><span class="sxs-lookup"><span data-stu-id="96bdb-113">Default</span></span> | <span data-ttu-id="96bdb-114">描述</span><span class="sxs-lookup"><span data-stu-id="96bdb-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="96bdb-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="96bdb-115">Alpha</span></span>     | <span data-ttu-id="96bdb-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="96bdb-116">BYTE</span></span>   | <span data-ttu-id="96bdb-117">-1</span><span class="sxs-lookup"><span data-stu-id="96bdb-117">-1</span></span>      | <span data-ttu-id="96bdb-118">設定整個影像的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="96bdb-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="96bdb-119">AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="96bdb-119">AlphaRamp</span></span> | <span data-ttu-id="96bdb-120">double</span><span class="sxs-lookup"><span data-stu-id="96bdb-120">double</span></span> | <span data-ttu-id="96bdb-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="96bdb-121">-1.0</span></span>    | <span data-ttu-id="96bdb-122">將 Alpha 設定為原始 Alpha 值的百分比。</span><span class="sxs-lookup"><span data-stu-id="96bdb-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="96bdb-123">備註</span><span class="sxs-lookup"><span data-stu-id="96bdb-123">Remarks</span></span>

<span data-ttu-id="96bdb-124">會忽略具有負值的屬性。</span><span class="sxs-lookup"><span data-stu-id="96bdb-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="96bdb-125">只有一個屬性可以有非負數值。</span><span class="sxs-lookup"><span data-stu-id="96bdb-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="96bdb-126">Alpha 屬性為影像中的每個圖元指定常數 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="96bdb-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="96bdb-127">這個屬性會覆寫原始影像中的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="96bdb-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="96bdb-128">AlphaRamp 屬性會將每個圖元的 Alpha 值指定為圖元原始值的百分比，從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="96bdb-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96bdb-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="96bdb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96bdb-130">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="96bdb-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



