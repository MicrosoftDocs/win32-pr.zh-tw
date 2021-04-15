---
title: Win32_TSLicenseReport 類別的 DeleteReport 方法
description: 刪除遠端桌面授權伺服器上的報表物件。 這不是靜態方法。
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- DeleteReport 方法遠端桌面服務
- DeleteReport 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，DeleteReport 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508356"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="e39cb-107">Win32 TSLicenseReport 類別的 DeleteReport 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e39cb-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="e39cb-108">刪除遠端桌面授權伺服器上的報表物件。</span><span class="sxs-lookup"><span data-stu-id="e39cb-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="e39cb-109">這不是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="e39cb-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e39cb-110">語法</span><span class="sxs-lookup"><span data-stu-id="e39cb-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="e39cb-111">參數</span><span class="sxs-lookup"><span data-stu-id="e39cb-111">Parameters</span></span>

<span data-ttu-id="e39cb-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e39cb-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e39cb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e39cb-113">Return value</span></span>

<span data-ttu-id="e39cb-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e39cb-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e39cb-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e39cb-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e39cb-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e39cb-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e39cb-117">備註</span><span class="sxs-lookup"><span data-stu-id="e39cb-117">Remarks</span></span>

<span data-ttu-id="e39cb-118">這不是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="e39cb-118">This is not a static method.</span></span> <span data-ttu-id="e39cb-119">您必須從每個使用者授權使用量報表物件呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e39cb-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="e39cb-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e39cb-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e39cb-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e39cb-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e39cb-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e39cb-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e39cb-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e39cb-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e39cb-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e39cb-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e39cb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e39cb-125">Requirements</span></span>



| <span data-ttu-id="e39cb-126">需求</span><span class="sxs-lookup"><span data-stu-id="e39cb-126">Requirement</span></span> | <span data-ttu-id="e39cb-127">值</span><span class="sxs-lookup"><span data-stu-id="e39cb-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39cb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e39cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e39cb-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="e39cb-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e39cb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e39cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e39cb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e39cb-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e39cb-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="e39cb-132">Namespace</span></span><br/>                | <span data-ttu-id="e39cb-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e39cb-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e39cb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e39cb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e39cb-135"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e39cb-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e39cb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e39cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e39cb-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e39cb-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e39cb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e39cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39cb-139">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="e39cb-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

