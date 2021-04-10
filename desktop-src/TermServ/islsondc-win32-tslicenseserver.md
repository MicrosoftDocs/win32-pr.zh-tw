---
title: Win32_TSLicenseServer 類別的 IsLSonDC 方法
description: 抓取遠端桌面授權 (RD 授權) 是否安裝在網域控制站上。
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- IsLSonDC 方法遠端桌面服務
- IsLSonDC 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSonDC 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934574"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="fdf25-106">Win32 TSLicenseServer 類別的 IsLSonDC 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fdf25-106">IsLSonDC method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="fdf25-107">抓取遠端桌面授權 (RD 授權) 是否安裝在網域控制站上。</span><span class="sxs-lookup"><span data-stu-id="fdf25-107">Retrieves whether Remote Desktop Licensing (RD Licensing) is installed on a domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf25-108">語法</span><span class="sxs-lookup"><span data-stu-id="fdf25-108">Syntax</span></span>


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a><span data-ttu-id="fdf25-109">參數</span><span class="sxs-lookup"><span data-stu-id="fdf25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf25-110">*OnDC* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fdf25-110">*OnDC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf25-111">指出 RD 授權是否安裝在網域控制站上的布林值。</span><span class="sxs-lookup"><span data-stu-id="fdf25-111">Boolean value that indicates whether RD Licensing is installed on a domain controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf25-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdf25-112">Return value</span></span>

<span data-ttu-id="fdf25-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="fdf25-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fdf25-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="fdf25-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fdf25-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="fdf25-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf25-116">備註</span><span class="sxs-lookup"><span data-stu-id="fdf25-116">Remarks</span></span>

<span data-ttu-id="fdf25-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="fdf25-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fdf25-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fdf25-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fdf25-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fdf25-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fdf25-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fdf25-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fdf25-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="fdf25-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf25-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdf25-122">Requirements</span></span>



| <span data-ttu-id="fdf25-123">需求</span><span class="sxs-lookup"><span data-stu-id="fdf25-123">Requirement</span></span> | <span data-ttu-id="fdf25-124">值</span><span class="sxs-lookup"><span data-stu-id="fdf25-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf25-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdf25-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf25-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="fdf25-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fdf25-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdf25-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf25-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdf25-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fdf25-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdf25-129">Namespace</span></span><br/>                | <span data-ttu-id="fdf25-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fdf25-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fdf25-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fdf25-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdf25-132"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdf25-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdf25-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf25-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf25-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdf25-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf25-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdf25-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf25-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="fdf25-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

