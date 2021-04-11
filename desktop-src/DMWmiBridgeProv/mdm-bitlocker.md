---
title: MDM_BitLocker 類別
description: '\_企業會使用 MDM BitLocker 類別來管理電腦和裝置的加密。'
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- MDM_BitLocker 類別
- MDM_BitLocker 類別，描述
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106139"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="b9e1a-105">MDM \_ BitLocker 類別</span><span class="sxs-lookup"><span data-stu-id="b9e1a-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="b9e1a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b9e1a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9e1a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b9e1a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9e1a-108">\_企業會使用 MDM BitLocker 類別來管理電腦和裝置的加密。</span><span class="sxs-lookup"><span data-stu-id="b9e1a-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="b9e1a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9e1a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e1a-110">語法</span><span class="sxs-lookup"><span data-stu-id="b9e1a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="b9e1a-111">成員</span><span class="sxs-lookup"><span data-stu-id="b9e1a-111">Members</span></span>

<span data-ttu-id="b9e1a-112">**MDM \_ BitLocker** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b9e1a-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="b9e1a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b9e1a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9e1a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b9e1a-114">Properties</span></span>

<span data-ttu-id="b9e1a-115">**MDM \_ BitLocker** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b9e1a-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b9e1a-116">AllowWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b9e1a-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-119">EncryptionMethodByDriveType</span><span class="sxs-lookup"><span data-stu-id="b9e1a-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-122">FixedDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="b9e1a-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="b9e1a-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9e1a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b9e1a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9e1a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9e1a-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b9e1a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9e1a-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="b9e1a-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="b9e1a-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-140">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-142">RequireStorageCardEncryption</span><span class="sxs-lookup"><span data-stu-id="b9e1a-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-143">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-145">SystemDrivesMinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="b9e1a-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-148">SystemDrivesRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="b9e1a-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-151">SystemDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="b9e1a-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9e1a-154">SystemDrivesRequireStartupAuthentication</span><span class="sxs-lookup"><span data-stu-id="b9e1a-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9e1a-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9e1a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9e1a-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b9e1a-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9e1a-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9e1a-157">Requirements</span></span>



| <span data-ttu-id="b9e1a-158">需求</span><span class="sxs-lookup"><span data-stu-id="b9e1a-158">Requirement</span></span> | <span data-ttu-id="b9e1a-159">值</span><span class="sxs-lookup"><span data-stu-id="b9e1a-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e1a-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9e1a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e1a-161">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9e1a-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9e1a-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9e1a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e1a-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="b9e1a-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b9e1a-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9e1a-164">Namespace</span></span><br/>                | <span data-ttu-id="b9e1a-165">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b9e1a-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b9e1a-166">MOF</span><span class="sxs-lookup"><span data-stu-id="b9e1a-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9e1a-167"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9e1a-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9e1a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="b9e1a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9e1a-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9e1a-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

