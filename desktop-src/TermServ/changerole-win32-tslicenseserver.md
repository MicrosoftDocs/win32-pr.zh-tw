---
title: Win32_TSLicenseServer 類別的 ChangeRole 方法
description: 變更遠端桌面授權伺服器的探索領域。 探索領域會決定網路上) 伺服器遠端桌面工作階段主機 (RD 工作階段主機可以自動探索授權伺服器。
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- ChangeRole 方法遠端桌面服務
- ChangeRole 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ChangeRole 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464693"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f5534-107">Win32 TSLicenseServer 類別的 ChangeRole 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f5534-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f5534-108">變更遠端桌面授權伺服器的探索領域。</span><span class="sxs-lookup"><span data-stu-id="f5534-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="f5534-109">探索領域會決定網路上) 伺服器遠端桌面工作階段主機 (RD 工作階段主機可以自動探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5534-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5534-110">語法</span><span class="sxs-lookup"><span data-stu-id="f5534-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="f5534-111">參數</span><span class="sxs-lookup"><span data-stu-id="f5534-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5534-112">*ServerRole* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5534-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5534-113">遠端桌面授權伺服器的探索領域。</span><span class="sxs-lookup"><span data-stu-id="f5534-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="f5534-114">您可以設定下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f5534-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="f5534-115">0</span><span class="sxs-lookup"><span data-stu-id="f5534-115">0</span></span>
</dt> <dd>

<span data-ttu-id="f5534-116">相同工作組中的 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5534-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="f5534-117">1</span><span class="sxs-lookup"><span data-stu-id="f5534-117">1</span></span>
</dt> <dd>

<span data-ttu-id="f5534-118">相同網域中 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5534-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="f5534-119">您必須以網域系統管理員的身分登入，才能設定此值。</span><span class="sxs-lookup"><span data-stu-id="f5534-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="f5534-120">2</span><span class="sxs-lookup"><span data-stu-id="f5534-120">2</span></span>
</dt> <dd>

<span data-ttu-id="f5534-121">相同樹系中的多個網域 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5534-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="f5534-122">您必須以企業系統管理員的身分登入，才能設定此值。</span><span class="sxs-lookup"><span data-stu-id="f5534-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5534-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5534-123">Return value</span></span>

<span data-ttu-id="f5534-124">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f5534-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f5534-125">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f5534-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f5534-126">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f5534-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5534-127">備註</span><span class="sxs-lookup"><span data-stu-id="f5534-127">Remarks</span></span>

<span data-ttu-id="f5534-128">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f5534-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f5534-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f5534-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5534-130">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f5534-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5534-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f5534-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5534-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f5534-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5534-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5534-133">Requirements</span></span>



| <span data-ttu-id="f5534-134">需求</span><span class="sxs-lookup"><span data-stu-id="f5534-134">Requirement</span></span> | <span data-ttu-id="f5534-135">值</span><span class="sxs-lookup"><span data-stu-id="f5534-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5534-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5534-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5534-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="f5534-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f5534-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5534-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5534-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5534-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f5534-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="f5534-140">Namespace</span></span><br/>                | <span data-ttu-id="f5534-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f5534-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f5534-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f5534-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5534-143"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5534-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5534-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f5534-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5534-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5534-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5534-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5534-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5534-147">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f5534-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

