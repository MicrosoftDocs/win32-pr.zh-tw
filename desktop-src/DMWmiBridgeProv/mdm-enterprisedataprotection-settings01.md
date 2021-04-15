---
title: MDM_EnterpriseDataProtection_Settings01 類別
description: MDM \_ EnterpriseDataProtection \_ Settings01 類別可用來設定 WINDOWS 資訊保護 (WIP)  (先前稱為企業資料保護) 特定設定。
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- MDM_EnterpriseDataProtection_Settings01 類別
- MDM_EnterpriseDataProtection_Settings01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466208"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="807f5-105">MDM \_ EnterpriseDataProtection \_ Settings01 類別</span><span class="sxs-lookup"><span data-stu-id="807f5-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="807f5-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="807f5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="807f5-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="807f5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="807f5-108">**MDM \_ EnterpriseDataProtection \_ Settings01** 類別可用來設定 Windows 資訊保護 (WIP)  (先前稱為企業資料保護) 特定設定。</span><span class="sxs-lookup"><span data-stu-id="807f5-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="807f5-109">如需有關 WIP 的詳細資訊，請參閱 [使用企業資料保護來保護您的企業資料 (EDP) ](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)。</span><span class="sxs-lookup"><span data-stu-id="807f5-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="807f5-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="807f5-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="807f5-111">語法</span><span class="sxs-lookup"><span data-stu-id="807f5-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="807f5-112">成員</span><span class="sxs-lookup"><span data-stu-id="807f5-112">Members</span></span>

<span data-ttu-id="807f5-113">**MDM \_ EnterpriseDataProtection \_ Settings01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="807f5-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="807f5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="807f5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="807f5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="807f5-115">Properties</span></span>

<span data-ttu-id="807f5-116">**MDM \_ EnterpriseDataProtection \_ Settings01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="807f5-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="807f5-117">AllowAzureRMSForEDP</span><span class="sxs-lookup"><span data-stu-id="807f5-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="807f5-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-120">AllowUserDecryption</span><span class="sxs-lookup"><span data-stu-id="807f5-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="807f5-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-123">DataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="807f5-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="807f5-126">限定詞： **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="807f5-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="807f5-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="807f5-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-130">EDPShowIcons</span><span class="sxs-lookup"><span data-stu-id="807f5-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="807f5-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="807f5-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="807f5-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="807f5-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="807f5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807f5-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="807f5-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="807f5-140">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="807f5-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="807f5-141">此類別的字串為 "Settings"。</span><span class="sxs-lookup"><span data-stu-id="807f5-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="807f5-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="807f5-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="807f5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807f5-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="807f5-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="807f5-146">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="807f5-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="807f5-147">此類別的字串為 "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="807f5-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="807f5-148">RevokeOnUnenroll</span><span class="sxs-lookup"><span data-stu-id="807f5-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-149">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="807f5-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-151">RMSTemplateIDForEDP</span><span class="sxs-lookup"><span data-stu-id="807f5-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="807f5-154">SMBAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="807f5-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="807f5-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="807f5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807f5-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="807f5-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="807f5-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="807f5-157">Requirements</span></span>



| <span data-ttu-id="807f5-158">需求</span><span class="sxs-lookup"><span data-stu-id="807f5-158">Requirement</span></span> | <span data-ttu-id="807f5-159">值</span><span class="sxs-lookup"><span data-stu-id="807f5-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="807f5-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="807f5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="807f5-161">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="807f5-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="807f5-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="807f5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="807f5-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="807f5-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="807f5-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="807f5-164">Namespace</span></span><br/>                | <span data-ttu-id="807f5-165">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="807f5-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="807f5-166">MOF</span><span class="sxs-lookup"><span data-stu-id="807f5-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="807f5-167"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="807f5-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="807f5-168">DLL</span><span class="sxs-lookup"><span data-stu-id="807f5-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="807f5-169"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="807f5-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

