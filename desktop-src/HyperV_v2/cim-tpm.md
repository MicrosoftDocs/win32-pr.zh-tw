---
description: 描述 (TPM) 裝置的信賴平臺模組。
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: CIM_TPM 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026562"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="416bb-103">CIM \_ TPM 類別</span><span class="sxs-lookup"><span data-stu-id="416bb-103">CIM\_TPM class</span></span>

<span data-ttu-id="416bb-104">描述 (TPM) 裝置的信賴平臺模組。</span><span class="sxs-lookup"><span data-stu-id="416bb-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="416bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="416bb-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="416bb-106">成員</span><span class="sxs-lookup"><span data-stu-id="416bb-106">Members</span></span>

<span data-ttu-id="416bb-107">**CIM \_ TPM** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="416bb-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="416bb-108">方法</span><span class="sxs-lookup"><span data-stu-id="416bb-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="416bb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="416bb-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="416bb-110">方法</span><span class="sxs-lookup"><span data-stu-id="416bb-110">Methods</span></span>

<span data-ttu-id="416bb-111">**CIM \_ TPM** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="416bb-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="416bb-112">方法</span><span class="sxs-lookup"><span data-stu-id="416bb-112">Method</span></span>                                                         | <span data-ttu-id="416bb-113">描述</span><span class="sxs-lookup"><span data-stu-id="416bb-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="416bb-114">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="416bb-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="416bb-115">變更 TPM 裝置的擁有者授權認證。</span><span class="sxs-lookup"><span data-stu-id="416bb-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="416bb-116">**RequestTPMStateChange**</span><span class="sxs-lookup"><span data-stu-id="416bb-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="416bb-117">要求將 TPM 的狀態變更為 **RequestedTPMState** 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="416bb-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="416bb-118">屬性</span><span class="sxs-lookup"><span data-stu-id="416bb-118">Properties</span></span>

