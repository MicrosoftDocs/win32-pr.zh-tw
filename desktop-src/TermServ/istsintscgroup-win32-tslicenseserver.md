---
title: Win32_TSLicenseServer 類別的 IsTSinTSCGroup 方法
description: 抓取遠端桌面工作階段主機 (RD 工作階段主機) server 是否為遠端桌面授權伺服器上終端機伺服器電腦本機群組的成員。
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- IsTSinTSCGroup 方法遠端桌面服務
- IsTSinTSCGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsTSinTSCGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509276"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="28506-106">Win32 TSLicenseServer 類別的 IsTSinTSCGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="28506-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="28506-107">抓取遠端桌面工作階段主機 (RD 工作階段主機) server 是否為遠端桌面授權伺服器上終端機伺服器電腦本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="28506-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="28506-108">語法</span><span class="sxs-lookup"><span data-stu-id="28506-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="28506-109">參數</span><span class="sxs-lookup"><span data-stu-id="28506-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28506-110">*tsname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28506-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28506-111">RD 工作階段主機伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="28506-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="28506-112">*IsMember* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28506-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28506-113">布林值，指出 RD 工作階段主機伺服器是否為終端機伺服器電腦本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="28506-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28506-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="28506-114">Return value</span></span>

<span data-ttu-id="28506-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="28506-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="28506-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="28506-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="28506-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="28506-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28506-118">備註</span><span class="sxs-lookup"><span data-stu-id="28506-118">Remarks</span></span>

<span data-ttu-id="28506-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="28506-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="28506-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="28506-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="28506-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="28506-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="28506-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="28506-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="28506-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="28506-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="28506-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="28506-124">Requirements</span></span>



| <span data-ttu-id="28506-125">需求</span><span class="sxs-lookup"><span data-stu-id="28506-125">Requirement</span></span> | <span data-ttu-id="28506-126">值</span><span class="sxs-lookup"><span data-stu-id="28506-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="28506-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28506-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28506-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="28506-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="28506-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28506-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28506-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28506-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="28506-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="28506-131">Namespace</span></span><br/>                | <span data-ttu-id="28506-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="28506-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="28506-133">MOF</span><span class="sxs-lookup"><span data-stu-id="28506-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28506-134"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="28506-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="28506-135">DLL</span><span class="sxs-lookup"><span data-stu-id="28506-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28506-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28506-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28506-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28506-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28506-138">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="28506-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

