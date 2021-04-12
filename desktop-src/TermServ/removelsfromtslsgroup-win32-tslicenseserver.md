---
title: Win32_TSLicenseServer 類別的 RemoveLSfromTSLSGroup 方法
description: 從與授權伺服器相同網域的網域控制站上的遠端桌面服務授權伺服器群組中，移除遠端桌面授權伺服器。
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- RemoveLSfromTSLSGroup 方法遠端桌面服務
- RemoveLSfromTSLSGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，RemoveLSfromTSLSGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508743"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="26fdc-106">Win32 TSLicenseServer 類別的 RemoveLSfromTSLSGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="26fdc-106">RemoveLSfromTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="26fdc-107">從與授權伺服器相同網域的網域控制站上的遠端桌面服務授權伺服器群組中，移除遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="26fdc-107">Removes the Remote Desktop license server from the Remote Desktop Services License Servers group on a domain controller in the same domain as the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="26fdc-108">語法</span><span class="sxs-lookup"><span data-stu-id="26fdc-108">Syntax</span></span>


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="26fdc-109">參數</span><span class="sxs-lookup"><span data-stu-id="26fdc-109">Parameters</span></span>

<span data-ttu-id="26fdc-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="26fdc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26fdc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="26fdc-111">Return value</span></span>

<span data-ttu-id="26fdc-112">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="26fdc-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="26fdc-113">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="26fdc-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="26fdc-114">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="26fdc-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26fdc-115">備註</span><span class="sxs-lookup"><span data-stu-id="26fdc-115">Remarks</span></span>

<span data-ttu-id="26fdc-116">您必須是 Domain Admins 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="26fdc-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="26fdc-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="26fdc-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26fdc-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="26fdc-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="26fdc-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="26fdc-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26fdc-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="26fdc-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="26fdc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="26fdc-121">Requirements</span></span>



| <span data-ttu-id="26fdc-122">需求</span><span class="sxs-lookup"><span data-stu-id="26fdc-122">Requirement</span></span> | <span data-ttu-id="26fdc-123">值</span><span class="sxs-lookup"><span data-stu-id="26fdc-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fdc-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26fdc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26fdc-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="26fdc-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="26fdc-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26fdc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26fdc-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26fdc-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="26fdc-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="26fdc-128">Namespace</span></span><br/>                | <span data-ttu-id="26fdc-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="26fdc-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="26fdc-130">MOF</span><span class="sxs-lookup"><span data-stu-id="26fdc-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26fdc-131"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="26fdc-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="26fdc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="26fdc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26fdc-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26fdc-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26fdc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26fdc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26fdc-135">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="26fdc-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

