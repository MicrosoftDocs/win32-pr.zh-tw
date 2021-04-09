---
title: Win32_TSLicenseServer 類別的 DeactivateServer 方法
description: 使用透過電話收到的確認碼來停用遠端桌面授權伺服器。
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- DeactivateServer 方法遠端桌面服務
- DeactivateServer 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，DeactivateServer 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934007"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6b954-106">Win32 TSLicenseServer 類別的 DeactivateServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6b954-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6b954-107">使用透過電話收到的確認碼來停用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="6b954-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b954-108">語法</span><span class="sxs-lookup"><span data-stu-id="6b954-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6b954-109">參數</span><span class="sxs-lookup"><span data-stu-id="6b954-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b954-110">*sConfirmCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b954-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b954-111">確認碼。</span><span class="sxs-lookup"><span data-stu-id="6b954-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="6b954-112">*ActivationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6b954-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b954-113">傳回的啟用狀態可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="6b954-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="6b954-114">0</span><span class="sxs-lookup"><span data-stu-id="6b954-114">0</span></span>
</dt> <dd>

<span data-ttu-id="6b954-115">啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="6b954-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="6b954-116">1</span><span class="sxs-lookup"><span data-stu-id="6b954-116">1</span></span>
</dt> <dd>

<span data-ttu-id="6b954-117">未啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="6b954-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="6b954-118">2</span><span class="sxs-lookup"><span data-stu-id="6b954-118">2</span></span>
</dt> <dd>

<span data-ttu-id="6b954-119">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6b954-119">An unknown error occurred.</span></span> <span data-ttu-id="6b954-120">不知道是否啟用遠端桌面服務授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="6b954-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b954-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b954-121">Return value</span></span>

<span data-ttu-id="6b954-122">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6b954-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6b954-123">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6b954-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6b954-124">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6b954-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b954-125">備註</span><span class="sxs-lookup"><span data-stu-id="6b954-125">Remarks</span></span>

<span data-ttu-id="6b954-126">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6b954-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6b954-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6b954-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6b954-128">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6b954-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6b954-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6b954-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6b954-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6b954-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b954-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b954-131">Requirements</span></span>



| <span data-ttu-id="6b954-132">需求</span><span class="sxs-lookup"><span data-stu-id="6b954-132">Requirement</span></span> | <span data-ttu-id="6b954-133">值</span><span class="sxs-lookup"><span data-stu-id="6b954-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b954-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b954-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6b954-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="6b954-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6b954-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b954-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6b954-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b954-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6b954-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="6b954-138">Namespace</span></span><br/>                | <span data-ttu-id="6b954-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6b954-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6b954-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6b954-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b954-141"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b954-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b954-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6b954-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b954-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b954-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b954-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b954-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b954-145">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="6b954-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

