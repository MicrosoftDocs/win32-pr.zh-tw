---
title: 'Win32_TSLicenseReport 類別的 GenerateReport 方法 (Gpmgmt) '
description: GenerateReport 不再適用于 Windows Server 2012。
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- GenerateReport 方法遠端桌面服務
- GenerateReport 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，GenerateReport 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384993"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="18e45-106">Win32 TSLicenseReport 類別的 GenerateReport 方法 \_</span><span class="sxs-lookup"><span data-stu-id="18e45-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="18e45-107">\[**GenerateReport** 不再適用于 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="18e45-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="18e45-108">相反地，請使用 [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)。\]</span><span class="sxs-lookup"><span data-stu-id="18e45-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="18e45-109">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18e45-109">This method is not supported.</span></span>

<span data-ttu-id="18e45-110">**Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上產生目前的每個使用者授權使用量報表。</span><span class="sxs-lookup"><span data-stu-id="18e45-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e45-111">語法</span><span class="sxs-lookup"><span data-stu-id="18e45-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="18e45-112">參數</span><span class="sxs-lookup"><span data-stu-id="18e45-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e45-113">*ScopeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18e45-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e45-114">授權使用方式報表的範圍。</span><span class="sxs-lookup"><span data-stu-id="18e45-114">Scope of the license usage report.</span></span> <span data-ttu-id="18e45-115">它可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="18e45-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="18e45-116">1</span><span class="sxs-lookup"><span data-stu-id="18e45-116">1</span></span>
</dt> <dd>

<span data-ttu-id="18e45-117">系統會為整個定義域產生報告。</span><span class="sxs-lookup"><span data-stu-id="18e45-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="18e45-118">2</span><span class="sxs-lookup"><span data-stu-id="18e45-118">2</span></span>
</dt> <dd>

<span data-ttu-id="18e45-119">系統會為 *ScopeValue* 參數中指定的組織單位 (OU) 產生報表。</span><span class="sxs-lookup"><span data-stu-id="18e45-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18e45-120">3</span><span class="sxs-lookup"><span data-stu-id="18e45-120">3</span></span>
</dt> <dd>

<span data-ttu-id="18e45-121">系統會為所有信任的網域產生報告。</span><span class="sxs-lookup"><span data-stu-id="18e45-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="18e45-122">*ScopeValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18e45-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e45-123">如果 *ScopeType* 參數為2，則 *ScopeType* 會指定要產生報告的 OU。</span><span class="sxs-lookup"><span data-stu-id="18e45-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="18e45-124">您必須使用 **ou =**_OUName1_*_，ou =_*_OUName2_\*\* 的格式來指定 *ScopeValue* 。</span><span class="sxs-lookup"><span data-stu-id="18e45-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="18e45-125">*檔案名* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18e45-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18e45-126">產生之報表的檔案名。</span><span class="sxs-lookup"><span data-stu-id="18e45-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e45-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="18e45-127">Return value</span></span>

<span data-ttu-id="18e45-128">傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="18e45-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="18e45-129">**Windows server 2008 R2 和 Windows server 2008：** 如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="18e45-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="18e45-130">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="18e45-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="18e45-131">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="18e45-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18e45-132">備註</span><span class="sxs-lookup"><span data-stu-id="18e45-132">Remarks</span></span>

<span data-ttu-id="18e45-133">此為靜態方法。</span><span class="sxs-lookup"><span data-stu-id="18e45-133">This is a static method.</span></span>

<span data-ttu-id="18e45-134">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="18e45-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="18e45-135">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="18e45-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18e45-136">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="18e45-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18e45-137">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="18e45-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18e45-138">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="18e45-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18e45-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="18e45-139">Requirements</span></span>



| <span data-ttu-id="18e45-140">需求</span><span class="sxs-lookup"><span data-stu-id="18e45-140">Requirement</span></span> | <span data-ttu-id="18e45-141">值</span><span class="sxs-lookup"><span data-stu-id="18e45-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e45-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18e45-142">Minimum supported client</span></span><br/> | <span data-ttu-id="18e45-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="18e45-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="18e45-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18e45-144">Minimum supported server</span></span><br/> | <span data-ttu-id="18e45-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18e45-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="18e45-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="18e45-146">End of client support</span></span><br/>    | <span data-ttu-id="18e45-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="18e45-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="18e45-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="18e45-148">End of server support</span></span><br/>    | <span data-ttu-id="18e45-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18e45-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="18e45-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="18e45-150">Namespace</span></span><br/>                | <span data-ttu-id="18e45-151">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="18e45-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="18e45-152">標頭</span><span class="sxs-lookup"><span data-stu-id="18e45-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="18e45-153"><dt>Gpmgmt。h</dt></span><span class="sxs-lookup"><span data-stu-id="18e45-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="18e45-154">MOF</span><span class="sxs-lookup"><span data-stu-id="18e45-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18e45-155"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="18e45-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18e45-156">DLL</span><span class="sxs-lookup"><span data-stu-id="18e45-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e45-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e45-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e45-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18e45-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e45-159">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="18e45-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

