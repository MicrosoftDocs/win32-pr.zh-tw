---
title: Win32_TSLicenseReport 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取使用權遠端桌面服務實例每個使用者 CAL) 在遠端桌面授權伺服器上產生的使用方式報告，以及授權報告產生、提取及刪除作業的方法。
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport 類別遠端桌面服務
- Win32_TSLicenseReport 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843176"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="1597e-105">Win32 \_ TSLicenseReport 類別</span><span class="sxs-lookup"><span data-stu-id="1597e-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="1597e-106">提供遠端桌面服務的每個使用者用戶端存取授權 (RDS 每個使用者的 CAL) 在遠端桌面授權伺服器上產生的使用方式報告，以及授權報告產生、提取和刪除作業的方法。</span><span class="sxs-lookup"><span data-stu-id="1597e-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1597e-107">語法</span><span class="sxs-lookup"><span data-stu-id="1597e-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="1597e-108">成員</span><span class="sxs-lookup"><span data-stu-id="1597e-108">Members</span></span>

<span data-ttu-id="1597e-109">**Win32 \_ TSLicenseReport** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1597e-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="1597e-110">方法</span><span class="sxs-lookup"><span data-stu-id="1597e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1597e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1597e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1597e-112">方法</span><span class="sxs-lookup"><span data-stu-id="1597e-112">Methods</span></span>

<span data-ttu-id="1597e-113">**Win32 \_ TSLicenseReport** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1597e-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="1597e-114">方法</span><span class="sxs-lookup"><span data-stu-id="1597e-114">Method</span></span>                                                                                                         | <span data-ttu-id="1597e-115">描述</span><span class="sxs-lookup"><span data-stu-id="1597e-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1597e-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="1597e-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="1597e-117">刪除遠端桌面授權伺服器上的報表物件。</span><span class="sxs-lookup"><span data-stu-id="1597e-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="1597e-118">這不是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="1597e-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1597e-119">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="1597e-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="1597e-120">抓取報表物件中的專案。</span><span class="sxs-lookup"><span data-stu-id="1597e-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="1597e-121">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="1597e-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="1597e-122">抓取每個使用者用戶端存取授權的失敗遠端桌面服務詳細資料 (RDS 每個使用者的 Cal) 從報告。</span><span class="sxs-lookup"><span data-stu-id="1597e-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="1597e-123">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="1597e-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="1597e-124">抓取每個使用者用戶端存取授權的失敗遠端桌面服務摘要資訊， (RDS 每個使用者的 Cal) 從報告。</span><span class="sxs-lookup"><span data-stu-id="1597e-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="1597e-125">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="1597e-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="1597e-126">從報告取得 (RDS 每一裝置的 Cal) 的每一裝置用戶端存取授權發出遠端桌面服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="1597e-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="1597e-127">**FetchReportSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="1597e-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="1597e-128">從報表物件中抓取授權摘要。</span><span class="sxs-lookup"><span data-stu-id="1597e-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="1597e-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="1597e-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="1597e-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1597e-130">This method is not supported.</span></span><br/> <span data-ttu-id="1597e-131">**Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上產生目前的每個使用者授權使用量報表。</span><span class="sxs-lookup"><span data-stu-id="1597e-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="1597e-132">**GenerateReportEx**</span><span class="sxs-lookup"><span data-stu-id="1597e-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="1597e-133">在遠端桌面授權伺服器上產生目前的每個使用者授權使用量報表。</span><span class="sxs-lookup"><span data-stu-id="1597e-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="1597e-134">屬性</span><span class="sxs-lookup"><span data-stu-id="1597e-134">Properties</span></span>

<span data-ttu-id="1597e-135">**Win32 \_ TSLicenseReport** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1597e-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1597e-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1597e-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1597e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1597e-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1597e-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1597e-140">報表名稱。</span><span class="sxs-lookup"><span data-stu-id="1597e-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-141">**GenerationDateTime**</span><span class="sxs-lookup"><span data-stu-id="1597e-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-142">資料類型： **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="1597e-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1597e-144">RD 授權報告產生日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1597e-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-145">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="1597e-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1597e-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1597e-148">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1597e-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1597e-149">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1597e-149">This property is not supported.</span></span>

<span data-ttu-id="1597e-150">**Windows server 2008 R2 和 Windows server 2008：** 已安裝的 RDS 每個使用者 Cal 數目。</span><span class="sxs-lookup"><span data-stu-id="1597e-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-151">**LicenseUsageCount**</span><span class="sxs-lookup"><span data-stu-id="1597e-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1597e-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1597e-154">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1597e-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1597e-155">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1597e-155">This property is not supported.</span></span>

<span data-ttu-id="1597e-156">**Windows server 2008 R2 和 Windows server 2008：** 目前使用中的 RDS 每個使用者 Cal 數目。</span><span class="sxs-lookup"><span data-stu-id="1597e-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="1597e-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1597e-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1597e-160">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1597e-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1597e-161">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1597e-161">This property is not supported.</span></span>

<span data-ttu-id="1597e-162">**Windows server 2008 R2 和 Windows server 2008：** RD 授權報表範圍類型。</span><span class="sxs-lookup"><span data-stu-id="1597e-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-163">**ScopeValue**</span><span class="sxs-lookup"><span data-stu-id="1597e-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1597e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1597e-166">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1597e-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1597e-167">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1597e-167">This property is not supported.</span></span>

<span data-ttu-id="1597e-168">**Windows server 2008 R2 和 Windows server 2008：** RD 授權報表範圍值。</span><span class="sxs-lookup"><span data-stu-id="1597e-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="1597e-169">**版本**</span><span class="sxs-lookup"><span data-stu-id="1597e-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1597e-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1597e-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1597e-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1597e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1597e-172">RD 授權報表版本。</span><span class="sxs-lookup"><span data-stu-id="1597e-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1597e-173">備註</span><span class="sxs-lookup"><span data-stu-id="1597e-173">Remarks</span></span>

<span data-ttu-id="1597e-174">使用 WMI 產生的報表會顯示在 RD 授權管理員中。</span><span class="sxs-lookup"><span data-stu-id="1597e-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="1597e-175">使用 WMI 刪除的報表也會從 RD 授權管理員中刪除。</span><span class="sxs-lookup"><span data-stu-id="1597e-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="1597e-176">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="1597e-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="1597e-177">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1597e-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1597e-178">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1597e-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1597e-179">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1597e-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1597e-180">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1597e-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1597e-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="1597e-181">Requirements</span></span>



| <span data-ttu-id="1597e-182">需求</span><span class="sxs-lookup"><span data-stu-id="1597e-182">Requirement</span></span> | <span data-ttu-id="1597e-183">值</span><span class="sxs-lookup"><span data-stu-id="1597e-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1597e-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1597e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="1597e-185">都不支援</span><span class="sxs-lookup"><span data-stu-id="1597e-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1597e-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1597e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="1597e-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1597e-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1597e-188">命名空間</span><span class="sxs-lookup"><span data-stu-id="1597e-188">Namespace</span></span><br/>                | <span data-ttu-id="1597e-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1597e-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1597e-190">MOF</span><span class="sxs-lookup"><span data-stu-id="1597e-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1597e-191"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="1597e-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1597e-192">DLL</span><span class="sxs-lookup"><span data-stu-id="1597e-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1597e-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1597e-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1597e-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1597e-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1597e-195">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="1597e-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="1597e-196">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="1597e-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="1597e-197">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="1597e-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="1597e-198">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="1597e-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

