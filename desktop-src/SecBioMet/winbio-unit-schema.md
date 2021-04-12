---
title: 'WINBIO_UNIT_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識設備的功能。
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_UNIT_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935063"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="d09da-105">WINBIO \_ 單元 \_ 架構結構</span><span class="sxs-lookup"><span data-stu-id="d09da-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="d09da-106">**WINBIO \_ 單元 \_ 架構** 結構描述生物特徵辨識設備的功能。</span><span class="sxs-lookup"><span data-stu-id="d09da-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="d09da-107">[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)函式會使用它。</span><span class="sxs-lookup"><span data-stu-id="d09da-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09da-108">語法</span><span class="sxs-lookup"><span data-stu-id="d09da-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="d09da-109">成員</span><span class="sxs-lookup"><span data-stu-id="d09da-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d09da-110">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="d09da-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-111">識別生物特徵辨識單位的值。</span><span class="sxs-lookup"><span data-stu-id="d09da-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-112">**PoolType**</span><span class="sxs-lookup"><span data-stu-id="d09da-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-113">指定生物特徵辨識單位類型的 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="d09da-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="d09da-114">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d09da-114">This can be one of the following values:</span></span>



| <span data-ttu-id="d09da-115">值</span><span class="sxs-lookup"><span data-stu-id="d09da-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="d09da-116">意義</span><span class="sxs-lookup"><span data-stu-id="d09da-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="d09da-117"><dt>**WINBIO \_ 集區 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="d09da-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="d09da-118">未知的類型。</span><span class="sxs-lookup"><span data-stu-id="d09da-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="d09da-119"><dt>**WINBIO \_ 集區 \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="d09da-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="d09da-120">會話會連接到服務提供者所管理的生物識別單位共用集合。</span><span class="sxs-lookup"><span data-stu-id="d09da-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="d09da-121"><dt>**WINBIO \_ 集區 \_ 私用**</dt></span><span class="sxs-lookup"><span data-stu-id="d09da-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="d09da-122">會話會連接到由呼叫端管理的生物特徵辨識單位集合。</span><span class="sxs-lookup"><span data-stu-id="d09da-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="d09da-123">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="d09da-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-124">指定生物特徵辨識單位類型的值。</span><span class="sxs-lookup"><span data-stu-id="d09da-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="d09da-125">目前只支援 **WINBIO \_ 類型 \_ 指紋** 。</span><span class="sxs-lookup"><span data-stu-id="d09da-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-126">**SensorSubType**</span><span class="sxs-lookup"><span data-stu-id="d09da-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-127">針對 **BiometricFactor** 成員所指定的生物特徵辨識類型定義的感應器子類型。</span><span class="sxs-lookup"><span data-stu-id="d09da-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="d09da-128">目前只支援 (**WINBIO \_ 類型 \_ 指紋**) 的指紋類型。</span><span class="sxs-lookup"><span data-stu-id="d09da-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="d09da-129">下列子類型目前為指紋定義：</span><span class="sxs-lookup"><span data-stu-id="d09da-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="d09da-130">WINBIO \_ 感應器 \_ 子類型 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="d09da-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="d09da-131">WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 滑動</span><span class="sxs-lookup"><span data-stu-id="d09da-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="d09da-132">WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 觸控</span><span class="sxs-lookup"><span data-stu-id="d09da-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="d09da-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d09da-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-134">生物識別感應器功能的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="d09da-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="d09da-135">這可以是下列值的位 **or** ：</span><span class="sxs-lookup"><span data-stu-id="d09da-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="d09da-136">WINBIO \_ 功能 \_ 感應器</span><span class="sxs-lookup"><span data-stu-id="d09da-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="d09da-137">WINBIO \_ 功能比對 \_</span><span class="sxs-lookup"><span data-stu-id="d09da-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="d09da-138">WINBIO \_ 功能 \_ 資料庫</span><span class="sxs-lookup"><span data-stu-id="d09da-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="d09da-139">WINBIO \_ 功能 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="d09da-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="d09da-140">WINBIO \_ 功能 \_ 加密</span><span class="sxs-lookup"><span data-stu-id="d09da-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="d09da-141">WINBIO \_ 功能 \_ 導覽</span><span class="sxs-lookup"><span data-stu-id="d09da-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="d09da-142">WINBIO \_ 功能 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="d09da-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="d09da-143">WINBIO \_ 功能 \_ 虛擬 \_ 感應器</span><span class="sxs-lookup"><span data-stu-id="d09da-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="d09da-144">**WINBIO \_ 功能 \_ 虛擬 \_ 感應器** 常數只適用于 Windows 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="d09da-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="d09da-145">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="d09da-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-146">包含裝置識別碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="d09da-146">A string value that contains the device ID.</span></span> <span data-ttu-id="d09da-147">字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="d09da-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-148">**說明**</span><span class="sxs-lookup"><span data-stu-id="d09da-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-149">包含生物特徵辨識單位描述的字串值。</span><span class="sxs-lookup"><span data-stu-id="d09da-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="d09da-150">字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="d09da-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-151">**製造商**</span><span class="sxs-lookup"><span data-stu-id="d09da-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-152">包含製造商名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="d09da-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="d09da-153">字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="d09da-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-154">**型號**</span><span class="sxs-lookup"><span data-stu-id="d09da-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-155">字串值，包含生物特徵辨識單位的模型編號。</span><span class="sxs-lookup"><span data-stu-id="d09da-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="d09da-156">字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="d09da-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d09da-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-158">以 **Null** 終止的 Unicode 字串，其中包含生物特徵辨識單位的序號。</span><span class="sxs-lookup"><span data-stu-id="d09da-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="d09da-159">字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="d09da-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="d09da-160">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="d09da-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d09da-161">[**WINBIO \_ 版本**](winbio-version.md)結構，其中包含生物識別單位的主要和次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d09da-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d09da-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="d09da-162">Requirements</span></span>



| <span data-ttu-id="d09da-163">需求</span><span class="sxs-lookup"><span data-stu-id="d09da-163">Requirement</span></span> | <span data-ttu-id="d09da-164">值</span><span class="sxs-lookup"><span data-stu-id="d09da-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09da-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d09da-165">Minimum supported client</span></span><br/> | <span data-ttu-id="d09da-166">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d09da-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d09da-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d09da-167">Minimum supported server</span></span><br/> | <span data-ttu-id="d09da-168">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d09da-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d09da-169">標頭</span><span class="sxs-lookup"><span data-stu-id="d09da-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="d09da-170"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d09da-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09da-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d09da-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09da-172">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="d09da-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="d09da-173">**WinBioEnumBiometricUnits**</span><span class="sxs-lookup"><span data-stu-id="d09da-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





