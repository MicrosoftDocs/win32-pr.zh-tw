---
title: Win32_TSLicenseServer 類別的 GetLicenseServerId 方法
description: 如果伺服器目前已啟用，則抓取遠端桌面授權伺服器識別碼。
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- GetLicenseServerId 方法遠端桌面服務
- GetLicenseServerId 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，GetLicenseServerId 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384329"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="047d5-106">Win32 TSLicenseServer 類別的 GetLicenseServerId 方法 \_</span><span class="sxs-lookup"><span data-stu-id="047d5-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="047d5-107">如果伺服器目前已啟用，則抓取遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="047d5-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="047d5-108">語法</span><span class="sxs-lookup"><span data-stu-id="047d5-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="047d5-109">參數</span><span class="sxs-lookup"><span data-stu-id="047d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047d5-110">*sLicenseServerId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="047d5-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="047d5-111">遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="047d5-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="047d5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="047d5-112">Return value</span></span>

<span data-ttu-id="047d5-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="047d5-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="047d5-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="047d5-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="047d5-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="047d5-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="047d5-116">備註</span><span class="sxs-lookup"><span data-stu-id="047d5-116">Remarks</span></span>

<span data-ttu-id="047d5-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="047d5-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="047d5-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="047d5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="047d5-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="047d5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="047d5-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="047d5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="047d5-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="047d5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="047d5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="047d5-122">Requirements</span></span>



| <span data-ttu-id="047d5-123">需求</span><span class="sxs-lookup"><span data-stu-id="047d5-123">Requirement</span></span> | <span data-ttu-id="047d5-124">值</span><span class="sxs-lookup"><span data-stu-id="047d5-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="047d5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="047d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="047d5-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="047d5-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="047d5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="047d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="047d5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="047d5-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="047d5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="047d5-129">Namespace</span></span><br/>                | <span data-ttu-id="047d5-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="047d5-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="047d5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="047d5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="047d5-132"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="047d5-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="047d5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="047d5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="047d5-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="047d5-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047d5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="047d5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047d5-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="047d5-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

