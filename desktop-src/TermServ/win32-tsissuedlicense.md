---
title: Win32_TSIssuedLicense 類別
description: 描述 (RDS \ 160; 的每一裝置用戶端存取使用權遠端桌面服務實例每一裝置的 Cal) 從遠端桌面授權伺服器發出。
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense 類別遠端桌面服務
- Win32_TSIssuedLicense 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968764"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="687b0-105">Win32 \_ TSIssuedLicense 類別</span><span class="sxs-lookup"><span data-stu-id="687b0-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="687b0-106">描述從遠端桌面授權伺服器發出的每一裝置用戶端存取授權 (RDS 每一裝置的 Cal) 的遠端桌面服務實例。</span><span class="sxs-lookup"><span data-stu-id="687b0-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="687b0-107">語法</span><span class="sxs-lookup"><span data-stu-id="687b0-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="687b0-108">成員</span><span class="sxs-lookup"><span data-stu-id="687b0-108">Members</span></span>

<span data-ttu-id="687b0-109">**Win32 \_ TSIssuedLicense** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="687b0-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="687b0-110">方法</span><span class="sxs-lookup"><span data-stu-id="687b0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="687b0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="687b0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="687b0-112">方法</span><span class="sxs-lookup"><span data-stu-id="687b0-112">Methods</span></span>

<span data-ttu-id="687b0-113">**Win32 \_ TSIssuedLicense** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="687b0-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="687b0-114">方法</span><span class="sxs-lookup"><span data-stu-id="687b0-114">Method</span></span>                                         | <span data-ttu-id="687b0-115">描述</span><span class="sxs-lookup"><span data-stu-id="687b0-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="687b0-116">**撤銷**</span><span class="sxs-lookup"><span data-stu-id="687b0-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="687b0-117">撤銷 **Win32 \_ TSIssuedLicense** 物件所代表的 RDS 每一裝置 cal。</span><span class="sxs-lookup"><span data-stu-id="687b0-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="687b0-118">屬性</span><span class="sxs-lookup"><span data-stu-id="687b0-118">Properties</span></span>

<span data-ttu-id="687b0-119">**Win32 \_ TSIssuedLicense** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="687b0-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687b0-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="687b0-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-121">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="687b0-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-123">識別授權將到期的日期。</span><span class="sxs-lookup"><span data-stu-id="687b0-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-124">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="687b0-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-125">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="687b0-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-127">識別授權的發出日期。</span><span class="sxs-lookup"><span data-stu-id="687b0-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-128">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="687b0-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="687b0-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687b0-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="687b0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="687b0-132">識別遠端桌面服務的授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="687b0-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-133">**LicenseId**</span><span class="sxs-lookup"><span data-stu-id="687b0-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="687b0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687b0-136">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="687b0-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="687b0-137">此授權的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="687b0-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-138">**LicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="687b0-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="687b0-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-141">授權的狀態。</span><span class="sxs-lookup"><span data-stu-id="687b0-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="687b0-142">0</span><span class="sxs-lookup"><span data-stu-id="687b0-142">0</span></span>
</dt> <dd>

<span data-ttu-id="687b0-143">授權狀態不明。</span><span class="sxs-lookup"><span data-stu-id="687b0-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-144">1</span><span class="sxs-lookup"><span data-stu-id="687b0-144">1</span></span>
</dt> <dd>

<span data-ttu-id="687b0-145">授權是暫時性授權。</span><span class="sxs-lookup"><span data-stu-id="687b0-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-146">2</span><span class="sxs-lookup"><span data-stu-id="687b0-146">2</span></span>
</dt> <dd>

<span data-ttu-id="687b0-147">授權為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="687b0-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-148">3</span><span class="sxs-lookup"><span data-stu-id="687b0-148">3</span></span>
</dt> <dd>

<span data-ttu-id="687b0-149">授權是升級授權。</span><span class="sxs-lookup"><span data-stu-id="687b0-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-150">4</span><span class="sxs-lookup"><span data-stu-id="687b0-150">4</span></span>
</dt> <dd>

<span data-ttu-id="687b0-151">已撤銷授權。</span><span class="sxs-lookup"><span data-stu-id="687b0-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-152">5</span><span class="sxs-lookup"><span data-stu-id="687b0-152">5</span></span>
</dt> <dd>

<span data-ttu-id="687b0-153">授權狀態為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="687b0-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-154">6</span><span class="sxs-lookup"><span data-stu-id="687b0-154">6</span></span>
</dt> <dd>

<span data-ttu-id="687b0-155">授權是並行授權。</span><span class="sxs-lookup"><span data-stu-id="687b0-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="687b0-156">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="687b0-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687b0-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-159">授權發出的硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="687b0-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-160">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="687b0-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687b0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-163">授權發出的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="687b0-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="687b0-164">**sIssuedToUser**</span><span class="sxs-lookup"><span data-stu-id="687b0-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687b0-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687b0-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687b0-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687b0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687b0-167">發出授權的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="687b0-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="687b0-168">備註</span><span class="sxs-lookup"><span data-stu-id="687b0-168">Remarks</span></span>

<span data-ttu-id="687b0-169">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="687b0-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="687b0-170">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="687b0-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="687b0-171">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="687b0-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="687b0-172">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="687b0-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="687b0-173">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="687b0-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="687b0-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="687b0-174">Requirements</span></span>



| <span data-ttu-id="687b0-175">需求</span><span class="sxs-lookup"><span data-stu-id="687b0-175">Requirement</span></span> | <span data-ttu-id="687b0-176">值</span><span class="sxs-lookup"><span data-stu-id="687b0-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="687b0-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="687b0-177">Minimum supported client</span></span><br/> | <span data-ttu-id="687b0-178">都不支援</span><span class="sxs-lookup"><span data-stu-id="687b0-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="687b0-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="687b0-179">Minimum supported server</span></span><br/> | <span data-ttu-id="687b0-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="687b0-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="687b0-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="687b0-181">Namespace</span></span><br/>                | <span data-ttu-id="687b0-182">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="687b0-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="687b0-183">MOF</span><span class="sxs-lookup"><span data-stu-id="687b0-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687b0-184"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="687b0-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="687b0-185">DLL</span><span class="sxs-lookup"><span data-stu-id="687b0-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687b0-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687b0-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="687b0-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="687b0-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687b0-188">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="687b0-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="687b0-189">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="687b0-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="687b0-190">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="687b0-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="687b0-191">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="687b0-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

