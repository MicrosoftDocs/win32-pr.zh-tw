---
description: 值，定義影片框架中深度值的單位。
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: 'MF_MT_DEPTH_VALUE_UNIT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969267"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="e8933-103">MF \_ MT \_ 深度 \_ 值 \_ 單位屬性</span><span class="sxs-lookup"><span data-stu-id="e8933-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="e8933-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e8933-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8933-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e8933-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8933-106">值，定義影片框架中深度值的單位。</span><span class="sxs-lookup"><span data-stu-id="e8933-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8933-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e8933-107">Data type</span></span>

<span data-ttu-id="e8933-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e8933-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="e8933-109">備註</span><span class="sxs-lookup"><span data-stu-id="e8933-109">Remarks</span></span>

<span data-ttu-id="e8933-110">Unit 值是 nanometers 中的 UINT64 值（以 1e-9 計量範圍為單位）。</span><span class="sxs-lookup"><span data-stu-id="e8933-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="e8933-111">如果此值不存在，則單位的預設值為 1e-3，這表示每個圖元層級會以1毫米的實體空間來測量。</span><span class="sxs-lookup"><span data-stu-id="e8933-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="e8933-112">深度相機無法理解所有圖元的深度。</span><span class="sxs-lookup"><span data-stu-id="e8933-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="e8933-113">當圖元的信賴度很低時（因為材質、遮蔽或超出範圍等），該圖元的深度值可能會無效。</span><span class="sxs-lookup"><span data-stu-id="e8933-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="e8933-114">當深度圖元值為0時，圖元就會無效。</span><span class="sxs-lookup"><span data-stu-id="e8933-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="e8933-115">有些深度相機會附加每個圖元的位元遮罩中繼資料（除了 depth 值），以代表圖元深度不正確原因，因為材質、遮蔽或超出範圍等等。建議您避免將這類中繼資料附加為深度值的位，因為在圖元著色器中使用這類值時，通常會造成困難。</span><span class="sxs-lookup"><span data-stu-id="e8933-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="e8933-116">相反。</span><span class="sxs-lookup"><span data-stu-id="e8933-116">Instead.</span></span> <span data-ttu-id="e8933-117">建議您使用具有相同解析度的個別8位映射緩衝區，並將其附加為 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8933-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="e8933-118">這類中繼資料會因每個相機廠商而異，且不會由平臺進行標準化。</span><span class="sxs-lookup"><span data-stu-id="e8933-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="e8933-119">我們建議使用完整的16個位來取得深度值，以便更輕鬆地處理下游，並使用固定值（例如0）進行失效。</span><span class="sxs-lookup"><span data-stu-id="e8933-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8933-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8933-120">Requirements</span></span>



| <span data-ttu-id="e8933-121">需求</span><span class="sxs-lookup"><span data-stu-id="e8933-121">Requirement</span></span> | <span data-ttu-id="e8933-122">值</span><span class="sxs-lookup"><span data-stu-id="e8933-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8933-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8933-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e8933-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8933-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8933-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8933-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e8933-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8933-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="e8933-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e8933-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8933-128"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8933-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




