---
title: MDM_Policy_Result01_Security02 類別
description: MDM \_ Policy \_ Result01 \_ Security02 類別代表可用的安全性原則。
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- MDM_Policy_Result01_Security02 類別
- MDM_Policy_Result01_Security02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024896"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="4828c-105">MDM \_ 原則 \_ Result01 \_ Security02 類別</span><span class="sxs-lookup"><span data-stu-id="4828c-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="4828c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="4828c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4828c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="4828c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4828c-108">**MDM \_ Policy \_ Result01 \_ Security02** 類別代表可用的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="4828c-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="4828c-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4828c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4828c-110">語法</span><span class="sxs-lookup"><span data-stu-id="4828c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="4828c-111">成員</span><span class="sxs-lookup"><span data-stu-id="4828c-111">Members</span></span>

<span data-ttu-id="4828c-112">**MDM \_ Policy \_ Result01 \_ Security02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4828c-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="4828c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4828c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4828c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4828c-114">Properties</span></span>

<span data-ttu-id="4828c-115">**MDM \_ Policy \_ Result01 \_ Security02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4828c-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4828c-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="4828c-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4828c-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="4828c-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4828c-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="4828c-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4828c-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4828c-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4828c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4828c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4828c-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4828c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4828c-129">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4828c-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="4828c-130">此類別的字串為 "Security"。</span><span class="sxs-lookup"><span data-stu-id="4828c-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="4828c-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4828c-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4828c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4828c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4828c-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4828c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4828c-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4828c-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="4828c-136">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="4828c-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="4828c-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="4828c-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4828c-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="4828c-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4828c-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="4828c-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4828c-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="4828c-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828c-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4828c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828c-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4828c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4828c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="4828c-149">Requirements</span></span>



| <span data-ttu-id="4828c-150">需求</span><span class="sxs-lookup"><span data-stu-id="4828c-150">Requirement</span></span> | <span data-ttu-id="4828c-151">值</span><span class="sxs-lookup"><span data-stu-id="4828c-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4828c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4828c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4828c-153">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4828c-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4828c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4828c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4828c-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="4828c-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4828c-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="4828c-156">Namespace</span></span><br/>                | <span data-ttu-id="4828c-157">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="4828c-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="4828c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4828c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4828c-159"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="4828c-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4828c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4828c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4828c-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4828c-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4828c-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4828c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4828c-163">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="4828c-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

