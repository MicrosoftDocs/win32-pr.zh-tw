---
title: Win32_TSLicenseServer 類別的 IsLSRegisteredToSCP 方法
description: 抓取是否在 Active Directory Domain Services 中將遠端桌面授權伺服器註冊為服務連接點。
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- IsLSRegisteredToSCP 方法遠端桌面服務
- IsLSRegisteredToSCP 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSRegisteredToSCP 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b203ff580c5ff8871d023c7f349626acdd693f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685579"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="3ed70-106">Win32 TSLicenseServer 類別的 IsLSRegisteredToSCP 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3ed70-106">IsLSRegisteredToSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="3ed70-107">抓取是否在 Active Directory Domain Services 中將遠端桌面授權伺服器註冊為服務連接點。</span><span class="sxs-lookup"><span data-stu-id="3ed70-107">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed70-108">語法</span><span class="sxs-lookup"><span data-stu-id="3ed70-108">Syntax</span></span>


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a><span data-ttu-id="3ed70-109">參數</span><span class="sxs-lookup"><span data-stu-id="3ed70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed70-110">*已註冊* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ed70-110">*Registered* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed70-111">布林值，指出是否在 Active Directory Domain Services 中將遠端桌面授權伺服器註冊為服務連接點。</span><span class="sxs-lookup"><span data-stu-id="3ed70-111">Boolean value that indicates whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed70-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ed70-112">Return value</span></span>

<span data-ttu-id="3ed70-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3ed70-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3ed70-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="3ed70-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3ed70-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed70-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed70-116">備註</span><span class="sxs-lookup"><span data-stu-id="3ed70-116">Remarks</span></span>

<span data-ttu-id="3ed70-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3ed70-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3ed70-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="3ed70-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3ed70-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ed70-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3ed70-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3ed70-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3ed70-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="3ed70-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed70-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ed70-122">Requirements</span></span>



| <span data-ttu-id="3ed70-123">需求</span><span class="sxs-lookup"><span data-stu-id="3ed70-123">Requirement</span></span> | <span data-ttu-id="3ed70-124">值</span><span class="sxs-lookup"><span data-stu-id="3ed70-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed70-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ed70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed70-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ed70-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3ed70-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ed70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed70-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ed70-128">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="3ed70-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ed70-129">Namespace</span></span><br/>                | <span data-ttu-id="3ed70-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3ed70-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3ed70-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed70-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed70-132"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed70-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ed70-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed70-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed70-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed70-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed70-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ed70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed70-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="3ed70-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

