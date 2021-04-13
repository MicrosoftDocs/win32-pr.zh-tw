---
title: Win32_TSLicenseServer 類別的 IsSecureAccessAllowed 方法
description: 抓取是否允許遠端桌面工作階段主機 (RD 工作階段主機) 伺服器要求遠端桌面服務 RDS \ 160 的 (用戶端存取授權從遠端桌面授權伺服器) 的 Cal。
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- IsSecureAccessAllowed 方法遠端桌面服務
- IsSecureAccessAllowed 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsSecureAccessAllowed 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508551"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="eb13a-106">Win32 TSLicenseServer 類別的 IsSecureAccessAllowed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eb13a-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="eb13a-107">抓取遠端桌面工作階段主機 (RD 工作階段主機) server 是否允許從遠端桌面授權伺服器遠端桌面服務 RDS Cal (要求) 用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="eb13a-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb13a-108">語法</span><span class="sxs-lookup"><span data-stu-id="eb13a-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="eb13a-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb13a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb13a-110">*tsname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb13a-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb13a-111">RD 工作階段主機伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb13a-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="eb13a-112">*允許* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb13a-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb13a-113">指出 RD 工作階段主機伺服器是否允許從授權伺服器要求 RDS Cal 的布林值。</span><span class="sxs-lookup"><span data-stu-id="eb13a-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb13a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb13a-114">Return value</span></span>

<span data-ttu-id="eb13a-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="eb13a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eb13a-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="eb13a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eb13a-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="eb13a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb13a-118">備註</span><span class="sxs-lookup"><span data-stu-id="eb13a-118">Remarks</span></span>

<span data-ttu-id="eb13a-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="eb13a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eb13a-120">傳回的值是根據「授權伺服器安全性群組」群組原則設定，以及遠端桌面授權伺服器上終端機伺服器電腦本機群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="eb13a-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="eb13a-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="eb13a-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eb13a-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="eb13a-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eb13a-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="eb13a-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eb13a-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="eb13a-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb13a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb13a-125">Requirements</span></span>



| <span data-ttu-id="eb13a-126">需求</span><span class="sxs-lookup"><span data-stu-id="eb13a-126">Requirement</span></span> | <span data-ttu-id="eb13a-127">值</span><span class="sxs-lookup"><span data-stu-id="eb13a-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb13a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb13a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eb13a-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="eb13a-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="eb13a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb13a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eb13a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb13a-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="eb13a-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb13a-132">Namespace</span></span><br/>                | <span data-ttu-id="eb13a-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="eb13a-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="eb13a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eb13a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb13a-135"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb13a-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb13a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eb13a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb13a-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb13a-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb13a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb13a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb13a-139">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="eb13a-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="eb13a-140">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="eb13a-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

