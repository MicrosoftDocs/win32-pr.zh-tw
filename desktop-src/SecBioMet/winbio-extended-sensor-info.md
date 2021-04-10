---
title: 'WINBIO_EXTENDED_SENSOR_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_SENSOR_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934022"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="34604-105">WINBIO \_ 擴充的 \_ 感應器 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="34604-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="34604-106">包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="34604-107">語法</span><span class="sxs-lookup"><span data-stu-id="34604-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="34604-108">成員</span><span class="sxs-lookup"><span data-stu-id="34604-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="34604-109">**GenericSensorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="34604-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="34604-110">連接到特定生物識別單位之感應器元件的一般功能。</span><span class="sxs-lookup"><span data-stu-id="34604-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="34604-111">**因素**</span><span class="sxs-lookup"><span data-stu-id="34604-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="34604-112">此結構包含感應器介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。</span><span class="sxs-lookup"><span data-stu-id="34604-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="34604-113">例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**， **WINBIO \_ 擴充 \_ 感應器 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="34604-114">**特定**</span><span class="sxs-lookup"><span data-stu-id="34604-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="34604-115">與特定生物特徵辨識因素相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="34604-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="34604-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="34604-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="34604-117">Reserved.</span></span> <span data-ttu-id="34604-118">必須為零。</span><span class="sxs-lookup"><span data-stu-id="34604-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="34604-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="34604-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="34604-120">與臉部特徵相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="34604-121">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="34604-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="34604-122">攝影機框架的大小，以圖元為 **單位的長度\*\*\*\*和寬度**（以圖元為單位）。 [](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34604-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="34604-123">點 (0，0) 代表框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="34604-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="34604-124">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="34604-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="34604-125">攝影機的相機框架距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="34604-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="34604-126">值為 (0，0) 表示臉部和攝影機的相機框架完全重迭。</span><span class="sxs-lookup"><span data-stu-id="34604-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="34604-127">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="34604-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="34604-128">相機的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="34604-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34604-129">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="34604-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="34604-130">與指紋模式相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="34604-131">**已保留**</span><span class="sxs-lookup"><span data-stu-id="34604-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="34604-132">保留的。</span><span class="sxs-lookup"><span data-stu-id="34604-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34604-133">**虹膜**</span><span class="sxs-lookup"><span data-stu-id="34604-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="34604-134">與鳶尾花模式相關的生物特徵辨識單位之感應器介面卡功能和註冊需求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="34604-135">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="34604-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="34604-136">攝影機框架的大小，以圖元為 **單位的長度\*\*\*\*和寬度**（以圖元為單位）。 [](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34604-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="34604-137">點 (0，0) 代表框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="34604-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="34604-138">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="34604-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="34604-139">鳶尾花攝影機框架的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="34604-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="34604-140">值為 (0，0) 表示鳶尾花和攝影機的相機框架完全重迭。</span><span class="sxs-lookup"><span data-stu-id="34604-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="34604-141">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="34604-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="34604-142">相機的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="34604-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34604-143">**語音**</span><span class="sxs-lookup"><span data-stu-id="34604-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="34604-144">與語音模式相關之生物特徵辨識單位的感應器介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34604-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="34604-145">**已保留**</span><span class="sxs-lookup"><span data-stu-id="34604-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="34604-146">保留的。</span><span class="sxs-lookup"><span data-stu-id="34604-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34604-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="34604-147">Requirements</span></span>



| <span data-ttu-id="34604-148">需求</span><span class="sxs-lookup"><span data-stu-id="34604-148">Requirement</span></span> | <span data-ttu-id="34604-149">值</span><span class="sxs-lookup"><span data-stu-id="34604-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34604-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34604-150">Minimum supported client</span></span><br/> | <span data-ttu-id="34604-151">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34604-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="34604-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34604-152">Minimum supported server</span></span><br/> | <span data-ttu-id="34604-153">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34604-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="34604-154">標頭</span><span class="sxs-lookup"><span data-stu-id="34604-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="34604-155"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="34604-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34604-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34604-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34604-157">**WINBIO \_ 功能常數**</span><span class="sxs-lookup"><span data-stu-id="34604-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="34604-158">**WINBIO \_ 生物特徵辨識 \_ 類型常數**</span><span class="sxs-lookup"><span data-stu-id="34604-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="34604-159">**WINBIO \_ 方向常數**</span><span class="sxs-lookup"><span data-stu-id="34604-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