<span data-ttu-id="416bb-119">**CIM \_ TPM** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="416bb-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="416bb-120">**AvailableRequestedTPMStates**</span><span class="sxs-lookup"><span data-stu-id="416bb-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="416bb-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416bb-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-123">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ TPM**」。**RequestTPMStateChange**，CIM \_ TPMCapabilities. RequestedTPMStatesSupported ") </span><span class="sxs-lookup"><span data-stu-id="416bb-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-124">[**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md)方法之 *RequestedTPMState* 參數的可能值。</span><span class="sxs-lookup"><span data-stu-id="416bb-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="416bb-125">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="416bb-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-126">**已啟用 S1-Active-擁有的** (2) </span><span class="sxs-lookup"><span data-stu-id="416bb-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-127">**S2 已停用-Active-擁有的** (3) </span><span class="sxs-lookup"><span data-stu-id="416bb-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-128">**已啟用 S3-非使用中-擁有的** (4) </span><span class="sxs-lookup"><span data-stu-id="416bb-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-129">**已停用 S4-非使用中-擁有的** (5) </span><span class="sxs-lookup"><span data-stu-id="416bb-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-130">**已啟用 S5-主動-** 無人擁有的 (6) </span><span class="sxs-lookup"><span data-stu-id="416bb-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-131">**S6 已停用-主動-** 無人 (7) </span><span class="sxs-lookup"><span data-stu-id="416bb-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-132">**S7 已啟用-非** 使用中-無人擁有的 (8) </span><span class="sxs-lookup"><span data-stu-id="416bb-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-133">**S8 已停用-非** 使用中-無人擁有的 (9) </span><span class="sxs-lookup"><span data-stu-id="416bb-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="416bb-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="416bb-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="416bb-135">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="416bb-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="416bb-136">**TPMManafucturerMajorRevision**</span><span class="sxs-lookup"><span data-stu-id="416bb-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="416bb-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v1dot2 \| Section 5.3 \| version \| revMajor ") </span><span class="sxs-lookup"><span data-stu-id="416bb-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-140">TPM 的製造商主要修訂。</span><span class="sxs-lookup"><span data-stu-id="416bb-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-141">**TPMManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="416bb-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="416bb-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 區段 \| 21.6 \_ TPM CAP \_ 版本 \_ 資訊 \| tpmVendorID ") </span><span class="sxs-lookup"><span data-stu-id="416bb-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-145">TPM 製造商識別碼。</span><span class="sxs-lookup"><span data-stu-id="416bb-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-146">**TPMManufacturerInfo**</span><span class="sxs-lookup"><span data-stu-id="416bb-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="416bb-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-149">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v 1.2. a \| r 區段 21.6 \| TPM \_ CAP \_ VERSION \_ INFO \| vendorSpecific ") </span><span class="sxs-lookup"><span data-stu-id="416bb-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-150">TPM 製造商所定義的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="416bb-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-151">**TPMManufacturerMinorRevision**</span><span class="sxs-lookup"><span data-stu-id="416bb-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="416bb-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-154">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v1dot2 \| Section 5.3 \| version \| revMinor ") </span><span class="sxs-lookup"><span data-stu-id="416bb-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-155">TPM 的製造商次要修訂。</span><span class="sxs-lookup"><span data-stu-id="416bb-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-156">**TPMSpecMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="416bb-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="416bb-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-159">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 第 5.3 \| 版 \| 的主要 "，" TSS。TCG \| Level 1 V1.1 \| 區段 2.3.2.18 ") </span><span class="sxs-lookup"><span data-stu-id="416bb-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-160">TPM 的主要版本。</span><span class="sxs-lookup"><span data-stu-id="416bb-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-161">**TPMSpecMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="416bb-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="416bb-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 第 5.3 \| 版 \| 次要版 "，" TSS。TCG \| Level 1 V1.1 \| 區段 2.3.2.18 ") </span><span class="sxs-lookup"><span data-stu-id="416bb-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-165">TPM 的次要版本。</span><span class="sxs-lookup"><span data-stu-id="416bb-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="416bb-166">**TPMState**</span><span class="sxs-lookup"><span data-stu-id="416bb-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="416bb-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-169">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 1 v1dot2 \| Section 9.4 "，" TPM。TCG \| 第2部分 v1dot2 \| 區段 7.1 \| tpm \_ 永久 \_ 旗標 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ tpm**。**RequestTPMStateChange**"，"**CIM \_ TPM**.**TransitioningToTPMState**") </span><span class="sxs-lookup"><span data-stu-id="416bb-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-170">TPM 的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="416bb-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="416bb-171">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="416bb-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-172">**已啟用 S1-Active-擁有的** (2) </span><span class="sxs-lookup"><span data-stu-id="416bb-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-173">**S2 已停用-Active-擁有的** (3) </span><span class="sxs-lookup"><span data-stu-id="416bb-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-174">**已啟用 S3-非使用中-擁有的** (4) </span><span class="sxs-lookup"><span data-stu-id="416bb-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-175">**已停用 S4-非使用中-擁有的** (5) </span><span class="sxs-lookup"><span data-stu-id="416bb-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-176">**已啟用 S5-主動-** 無人擁有的 (6) </span><span class="sxs-lookup"><span data-stu-id="416bb-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-177">**S6 已停用-主動-** 無人 (7) </span><span class="sxs-lookup"><span data-stu-id="416bb-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-178">**S7 已啟用-非** 使用中-無人擁有的 (8) </span><span class="sxs-lookup"><span data-stu-id="416bb-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-179">**S8 已停用-非** 使用中-無人擁有的 (9) </span><span class="sxs-lookup"><span data-stu-id="416bb-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="416bb-180">**不適用** (10) </span><span class="sxs-lookup"><span data-stu-id="416bb-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="416bb-181">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="416bb-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="416bb-182">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="416bb-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="416bb-183">**TransitioningToTPMState**</span><span class="sxs-lookup"><span data-stu-id="416bb-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416bb-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="416bb-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416bb-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="416bb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416bb-186">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ TPM**」。**RequestTPMStateChange**"，"**CIM \_ TPM**.**TPMState**") </span><span class="sxs-lookup"><span data-stu-id="416bb-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="416bb-187">TPM 正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="416bb-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="416bb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="416bb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**已啟用 S1-Active-擁有的** (2) </span><span class="sxs-lookup"><span data-stu-id="416bb-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="416bb-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 已停用-Active-擁有的** (3) </span><span class="sxs-lookup"><span data-stu-id="416bb-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**已啟用 S3-非使用中-擁有的** (4) </span><span class="sxs-lookup"><span data-stu-id="416bb-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="416bb-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**已停用 S4-非使用中-擁有的** (5) </span><span class="sxs-lookup"><span data-stu-id="416bb-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**已啟用 S5-主動-** 無人擁有的 (6) </span><span class="sxs-lookup"><span data-stu-id="416bb-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 已停用-主動-** 無人 (7) </span><span class="sxs-lookup"><span data-stu-id="416bb-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 已啟用-非** 使用中-無人擁有的 (8) </span><span class="sxs-lookup"><span data-stu-id="416bb-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="416bb-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 已停用-非** 使用中-無人擁有的 (9) </span><span class="sxs-lookup"><span data-stu-id="416bb-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="416bb-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (10) </span><span class="sxs-lookup"><span data-stu-id="416bb-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="416bb-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**沒有變更** (11) </span><span class="sxs-lookup"><span data-stu-id="416bb-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="416bb-199"> (12) </span><span class="sxs-lookup"><span data-stu-id="416bb-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="416bb-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="416bb-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="416bb-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="416bb-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="416bb-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="416bb-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="416bb-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="416bb-203">Requirements</span></span>



| <span data-ttu-id="416bb-204">需求</span><span class="sxs-lookup"><span data-stu-id="416bb-204">Requirement</span></span> | <span data-ttu-id="416bb-205">值</span><span class="sxs-lookup"><span data-stu-id="416bb-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416bb-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="416bb-206">Minimum supported client</span></span><br/> | <span data-ttu-id="416bb-207">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="416bb-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="416bb-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="416bb-208">Minimum supported server</span></span><br/> | <span data-ttu-id="416bb-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="416bb-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="416bb-210">命名空間</span><span class="sxs-lookup"><span data-stu-id="416bb-210">Namespace</span></span><br/>                | <span data-ttu-id="416bb-211">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="416bb-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="416bb-212">MOF</span><span class="sxs-lookup"><span data-stu-id="416bb-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="416bb-213"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="416bb-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="416bb-214">DLL</span><span class="sxs-lookup"><span data-stu-id="416bb-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416bb-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="416bb-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="416bb-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="416bb-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416bb-217">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="416bb-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

