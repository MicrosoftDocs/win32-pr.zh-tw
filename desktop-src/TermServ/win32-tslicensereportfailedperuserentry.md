---
title: Win32_TSLicenseReportFailedPerUserEntry 類別
description: 提供有關每個使用者用戶端存取使用權的失敗遠端桌面服務詳細資料 (RDS \ 160;) 的每個使用者 CAL。
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry 類別遠端桌面服務
- Win32_TSLicenseReportFailedPerUserEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383950"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="8fd3f-105">Win32 \_ TSLicenseReportFailedPerUserEntry 類別</span><span class="sxs-lookup"><span data-stu-id="8fd3f-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="8fd3f-106">提供每個使用者用戶端存取使用權 (RDS 每個使用者 CAL) 的失敗遠端桌面服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="8fd3f-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd3f-108">語法</span><span class="sxs-lookup"><span data-stu-id="8fd3f-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="8fd3f-109">成員</span><span class="sxs-lookup"><span data-stu-id="8fd3f-109">Members</span></span>

<span data-ttu-id="8fd3f-110">**Win32 \_ TSLicenseReportFailedPerUserEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8fd3f-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="8fd3f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd3f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fd3f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd3f-112">Properties</span></span>

<span data-ttu-id="8fd3f-113">**Win32 \_ TSLicenseReportFailedPerUserEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fd3f-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd3f-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd3f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fd3f-117">指定所發出之 CAL 的類型。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="8fd3f-118">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-118">This will be one of the following values.</span></span>

<span data-ttu-id="8fd3f-119">「內建 TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="8fd3f-120">「TS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="8fd3f-121">「TS 網際網路連接器 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="8fd3f-122">「TS 每個使用者 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-122">"TS Per User CAL"</span></span>

<span data-ttu-id="8fd3f-123">「TS 或 RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="8fd3f-124">「TS 或 RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="8fd3f-125">「每個裝置訂用帳戶授權的 VDI 標準套件」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="8fd3f-126">「VDI Premium Suite 每個裝置訂用帳戶授權」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="8fd3f-127">「RDS 每一裝置的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="8fd3f-128">「RDS 每個使用者的 CAL」</span><span class="sxs-lookup"><span data-stu-id="8fd3f-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd3f-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd3f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fd3f-132">已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="8fd3f-133">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="8fd3f-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="8fd3f-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-135">此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-136">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="8fd3f-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-137">此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="8fd3f-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-139">此授權僅支援執行 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8fd3f-140">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd3f-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd3f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fd3f-143">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="8fd3f-144">4</span><span class="sxs-lookup"><span data-stu-id="8fd3f-144">4</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fd3f-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-146">3</span><span class="sxs-lookup"><span data-stu-id="8fd3f-146">3</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fd3f-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-148">2</span><span class="sxs-lookup"><span data-stu-id="8fd3f-148">2</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fd3f-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-150">1</span><span class="sxs-lookup"><span data-stu-id="8fd3f-150">1</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-151">不支援。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-152">0</span><span class="sxs-lookup"><span data-stu-id="8fd3f-152">0</span></span>
</dt> <dd>

<span data-ttu-id="8fd3f-153">不支援。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8fd3f-154">**TriedIssuanceOn**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd3f-155">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd3f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fd3f-157">嘗試發佈授權的日期。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="8fd3f-158">**使用者**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd3f-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd3f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd3f-161">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fd3f-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fd3f-162">嘗試發行授權的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8fd3f-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fd3f-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fd3f-163">Requirements</span></span>



| <span data-ttu-id="8fd3f-164">需求</span><span class="sxs-lookup"><span data-stu-id="8fd3f-164">Requirement</span></span> | <span data-ttu-id="8fd3f-165">值</span><span class="sxs-lookup"><span data-stu-id="8fd3f-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd3f-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fd3f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd3f-167">都不支援</span><span class="sxs-lookup"><span data-stu-id="8fd3f-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8fd3f-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fd3f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd3f-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fd3f-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="8fd3f-170">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fd3f-170">Namespace</span></span><br/>                | <span data-ttu-id="8fd3f-171">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8fd3f-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8fd3f-172">MOF</span><span class="sxs-lookup"><span data-stu-id="8fd3f-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fd3f-173"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fd3f-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fd3f-174">DLL</span><span class="sxs-lookup"><span data-stu-id="8fd3f-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fd3f-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fd3f-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd3f-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fd3f-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd3f-177">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

