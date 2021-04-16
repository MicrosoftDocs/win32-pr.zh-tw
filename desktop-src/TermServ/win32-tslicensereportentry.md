---
title: Win32_TSLicenseReportEntry 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取使用權發出遠端桌面服務的詳細資料;) 的每個使用者 CAL。
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry 類別遠端桌面服務
- Win32_TSLicenseReportEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383953"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="b452f-105">Win32 \_ TSLicenseReportEntry 類別</span><span class="sxs-lookup"><span data-stu-id="b452f-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="b452f-106">提供每個使用者用戶端存取使用權 (RDS 每個使用者 CAL) 所發出遠端桌面服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b452f-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="b452f-107">語法</span><span class="sxs-lookup"><span data-stu-id="b452f-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="b452f-108">成員</span><span class="sxs-lookup"><span data-stu-id="b452f-108">Members</span></span>

<span data-ttu-id="b452f-109">**Win32 \_ TSLicenseReportEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b452f-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="b452f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b452f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b452f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b452f-111">Properties</span></span>

<span data-ttu-id="b452f-112">**Win32 \_ TSLicenseReportEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b452f-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b452f-113">**CALType**</span><span class="sxs-lookup"><span data-stu-id="b452f-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b452f-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b452f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b452f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b452f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b452f-116">指定所發出之 CAL 的類型。</span><span class="sxs-lookup"><span data-stu-id="b452f-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="b452f-117">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b452f-117">This will be one of the following values.</span></span>

<span data-ttu-id="b452f-118">**Windows server 2008 R2 和 Windows server 2008：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b452f-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="b452f-119">「內建 TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="b452f-120">「TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="b452f-121">「TS 網際網路連接器 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="b452f-122">「TS 每個使用者 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-122">"TS Per User CAL"</span></span>

<span data-ttu-id="b452f-123">「TS 或 RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="b452f-124">「TS 或 RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="b452f-125">「每個裝置訂用帳戶授權的 VDI 標準套件」</span><span class="sxs-lookup"><span data-stu-id="b452f-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="b452f-126">「VDI Premium Suite 每個裝置訂用帳戶授權」</span><span class="sxs-lookup"><span data-stu-id="b452f-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="b452f-127">「RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="b452f-128">「RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b452f-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="b452f-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="b452f-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b452f-130">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="b452f-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b452f-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b452f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b452f-132">發給使用者之授權的到期日。</span><span class="sxs-lookup"><span data-stu-id="b452f-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="b452f-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="b452f-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b452f-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b452f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b452f-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b452f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b452f-136">已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。</span><span class="sxs-lookup"><span data-stu-id="b452f-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="b452f-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="b452f-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="b452f-138">此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b452f-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b452f-139">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="b452f-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="b452f-140">此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b452f-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b452f-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="b452f-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="b452f-142">此授權僅支援執行 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b452f-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b452f-143">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="b452f-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b452f-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b452f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b452f-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b452f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b452f-146">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="b452f-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="b452f-147">4</span><span class="sxs-lookup"><span data-stu-id="b452f-147">4</span></span>
</dt> <dd>

<span data-ttu-id="b452f-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b452f-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="b452f-149">3</span><span class="sxs-lookup"><span data-stu-id="b452f-149">3</span></span>
</dt> <dd>

<span data-ttu-id="b452f-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b452f-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="b452f-151">2</span><span class="sxs-lookup"><span data-stu-id="b452f-151">2</span></span>
</dt> <dd>

<span data-ttu-id="b452f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b452f-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="b452f-153">1</span><span class="sxs-lookup"><span data-stu-id="b452f-153">1</span></span>
</dt> <dd>

<span data-ttu-id="b452f-154">不支援。</span><span class="sxs-lookup"><span data-stu-id="b452f-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b452f-155">0</span><span class="sxs-lookup"><span data-stu-id="b452f-155">0</span></span>
</dt> <dd>

<span data-ttu-id="b452f-156">不支援。</span><span class="sxs-lookup"><span data-stu-id="b452f-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b452f-157">**使用者**</span><span class="sxs-lookup"><span data-stu-id="b452f-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b452f-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b452f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b452f-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b452f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b452f-160">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b452f-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b452f-161">授權簽發者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b452f-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b452f-162">備註</span><span class="sxs-lookup"><span data-stu-id="b452f-162">Remarks</span></span>

<span data-ttu-id="b452f-163">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="b452f-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b452f-164">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b452f-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b452f-165">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b452f-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b452f-166">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b452f-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b452f-167">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b452f-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b452f-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="b452f-168">Requirements</span></span>



| <span data-ttu-id="b452f-169">需求</span><span class="sxs-lookup"><span data-stu-id="b452f-169">Requirement</span></span> | <span data-ttu-id="b452f-170">值</span><span class="sxs-lookup"><span data-stu-id="b452f-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b452f-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b452f-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b452f-172">都不支援</span><span class="sxs-lookup"><span data-stu-id="b452f-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b452f-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b452f-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b452f-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b452f-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b452f-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="b452f-175">Namespace</span></span><br/>                | <span data-ttu-id="b452f-176">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b452f-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b452f-177">MOF</span><span class="sxs-lookup"><span data-stu-id="b452f-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b452f-178"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b452f-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b452f-179">DLL</span><span class="sxs-lookup"><span data-stu-id="b452f-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b452f-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b452f-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b452f-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b452f-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b452f-182">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="b452f-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b452f-183">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="b452f-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="b452f-184">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b452f-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="b452f-185">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="b452f-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b452f-186">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="b452f-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

