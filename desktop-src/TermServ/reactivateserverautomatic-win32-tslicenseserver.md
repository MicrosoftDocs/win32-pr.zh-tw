---
title: Win32_TSLicenseServer 類別的 ReactivateServerAutomatic 方法
description: 使用自動連線至網際網路，重新開機遠端桌面授權伺服器。
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- ReactivateServerAutomatic 方法遠端桌面服務
- ReactivateServerAutomatic 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ReactivateServerAutomatic 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967759"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d8e85-106">Win32 TSLicenseServer 類別的 ReactivateServerAutomatic 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d8e85-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d8e85-107">使用自動連線至網際網路，重新開機遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8e85-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e85-108">語法</span><span class="sxs-lookup"><span data-stu-id="d8e85-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d8e85-109">參數</span><span class="sxs-lookup"><span data-stu-id="d8e85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e85-110">*原因* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8e85-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-111">啟用的原因。</span><span class="sxs-lookup"><span data-stu-id="d8e85-111">Reason for the activation.</span></span> <span data-ttu-id="d8e85-112">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="d8e85-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d8e85-113">0</span><span class="sxs-lookup"><span data-stu-id="d8e85-113">0</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-114">伺服器已重新部署。</span><span class="sxs-lookup"><span data-stu-id="d8e85-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-115">1</span><span class="sxs-lookup"><span data-stu-id="d8e85-115">1</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-116">憑證已損毀。</span><span class="sxs-lookup"><span data-stu-id="d8e85-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-117">2</span><span class="sxs-lookup"><span data-stu-id="d8e85-117">2</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-118">私密金鑰遭到盜用。</span><span class="sxs-lookup"><span data-stu-id="d8e85-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-119">3</span><span class="sxs-lookup"><span data-stu-id="d8e85-119">3</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-120">啟用金鑰已過期。</span><span class="sxs-lookup"><span data-stu-id="d8e85-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-121">4</span><span class="sxs-lookup"><span data-stu-id="d8e85-121">4</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-122">伺服器已升級。</span><span class="sxs-lookup"><span data-stu-id="d8e85-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d8e85-123">*ActivationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d8e85-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-124">傳回的啟用狀態可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d8e85-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d8e85-125">0</span><span class="sxs-lookup"><span data-stu-id="d8e85-125">0</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-126">啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8e85-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-127">1</span><span class="sxs-lookup"><span data-stu-id="d8e85-127">1</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-128">未啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8e85-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="d8e85-129">2</span><span class="sxs-lookup"><span data-stu-id="d8e85-129">2</span></span>
</dt> <dd>

<span data-ttu-id="d8e85-130">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d8e85-130">An unknown error occurred.</span></span> <span data-ttu-id="d8e85-131">不知道是否啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8e85-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e85-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8e85-132">Return value</span></span>

<span data-ttu-id="d8e85-133">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d8e85-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d8e85-134">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d8e85-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d8e85-135">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d8e85-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e85-136">備註</span><span class="sxs-lookup"><span data-stu-id="d8e85-136">Remarks</span></span>

<span data-ttu-id="d8e85-137">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d8e85-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d8e85-138">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d8e85-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d8e85-139">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d8e85-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d8e85-140">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d8e85-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d8e85-141">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d8e85-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e85-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8e85-142">Requirements</span></span>



| <span data-ttu-id="d8e85-143">需求</span><span class="sxs-lookup"><span data-stu-id="d8e85-143">Requirement</span></span> | <span data-ttu-id="d8e85-144">值</span><span class="sxs-lookup"><span data-stu-id="d8e85-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e85-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8e85-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e85-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="d8e85-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d8e85-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8e85-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e85-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8e85-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d8e85-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8e85-149">Namespace</span></span><br/>                | <span data-ttu-id="d8e85-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d8e85-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d8e85-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d8e85-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8e85-152"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8e85-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8e85-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e85-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8e85-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e85-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e85-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8e85-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e85-156">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="d8e85-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

