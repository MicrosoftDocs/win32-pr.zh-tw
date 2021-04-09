---
title: 'WINBIO_EXTENDED_STORAGE_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_STORAGE_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934021"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="d2683-105">WINBIO \_ 延伸 \_ 儲存體 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="d2683-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="d2683-106">包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2683-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2683-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="d2683-108">成員</span><span class="sxs-lookup"><span data-stu-id="d2683-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2683-109">**GenericStorageCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2683-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-110">連接到特定生物識別單位之儲存體元件的一般功能。</span><span class="sxs-lookup"><span data-stu-id="d2683-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="d2683-111">**因素**</span><span class="sxs-lookup"><span data-stu-id="d2683-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-112">此結構包含存放裝置介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。</span><span class="sxs-lookup"><span data-stu-id="d2683-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="d2683-113">例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**， **WINBIO \_ 延伸 \_ 儲存體 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d2683-114">**特定**</span><span class="sxs-lookup"><span data-stu-id="d2683-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-115">與特定生物特徵辨識因素相關之生物特徵辨識設備的存放裝置介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="d2683-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="d2683-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="d2683-117">Reserved.</span></span> <span data-ttu-id="d2683-118">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d2683-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2683-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="d2683-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-120">與臉部特徵相關的生物特徵辨識設備之存放裝置介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="d2683-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2683-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-122">連接到特定生物特徵辨識裝置的儲存元件臉部辨識功能。</span><span class="sxs-lookup"><span data-stu-id="d2683-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2683-123">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="d2683-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-124">與指紋模式相關之生物特徵辨識設備的儲存介面卡功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d2683-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2683-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-126">連線到特定生物識別單位之儲存體元件的指紋辨識功能</span><span class="sxs-lookup"><span data-stu-id="d2683-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2683-127">**虹膜**</span><span class="sxs-lookup"><span data-stu-id="d2683-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-128">與鳶尾花模式相關的生物特徵辨識單位之儲存體介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d2683-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2683-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-130">連線到特定生物識別單位之儲存體元件的鳶尾花辨識功能</span><span class="sxs-lookup"><span data-stu-id="d2683-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2683-131">**語音**</span><span class="sxs-lookup"><span data-stu-id="d2683-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-132">與語音模式相關的生物特徵辨識單位之存放裝置介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2683-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d2683-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2683-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d2683-134">連線到特定生物識別單位之儲存體元件的語音辨識功能</span><span class="sxs-lookup"><span data-stu-id="d2683-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2683-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2683-135">Requirements</span></span>



| <span data-ttu-id="d2683-136">需求</span><span class="sxs-lookup"><span data-stu-id="d2683-136">Requirement</span></span> | <span data-ttu-id="d2683-137">值</span><span class="sxs-lookup"><span data-stu-id="d2683-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2683-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2683-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d2683-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2683-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d2683-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2683-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d2683-141">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2683-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="d2683-142">標頭</span><span class="sxs-lookup"><span data-stu-id="d2683-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2683-143"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="d2683-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2683-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2683-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2683-145">**WINBIO \_ 生物特徵辨識 \_ 類型常數**</span><span class="sxs-lookup"><span data-stu-id="d2683-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="d2683-146">**WINBIO \_ 功能常數**</span><span class="sxs-lookup"><span data-stu-id="d2683-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





