---
title: MDM_EnterpriseModernAppManagement_AppManagement01_03 類別
description: MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03 類別提供應用程式的特定資訊，例如名稱、版本和發行者。
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_03 類別
- MDM_EnterpriseModernAppManagement_AppManagement01_03 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104987"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="9dacd-105">MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03 類別</span><span class="sxs-lookup"><span data-stu-id="9dacd-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="9dacd-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="9dacd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9dacd-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="9dacd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9dacd-108">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** 類別提供應用程式的特定資訊，例如名稱、版本和發行者。</span><span class="sxs-lookup"><span data-stu-id="9dacd-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="9dacd-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9dacd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dacd-110">語法</span><span class="sxs-lookup"><span data-stu-id="9dacd-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="9dacd-111">成員</span><span class="sxs-lookup"><span data-stu-id="9dacd-111">Members</span></span>

<span data-ttu-id="9dacd-112">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9dacd-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="9dacd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9dacd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dacd-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9dacd-114">Properties</span></span>

<span data-ttu-id="9dacd-115">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9dacd-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9dacd-116">架構</span><span class="sxs-lookup"><span data-stu-id="9dacd-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="9dacd-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="9dacd-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9dacd-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9dacd-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9dacd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9dacd-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9dacd-129">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dacd-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="9dacd-130">針對這個類別，字串是封裝完整名稱的實例。</span><span class="sxs-lookup"><span data-stu-id="9dacd-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="9dacd-131">IsBundle</span><span class="sxs-lookup"><span data-stu-id="9dacd-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dacd-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-134">IsFramework</span><span class="sxs-lookup"><span data-stu-id="9dacd-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dacd-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-137">IsProvisioned</span><span class="sxs-lookup"><span data-stu-id="9dacd-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dacd-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-140">名稱</span><span class="sxs-lookup"><span data-stu-id="9dacd-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-143">PackageStatus</span><span class="sxs-lookup"><span data-stu-id="9dacd-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dacd-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9dacd-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9dacd-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9dacd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-149">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9dacd-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9dacd-150">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9dacd-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="9dacd-151">針對此類別，字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID* / *PackageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="9dacd-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="9dacd-152">發行者</span><span class="sxs-lookup"><span data-stu-id="9dacd-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-155">RequiresReinstall</span><span class="sxs-lookup"><span data-stu-id="9dacd-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dacd-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="9dacd-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-161">使用者</span><span class="sxs-lookup"><span data-stu-id="9dacd-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9dacd-164">版本</span><span class="sxs-lookup"><span data-stu-id="9dacd-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dacd-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dacd-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dacd-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dacd-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dacd-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dacd-167">Requirements</span></span>



| <span data-ttu-id="9dacd-168">需求</span><span class="sxs-lookup"><span data-stu-id="9dacd-168">Requirement</span></span> | <span data-ttu-id="9dacd-169">值</span><span class="sxs-lookup"><span data-stu-id="9dacd-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dacd-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9dacd-170">Minimum supported client</span></span><br/> | <span data-ttu-id="9dacd-171">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9dacd-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9dacd-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9dacd-172">Minimum supported server</span></span><br/> | <span data-ttu-id="9dacd-173">都不支援</span><span class="sxs-lookup"><span data-stu-id="9dacd-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9dacd-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="9dacd-174">Namespace</span></span><br/>                | <span data-ttu-id="9dacd-175">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9dacd-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9dacd-176">MOF</span><span class="sxs-lookup"><span data-stu-id="9dacd-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dacd-177"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="9dacd-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dacd-178">DLL</span><span class="sxs-lookup"><span data-stu-id="9dacd-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dacd-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dacd-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dacd-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dacd-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dacd-181">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="9dacd-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

