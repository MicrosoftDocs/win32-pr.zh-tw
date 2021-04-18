---
title: Win32_TSLicenseServer 類別的 IsLSPublished 方法
description: 抓取 Active Directory Domain Services (AD \ 160; DS) 中是否發佈遠端桌面授權伺服器。
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- IsLSPublished 方法遠端桌面服務
- IsLSPublished 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSPublished 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968769"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="061d1-106">Win32 TSLicenseServer 類別的 IsLSPublished 方法 \_</span><span class="sxs-lookup"><span data-stu-id="061d1-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="061d1-107">抓取 Active Directory Domain Services (AD DS) 中是否發佈遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="061d1-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="061d1-108">語法</span><span class="sxs-lookup"><span data-stu-id="061d1-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="061d1-109">參數</span><span class="sxs-lookup"><span data-stu-id="061d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061d1-110">*已發佈* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="061d1-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="061d1-111">指出授權伺服器是否已在 AD DS 中發佈的布林值。</span><span class="sxs-lookup"><span data-stu-id="061d1-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061d1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="061d1-112">Return value</span></span>

<span data-ttu-id="061d1-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="061d1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="061d1-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="061d1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="061d1-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="061d1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="061d1-116">備註</span><span class="sxs-lookup"><span data-stu-id="061d1-116">Remarks</span></span>

<span data-ttu-id="061d1-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="061d1-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="061d1-118">如果授權伺服器是在 AD DS 發佈的，則遠端桌面工作階段主機 () RD 工作階段主機相同樹系中的伺服器，就會自動探索該伺服器。</span><span class="sxs-lookup"><span data-stu-id="061d1-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="061d1-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="061d1-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="061d1-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="061d1-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="061d1-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="061d1-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="061d1-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="061d1-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="061d1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="061d1-123">Requirements</span></span>



| <span data-ttu-id="061d1-124">需求</span><span class="sxs-lookup"><span data-stu-id="061d1-124">Requirement</span></span> | <span data-ttu-id="061d1-125">值</span><span class="sxs-lookup"><span data-stu-id="061d1-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="061d1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="061d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="061d1-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="061d1-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="061d1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="061d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="061d1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="061d1-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="061d1-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="061d1-130">Namespace</span></span><br/>                | <span data-ttu-id="061d1-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="061d1-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="061d1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="061d1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="061d1-133"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="061d1-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="061d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="061d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061d1-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061d1-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061d1-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="061d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061d1-137">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="061d1-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

