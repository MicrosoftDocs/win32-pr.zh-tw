---
title: Win32_TSLicenseReportPerDeviceEntry 類別
description: 提供有關每一裝置用戶端存取使用權 (RDS \ 160; 的失敗遠端桌面服務詳細資料;) 的每一裝置 CAL。
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry 類別遠端桌面服務
- Win32_TSLicenseReportPerDeviceEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464472"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="b0886-105">Win32 \_ TSLicenseReportPerDeviceEntry 類別</span><span class="sxs-lookup"><span data-stu-id="b0886-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="b0886-106">提供 (RDS 每一裝置的 CAL) 的每一裝置用戶端存取授權失敗遠端桌面服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0886-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="b0886-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b0886-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0886-108">語法</span><span class="sxs-lookup"><span data-stu-id="b0886-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="b0886-109">成員</span><span class="sxs-lookup"><span data-stu-id="b0886-109">Members</span></span>

<span data-ttu-id="b0886-110">**Win32 \_ TSLicenseReportPerDeviceEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0886-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="b0886-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b0886-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0886-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b0886-112">Properties</span></span>

<span data-ttu-id="b0886-113">**Win32 \_ TSLicenseReportPerDeviceEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b0886-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0886-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="b0886-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0886-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0886-117">指定所發出之 CAL 的類型。</span><span class="sxs-lookup"><span data-stu-id="b0886-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="b0886-118">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b0886-118">This will be one of the following values.</span></span>

<span data-ttu-id="b0886-119">「內建 TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="b0886-120">「TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="b0886-121">「TS 網際網路連接器 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="b0886-122">「TS 每個使用者 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-122">"TS Per User CAL"</span></span>

<span data-ttu-id="b0886-123">「TS 或 RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="b0886-124">「TS 或 RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="b0886-125">「每個裝置訂用帳戶授權的 VDI 標準套件」</span><span class="sxs-lookup"><span data-stu-id="b0886-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="b0886-126">「VDI Premium Suite 每個裝置訂用帳戶授權」</span><span class="sxs-lookup"><span data-stu-id="b0886-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="b0886-127">「RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="b0886-128">「RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="b0886-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="b0886-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="b0886-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-130">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="b0886-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0886-132">授權的到期日。</span><span class="sxs-lookup"><span data-stu-id="b0886-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="b0886-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="b0886-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0886-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0886-136">已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。</span><span class="sxs-lookup"><span data-stu-id="b0886-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="b0886-137">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b0886-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="b0886-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="b0886-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="b0886-139">此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0886-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b0886-140">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="b0886-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="b0886-141">此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0886-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b0886-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="b0886-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="b0886-143">此授權僅支援執行 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0886-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0886-144">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="b0886-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b0886-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0886-147">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0886-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="b0886-148">4</span><span class="sxs-lookup"><span data-stu-id="b0886-148">4</span></span>
</dt> <dd>

<span data-ttu-id="b0886-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0886-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="b0886-150">3</span><span class="sxs-lookup"><span data-stu-id="b0886-150">3</span></span>
</dt> <dd>

<span data-ttu-id="b0886-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0886-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="b0886-152">2</span><span class="sxs-lookup"><span data-stu-id="b0886-152">2</span></span>
</dt> <dd>

<span data-ttu-id="b0886-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0886-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="b0886-154">1</span><span class="sxs-lookup"><span data-stu-id="b0886-154">1</span></span>
</dt> <dd>

<span data-ttu-id="b0886-155">不支援。</span><span class="sxs-lookup"><span data-stu-id="b0886-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b0886-156">0</span><span class="sxs-lookup"><span data-stu-id="b0886-156">0</span></span>
</dt> <dd>

<span data-ttu-id="b0886-157">不支援。</span><span class="sxs-lookup"><span data-stu-id="b0886-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0886-158">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="b0886-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0886-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0886-161">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b0886-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b0886-162">電腦的硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0886-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b0886-163">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="b0886-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0886-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0886-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0886-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0886-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0886-166">嘗試授權發行的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b0886-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0886-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0886-167">Requirements</span></span>



| <span data-ttu-id="b0886-168">需求</span><span class="sxs-lookup"><span data-stu-id="b0886-168">Requirement</span></span> | <span data-ttu-id="b0886-169">值</span><span class="sxs-lookup"><span data-stu-id="b0886-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0886-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0886-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b0886-171">都不支援</span><span class="sxs-lookup"><span data-stu-id="b0886-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b0886-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0886-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b0886-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0886-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="b0886-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="b0886-174">Namespace</span></span><br/>                | <span data-ttu-id="b0886-175">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b0886-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b0886-176">MOF</span><span class="sxs-lookup"><span data-stu-id="b0886-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0886-177"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0886-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0886-178">DLL</span><span class="sxs-lookup"><span data-stu-id="b0886-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0886-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0886-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0886-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0886-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0886-181">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="b0886-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

