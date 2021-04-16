---
description: 值，定義影片畫面中深度值的測量系統。
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: 'MF_MT_DEPTH_MEASUREMENT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563918"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="66894-103">MF \_ MT \_ 深度 \_ 度量屬性</span><span class="sxs-lookup"><span data-stu-id="66894-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="66894-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="66894-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="66894-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="66894-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="66894-106">值，定義影片畫面中深度值的測量系統。</span><span class="sxs-lookup"><span data-stu-id="66894-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="66894-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="66894-107">Data type</span></span>

<span data-ttu-id="66894-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66894-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="66894-109">備註</span><span class="sxs-lookup"><span data-stu-id="66894-109">Remarks</span></span>

<span data-ttu-id="66894-110">這個值是 [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)列舉的成員</span><span class="sxs-lookup"><span data-stu-id="66894-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="66894-111">如果這個屬性不存在，則會假設為 **DistanceToFocalPlane**。</span><span class="sxs-lookup"><span data-stu-id="66894-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="66894-112">在 3D Euclidian 座標系統中，通常會更容易使用焦點平面的距離。</span><span class="sxs-lookup"><span data-stu-id="66894-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![distancetofocalplane 的圖例](images/distance-to-focal-plane.png)

<span data-ttu-id="66894-114">與焦距中心格式的距離通常是來自感應器的原始資料，例如飛行攝影機的時間。</span><span class="sxs-lookup"><span data-stu-id="66894-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![distancetoopticalcenter 的圖例](images/distance-to-optical-center.png)

<span data-ttu-id="66894-116">深度相機無法理解所有圖元的深度。</span><span class="sxs-lookup"><span data-stu-id="66894-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="66894-117">當圖元的信賴度很低時（因為材質、遮蔽或超出範圍等），該圖元的深度值可能會無效。</span><span class="sxs-lookup"><span data-stu-id="66894-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="66894-118">當深度圖元值為0時，圖元就會無效。</span><span class="sxs-lookup"><span data-stu-id="66894-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="66894-119">有些深度相機會附加每個圖元的位元遮罩中繼資料（除了 depth 值），以代表圖元深度不正確原因，因為材質、遮蔽或超出範圍等等。建議您避免將這類中繼資料附加為深度值的位，因為在圖元著色器中使用這類值時，通常會造成困難。</span><span class="sxs-lookup"><span data-stu-id="66894-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="66894-120">相反。</span><span class="sxs-lookup"><span data-stu-id="66894-120">Instead.</span></span> <span data-ttu-id="66894-121">建議您使用具有相同解析度的個別8位映射緩衝區，並將其附加為 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的屬性。</span><span class="sxs-lookup"><span data-stu-id="66894-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="66894-122">這類中繼資料會因每個相機廠商而異，且不會由平臺進行標準化。</span><span class="sxs-lookup"><span data-stu-id="66894-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="66894-123">我們建議使用完整的16個位來取得深度值，以便更輕鬆地處理下游，並使用固定值（例如0）進行失效。</span><span class="sxs-lookup"><span data-stu-id="66894-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="66894-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="66894-124">Requirements</span></span>



| <span data-ttu-id="66894-125">需求</span><span class="sxs-lookup"><span data-stu-id="66894-125">Requirement</span></span> | <span data-ttu-id="66894-126">值</span><span class="sxs-lookup"><span data-stu-id="66894-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66894-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66894-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66894-128">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66894-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="66894-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66894-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66894-130">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66894-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="66894-131">標頭</span><span class="sxs-lookup"><span data-stu-id="66894-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="66894-132"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="66894-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




