---
title: Win32_TSLicenseServer 類別的 CreateTSCGroup 方法
description: CreateTSCGroup 不再適用于 Windows Server 2012。
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- CreateTSCGroup 方法遠端桌面服務
- CreateTSCGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，CreateTSCGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843224"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d91c4-106">Win32 TSLicenseServer 類別的 CreateTSCGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d91c4-106">CreateTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d91c4-107">\[**CreateTSCGroup** 不再適用于 Windows Server 2012。\]</span><span class="sxs-lookup"><span data-stu-id="d91c4-107">\[**CreateTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="d91c4-108">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d91c4-108">This method is not supported.</span></span>

<span data-ttu-id="d91c4-109">**Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上建立終端機伺服器電腦本機群組。</span><span class="sxs-lookup"><span data-stu-id="d91c4-109">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91c4-110">語法</span><span class="sxs-lookup"><span data-stu-id="d91c4-110">Syntax</span></span>


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="d91c4-111">參數</span><span class="sxs-lookup"><span data-stu-id="d91c4-111">Parameters</span></span>

<span data-ttu-id="d91c4-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d91c4-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d91c4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d91c4-113">Return value</span></span>

<span data-ttu-id="d91c4-114">傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="d91c4-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="d91c4-115">**Windows server 2008 R2 和 Windows server 2008：** 如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d91c4-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d91c4-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d91c4-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d91c4-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d91c4-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d91c4-118">備註</span><span class="sxs-lookup"><span data-stu-id="d91c4-118">Remarks</span></span>

<span data-ttu-id="d91c4-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d91c4-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d91c4-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d91c4-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d91c4-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d91c4-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d91c4-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d91c4-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d91c4-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d91c4-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d91c4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d91c4-124">Requirements</span></span>



| <span data-ttu-id="d91c4-125">需求</span><span class="sxs-lookup"><span data-stu-id="d91c4-125">Requirement</span></span> | <span data-ttu-id="d91c4-126">值</span><span class="sxs-lookup"><span data-stu-id="d91c4-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91c4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d91c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d91c4-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="d91c4-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d91c4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d91c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d91c4-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d91c4-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d91c4-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d91c4-131">End of client support</span></span><br/>    | <span data-ttu-id="d91c4-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="d91c4-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d91c4-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d91c4-133">End of server support</span></span><br/>    | <span data-ttu-id="d91c4-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d91c4-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="d91c4-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="d91c4-135">Namespace</span></span><br/>                | <span data-ttu-id="d91c4-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d91c4-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d91c4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d91c4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d91c4-138"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d91c4-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d91c4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d91c4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d91c4-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d91c4-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91c4-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d91c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91c4-142">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="d91c4-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="d91c4-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="d91c4-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

