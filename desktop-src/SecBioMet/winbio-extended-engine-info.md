---
title: 'WINBIO_EXTENDED_ENGINE_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENGINE_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844319"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="67944-105">WINBIO \_ 延伸 \_ 引擎 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="67944-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="67944-106">包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="67944-107">語法</span><span class="sxs-lookup"><span data-stu-id="67944-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="67944-108">成員</span><span class="sxs-lookup"><span data-stu-id="67944-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="67944-109">**GenericEngineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="67944-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="67944-110">連接到特定生物識別單位之引擎元件的一般功能。</span><span class="sxs-lookup"><span data-stu-id="67944-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="67944-111">**因素**</span><span class="sxs-lookup"><span data-stu-id="67944-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="67944-112">此結構包含引擎介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。</span><span class="sxs-lookup"><span data-stu-id="67944-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="67944-113">例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**，則 **WINBIO \_ 擴充 \_ 引擎 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="67944-114">**特定**</span><span class="sxs-lookup"><span data-stu-id="67944-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="67944-115">與特定生物特徵辨識因素相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="67944-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="67944-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="67944-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-117">Reserved.</span></span> <span data-ttu-id="67944-118">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67944-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="67944-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="67944-120">與臉部特徵相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="67944-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="67944-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="67944-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-122">Reserved.</span></span> <span data-ttu-id="67944-123">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67944-124">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="67944-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67944-125">**Null**</span><span class="sxs-lookup"><span data-stu-id="67944-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="67944-126">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-126">Reserved.</span></span> <span data-ttu-id="67944-127">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="67944-128">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="67944-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="67944-129">與指紋模式相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="67944-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="67944-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="67944-131">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-131">Reserved.</span></span> <span data-ttu-id="67944-132">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67944-133">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="67944-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="67944-134">建立新指紋範本所需的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="67944-135">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="67944-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="67944-136">建立新指紋範本所需的良好樣本總數。</span><span class="sxs-lookup"><span data-stu-id="67944-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="67944-137">**中心**</span><span class="sxs-lookup"><span data-stu-id="67944-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="67944-138">建立新的指紋範本所需之指紋中心的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="67944-139">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="67944-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="67944-140">建立新的指紋範本所需之指紋上邊緣的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="67944-141">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="67944-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="67944-142">建立新的指紋範本所需之指紋下邊緣的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="67944-143">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="67944-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="67944-144">建立新的指紋範本所需之指紋左邊緣的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="67944-145">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="67944-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="67944-146">建立新的指紋範本時所需的指紋右邊緣的良好樣本數。</span><span class="sxs-lookup"><span data-stu-id="67944-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="67944-147">**虹膜**</span><span class="sxs-lookup"><span data-stu-id="67944-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="67944-148">與鳶尾花模式相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="67944-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="67944-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="67944-150">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-150">Reserved.</span></span> <span data-ttu-id="67944-151">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67944-152">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="67944-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67944-153">**Null**</span><span class="sxs-lookup"><span data-stu-id="67944-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="67944-154">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-154">Reserved.</span></span> <span data-ttu-id="67944-155">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="67944-156">**語音**</span><span class="sxs-lookup"><span data-stu-id="67944-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="67944-157">與語音模式相關的生物特徵辨識單位之引擎介面卡功能和註冊需求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67944-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="67944-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="67944-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="67944-159">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-159">Reserved.</span></span> <span data-ttu-id="67944-160">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67944-161">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="67944-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67944-162">**Null**</span><span class="sxs-lookup"><span data-stu-id="67944-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="67944-163">保留的。</span><span class="sxs-lookup"><span data-stu-id="67944-163">Reserved.</span></span> <span data-ttu-id="67944-164">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67944-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67944-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="67944-165">Requirements</span></span>



| <span data-ttu-id="67944-166">需求</span><span class="sxs-lookup"><span data-stu-id="67944-166">Requirement</span></span> | <span data-ttu-id="67944-167">值</span><span class="sxs-lookup"><span data-stu-id="67944-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67944-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67944-168">Minimum supported client</span></span><br/> | <span data-ttu-id="67944-169">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67944-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="67944-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67944-170">Minimum supported server</span></span><br/> | <span data-ttu-id="67944-171">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67944-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="67944-172">標頭</span><span class="sxs-lookup"><span data-stu-id="67944-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="67944-173"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="67944-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67944-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67944-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67944-175">**WINBIO \_ 功能常數**</span><span class="sxs-lookup"><span data-stu-id="67944-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="67944-176">**WINBIO \_ 生物特徵辨識 \_ 類型常數**</span><span class="sxs-lookup"><span data-stu-id="67944-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





