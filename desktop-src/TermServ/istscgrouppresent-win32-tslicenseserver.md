---
title: Win32_TSLicenseServer 類別的 IsTSCGroupPresent 方法
description: IsTSCGroupPresent 不再適用于 Windows Server 2012。
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- IsTSCGroupPresent 方法遠端桌面服務
- IsTSCGroupPresent 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsTSCGroupPresent 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024873"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="9f96c-106">Win32 TSLicenseServer 類別的 IsTSCGroupPresent 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9f96c-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9f96c-107">\[**IsTSCGroupPresent** 不再適用于 Windows Server 2012。\]</span><span class="sxs-lookup"><span data-stu-id="9f96c-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="9f96c-108">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9f96c-108">This method is not supported.</span></span>

<span data-ttu-id="9f96c-109">**Windows server 2008 R2 和 Windows server 2008：** 抓取終端機伺服器電腦本機群組是否存在於遠端桌面授權伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9f96c-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f96c-110">語法</span><span class="sxs-lookup"><span data-stu-id="9f96c-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="9f96c-111">參數</span><span class="sxs-lookup"><span data-stu-id="9f96c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f96c-112">*存在* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9f96c-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f96c-113">指出終端機伺服器電腦本機群組是否存在的布林值。</span><span class="sxs-lookup"><span data-stu-id="9f96c-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f96c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f96c-114">Return value</span></span>

<span data-ttu-id="9f96c-115">傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="9f96c-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="9f96c-116">**Windows server 2008 R2 和 Windows server 2008：** 如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="9f96c-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9f96c-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="9f96c-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9f96c-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="9f96c-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f96c-119">備註</span><span class="sxs-lookup"><span data-stu-id="9f96c-119">Remarks</span></span>

<span data-ttu-id="9f96c-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9f96c-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9f96c-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9f96c-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f96c-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9f96c-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f96c-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9f96c-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f96c-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="9f96c-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f96c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f96c-125">Requirements</span></span>



| <span data-ttu-id="9f96c-126">需求</span><span class="sxs-lookup"><span data-stu-id="9f96c-126">Requirement</span></span> | <span data-ttu-id="9f96c-127">值</span><span class="sxs-lookup"><span data-stu-id="9f96c-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f96c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f96c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f96c-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f96c-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9f96c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f96c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f96c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f96c-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9f96c-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9f96c-132">End of client support</span></span><br/>    | <span data-ttu-id="9f96c-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f96c-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9f96c-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9f96c-134">End of server support</span></span><br/>    | <span data-ttu-id="9f96c-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f96c-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="9f96c-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f96c-136">Namespace</span></span><br/>                | <span data-ttu-id="9f96c-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9f96c-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9f96c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9f96c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f96c-139"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f96c-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f96c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9f96c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f96c-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f96c-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f96c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f96c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f96c-143">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="9f96c-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

