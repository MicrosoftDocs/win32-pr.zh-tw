---
title: Win32_TSLicenseReportSummaryEntry 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取授權已安裝和發行遠端桌面服務的摘要;) 的每個使用者 Cal。
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry 類別遠端桌面服務
- Win32_TSLicenseReportSummaryEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969559"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="8fe6b-105">Win32 \_ TSLicenseReportSummaryEntry 類別</span><span class="sxs-lookup"><span data-stu-id="8fe6b-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="8fe6b-106">提供每個使用者用戶端存取授權 (RDS 每個使用者的 Cal) 的已安裝和發行遠端桌面服務的摘要。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe6b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8fe6b-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="8fe6b-108">成員</span><span class="sxs-lookup"><span data-stu-id="8fe6b-108">Members</span></span>

<span data-ttu-id="8fe6b-109">**Win32 \_ TSLicenseReportSummaryEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8fe6b-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="8fe6b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8fe6b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fe6b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8fe6b-111">Properties</span></span>

<span data-ttu-id="8fe6b-112">**Win32 \_ TSLicenseReportSummaryEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fe6b-113">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-116">已安裝的 RDS 每個使用者 Cal 數目。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-117">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-120">所發出的 RDS 每個使用者 Cal 數目。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-124">已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="8fe6b-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="8fe6b-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-126">此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-127">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="8fe6b-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-128">此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="8fe6b-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-130">此授權僅支援執行 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8fe6b-131">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-134">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="8fe6b-135">4</span><span class="sxs-lookup"><span data-stu-id="8fe6b-135">4</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fe6b-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-137">3</span><span class="sxs-lookup"><span data-stu-id="8fe6b-137">3</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fe6b-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-139">2</span><span class="sxs-lookup"><span data-stu-id="8fe6b-139">2</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fe6b-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-141">1</span><span class="sxs-lookup"><span data-stu-id="8fe6b-141">1</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-142">不支援。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-143">0</span><span class="sxs-lookup"><span data-stu-id="8fe6b-143">0</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-144">不支援。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8fe6b-145">**TSCALAvailability**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-148">RDS 每個使用者 Cal 的可用性。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="8fe6b-149">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="8fe6b-150">目前</span><span class="sxs-lookup"><span data-stu-id="8fe6b-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-151">您可以使用 RDS 每個使用者的 Cal。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-152">有限</span><span class="sxs-lookup"><span data-stu-id="8fe6b-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-153">RDS 每個使用者 Cal 的可用性有限。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-154">"None"</span><span class="sxs-lookup"><span data-stu-id="8fe6b-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-155">無法使用 RDS 每個使用者的 Cal。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-156">「未追蹤」</span><span class="sxs-lookup"><span data-stu-id="8fe6b-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-157">未追蹤 RDS 每個使用者 Cal 的可用性。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8fe6b-158">**TSCALType**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6b-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fe6b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6b-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fe6b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6b-161">RDS 每個使用者 Cal 的類型。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="8fe6b-162">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="8fe6b-163">「每個裝置」</span><span class="sxs-lookup"><span data-stu-id="8fe6b-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-164">每個裝置會發出 RDS 每個使用者的 Cal。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-165">「每位使用者」</span><span class="sxs-lookup"><span data-stu-id="8fe6b-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-166">每個使用者都會發出 RDS 每個使用者的 Cal。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6b-167">不明</span><span class="sxs-lookup"><span data-stu-id="8fe6b-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="8fe6b-168">RDS 每個使用者 Cal 的類型未知。</span><span class="sxs-lookup"><span data-stu-id="8fe6b-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fe6b-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe6b-169">Requirements</span></span>



| <span data-ttu-id="8fe6b-170">需求</span><span class="sxs-lookup"><span data-stu-id="8fe6b-170">Requirement</span></span> | <span data-ttu-id="8fe6b-171">值</span><span class="sxs-lookup"><span data-stu-id="8fe6b-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe6b-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fe6b-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe6b-173">都不支援</span><span class="sxs-lookup"><span data-stu-id="8fe6b-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8fe6b-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fe6b-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe6b-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fe6b-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8fe6b-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fe6b-176">Namespace</span></span><br/>                | <span data-ttu-id="8fe6b-177">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8fe6b-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8fe6b-178">MOF</span><span class="sxs-lookup"><span data-stu-id="8fe6b-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fe6b-179"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fe6b-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fe6b-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe6b-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe6b-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe6b-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





