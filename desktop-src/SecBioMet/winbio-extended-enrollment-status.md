---
title: 'WINBIO_EXTENDED_ENROLLMENT_STATUS 結構 (Winbio \_ 類型 .h) '
description: 包含正在進行中之註冊狀態的其他相關資訊。
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENROLLMENT_STATUS 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094063"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="70539-105">WINBIO \_ 延伸 \_ 註冊 \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="70539-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="70539-106">包含正在進行中之註冊狀態的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="70539-107">語法</span><span class="sxs-lookup"><span data-stu-id="70539-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="70539-108">成員</span><span class="sxs-lookup"><span data-stu-id="70539-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70539-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="70539-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="70539-110">註冊範本的範例集合狀態。</span><span class="sxs-lookup"><span data-stu-id="70539-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="70539-111">此成員可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="70539-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="70539-112">值</span><span class="sxs-lookup"><span data-stu-id="70539-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="70539-113">意義</span><span class="sxs-lookup"><span data-stu-id="70539-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="70539-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="70539-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="70539-115">註冊可供儲存。</span><span class="sxs-lookup"><span data-stu-id="70539-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="70539-116"><dt>**WINBIO \_ E \_ 不正確作業 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70539-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="70539-117">沒有任何註冊正在進行中。</span><span class="sxs-lookup"><span data-stu-id="70539-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="70539-118"><dt>**WINBIO \_ 我 \_ 更多 \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="70539-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="70539-119">需要更多範例才能完成範本。</span><span class="sxs-lookup"><span data-stu-id="70539-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="70539-120"><dt>**WINBIO \_ 電子 \_ 錯誤 \_ 捕捉**</dt></span><span class="sxs-lookup"><span data-stu-id="70539-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="70539-121">無法使用最新的範例。</span><span class="sxs-lookup"><span data-stu-id="70539-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="70539-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="70539-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="70539-123">如果 **templatestatus.archived** 成員的值是 **WINBIO \_ E \_ 錯誤的 \_ 捕獲**，則為最新範例無法使用的原因。</span><span class="sxs-lookup"><span data-stu-id="70539-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="70539-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="70539-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="70539-125">從引擎介面卡取得完成範本百分比的最佳估計值，以0到100的值表示。</span><span class="sxs-lookup"><span data-stu-id="70539-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="70539-126">**因素**</span><span class="sxs-lookup"><span data-stu-id="70539-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="70539-127">此結構包含引擎介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。</span><span class="sxs-lookup"><span data-stu-id="70539-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="70539-128">例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**，則 [**WINBIO \_ 擴充 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md) 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="70539-129">**SubFactor**</span><span class="sxs-lookup"><span data-stu-id="70539-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="70539-130">**WINBIO \_ 生物識別 \_ 子類型** 值，提供註冊的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="70539-131">**特定**</span><span class="sxs-lookup"><span data-stu-id="70539-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="70539-132">針對特定生物特徵辨識因素進行中之註冊的狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="70539-133">**Null**</span><span class="sxs-lookup"><span data-stu-id="70539-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="70539-134">保留的。</span><span class="sxs-lookup"><span data-stu-id="70539-134">Reserved.</span></span> <span data-ttu-id="70539-135">必須為零。</span><span class="sxs-lookup"><span data-stu-id="70539-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="70539-136">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="70539-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="70539-137">臉部特徵進行中之註冊狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="70539-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="70539-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="70539-139">要註冊之個人臉部的相機框架內的位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="70539-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="70539-140">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="70539-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="70539-141">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="70539-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="70539-142">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="70539-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="70539-143">**距離**</span><span class="sxs-lookup"><span data-stu-id="70539-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="70539-144">臉部的實際位置與臉部的理想焦距之間的距離。</span><span class="sxs-lookup"><span data-stu-id="70539-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="70539-145">此值範圍從-100 到100。</span><span class="sxs-lookup"><span data-stu-id="70539-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="70539-146">0表示理想的距離，正值表示臉部的實際位置太遠，負值表示實際位置太近。</span><span class="sxs-lookup"><span data-stu-id="70539-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="70539-147">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="70539-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="70539-148">針對指紋模式進行中之註冊狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="70539-149">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="70539-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="70539-150">建立新指紋範本所需的樣本總數。</span><span class="sxs-lookup"><span data-stu-id="70539-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="70539-151">**中心**</span><span class="sxs-lookup"><span data-stu-id="70539-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="70539-152">建立新的指紋範本時所需的指紋中心樣本數。</span><span class="sxs-lookup"><span data-stu-id="70539-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="70539-153">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="70539-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="70539-154">建立新的指紋範本所需之指紋上邊緣的樣本數。</span><span class="sxs-lookup"><span data-stu-id="70539-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="70539-155">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="70539-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="70539-156">建立新的指紋範本所需之指紋下邊緣的樣本數。</span><span class="sxs-lookup"><span data-stu-id="70539-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="70539-157">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="70539-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="70539-158">建立新的指紋範本所需之指紋左邊緣的樣本數。</span><span class="sxs-lookup"><span data-stu-id="70539-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="70539-159">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="70539-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="70539-160">建立新的指紋範本時所需的指紋右邊的樣本數。</span><span class="sxs-lookup"><span data-stu-id="70539-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="70539-161">**虹膜**</span><span class="sxs-lookup"><span data-stu-id="70539-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="70539-162">鳶尾花模式進行中之註冊狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="70539-163">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="70539-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="70539-164">要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="70539-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="70539-165">如果鳶尾花辨識系統只監視一眼，這個位置就是該眼睛的鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="70539-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="70539-166">如果鳶尾花辨識系統同時監視這兩眼，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="70539-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="70539-167">如果鳶尾花辨識系統同時監視這兩個眼睛，而兩個眼睛都在攝影機框架中，則這個位置可能是個人的正確眼睛鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="70539-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="70539-168">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="70539-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="70539-169">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="70539-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="70539-170">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="70539-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="70539-171">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="70539-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="70539-172">要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="70539-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="70539-173">如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。</span><span class="sxs-lookup"><span data-stu-id="70539-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="70539-174">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的最左邊鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="70539-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="70539-175">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="70539-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="70539-176">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="70539-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="70539-177">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="70539-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="70539-178">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="70539-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="70539-179">要註冊之個人的其中一個瞳孔中心位置。</span><span class="sxs-lookup"><span data-stu-id="70539-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="70539-180">如果鳶尾花辨識系統只監控一眼，這個位置就是該眼睛小學生的中心。</span><span class="sxs-lookup"><span data-stu-id="70539-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="70539-181">如果鳶尾花辨識系統同時監視這兩種情況，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛小學生中心。</span><span class="sxs-lookup"><span data-stu-id="70539-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="70539-182">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的適當眼睛小學生中心。</span><span class="sxs-lookup"><span data-stu-id="70539-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="70539-183">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="70539-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="70539-184">要註冊之個人的其中一個瞳孔中心位置。</span><span class="sxs-lookup"><span data-stu-id="70539-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="70539-185">如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。</span><span class="sxs-lookup"><span data-stu-id="70539-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="70539-186">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人左側的小學生中心。</span><span class="sxs-lookup"><span data-stu-id="70539-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="70539-187">**距離**</span><span class="sxs-lookup"><span data-stu-id="70539-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="70539-188">鳶尾花的實際位置與鳶尾花的理想焦距距離之間的距離。</span><span class="sxs-lookup"><span data-stu-id="70539-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="70539-189">此值範圍從-100 到100。</span><span class="sxs-lookup"><span data-stu-id="70539-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="70539-190">0表示理想的距離，正值表示鳶尾花的實際位置太遠，負值則表示實際位置太近。</span><span class="sxs-lookup"><span data-stu-id="70539-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="70539-191">**語音**</span><span class="sxs-lookup"><span data-stu-id="70539-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="70539-192">語音模式進行中的註冊狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70539-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="70539-193">**已保留**</span><span class="sxs-lookup"><span data-stu-id="70539-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="70539-194">保留的。</span><span class="sxs-lookup"><span data-stu-id="70539-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70539-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="70539-195">Requirements</span></span>



| <span data-ttu-id="70539-196">需求</span><span class="sxs-lookup"><span data-stu-id="70539-196">Requirement</span></span> | <span data-ttu-id="70539-197">值</span><span class="sxs-lookup"><span data-stu-id="70539-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70539-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70539-198">Minimum supported client</span></span><br/> | <span data-ttu-id="70539-199">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70539-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="70539-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70539-200">Minimum supported server</span></span><br/> | <span data-ttu-id="70539-201">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70539-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="70539-202">標頭</span><span class="sxs-lookup"><span data-stu-id="70539-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="70539-203"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="70539-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





