---
title: Win32_TSLicenseServer 類別的 DeactivateServerAutomatic 方法
description: 透過網際網路停用遠端桌面授權伺服器。
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- DeactivateServerAutomatic 方法遠端桌面服務
- DeactivateServerAutomatic 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，DeactivateServerAutomatic 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024758"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="36b10-106">Win32 TSLicenseServer 類別的 DeactivateServerAutomatic 方法 \_</span><span class="sxs-lookup"><span data-stu-id="36b10-106">DeactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="36b10-107">透過網際網路停用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b10-107">Deactivates the Remote Desktop license server over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b10-108">語法</span><span class="sxs-lookup"><span data-stu-id="36b10-108">Syntax</span></span>


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="36b10-109">參數</span><span class="sxs-lookup"><span data-stu-id="36b10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b10-110">*ActivationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36b10-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36b10-111">傳回的啟用狀態可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="36b10-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="36b10-112">0</span><span class="sxs-lookup"><span data-stu-id="36b10-112">0</span></span>
</dt> <dd>

<span data-ttu-id="36b10-113">啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b10-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="36b10-114">1</span><span class="sxs-lookup"><span data-stu-id="36b10-114">1</span></span>
</dt> <dd>

<span data-ttu-id="36b10-115">未啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b10-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="36b10-116">2</span><span class="sxs-lookup"><span data-stu-id="36b10-116">2</span></span>
</dt> <dd>

<span data-ttu-id="36b10-117">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b10-117">An unknown error occurred.</span></span> <span data-ttu-id="36b10-118">不知道是否啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b10-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b10-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="36b10-119">Return value</span></span>

<span data-ttu-id="36b10-120">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="36b10-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="36b10-121">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="36b10-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="36b10-122">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="36b10-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="36b10-123">備註</span><span class="sxs-lookup"><span data-stu-id="36b10-123">Remarks</span></span>

<span data-ttu-id="36b10-124">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="36b10-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="36b10-125">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="36b10-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36b10-126">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="36b10-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="36b10-127">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="36b10-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36b10-128">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="36b10-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="36b10-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="36b10-129">Requirements</span></span>



| <span data-ttu-id="36b10-130">需求</span><span class="sxs-lookup"><span data-stu-id="36b10-130">Requirement</span></span> | <span data-ttu-id="36b10-131">值</span><span class="sxs-lookup"><span data-stu-id="36b10-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b10-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36b10-132">Minimum supported client</span></span><br/> | <span data-ttu-id="36b10-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="36b10-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="36b10-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36b10-134">Minimum supported server</span></span><br/> | <span data-ttu-id="36b10-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36b10-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="36b10-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="36b10-136">Namespace</span></span><br/>                | <span data-ttu-id="36b10-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="36b10-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="36b10-138">MOF</span><span class="sxs-lookup"><span data-stu-id="36b10-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36b10-139"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="36b10-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="36b10-140">DLL</span><span class="sxs-lookup"><span data-stu-id="36b10-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36b10-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36b10-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b10-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36b10-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b10-143">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="36b10-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

