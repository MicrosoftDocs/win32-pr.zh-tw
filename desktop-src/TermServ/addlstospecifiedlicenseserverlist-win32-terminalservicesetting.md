---
title: Win32_TerminalServiceSetting 類別的 AddLSToSpecifiedLicenseServerList 方法
description: 將指定的授權伺服器新增至指定授權伺服器清單的結尾。
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- AddLSToSpecifiedLicenseServerList 方法遠端桌面服務
- AddLSToSpecifiedLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，AddLSToSpecifiedLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934131"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="40127-106">Win32 TerminalServiceSetting 類別的 AddLSToSpecifiedLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="40127-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="40127-107">將指定的授權伺服器新增至指定授權伺服器清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="40127-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="40127-108">語法</span><span class="sxs-lookup"><span data-stu-id="40127-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="40127-109">參數</span><span class="sxs-lookup"><span data-stu-id="40127-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40127-110">*LicenseServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40127-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40127-111">要新增之授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="40127-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40127-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="40127-112">Return value</span></span>

<span data-ttu-id="40127-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="40127-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="40127-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="40127-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="40127-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="40127-115">Requirements</span></span>



| <span data-ttu-id="40127-116">需求</span><span class="sxs-lookup"><span data-stu-id="40127-116">Requirement</span></span> | <span data-ttu-id="40127-117">值</span><span class="sxs-lookup"><span data-stu-id="40127-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40127-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40127-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40127-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="40127-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="40127-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40127-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40127-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40127-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="40127-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="40127-122">Namespace</span></span><br/>                | <span data-ttu-id="40127-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="40127-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="40127-124">MOF</span><span class="sxs-lookup"><span data-stu-id="40127-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40127-125"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="40127-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="40127-126">DLL</span><span class="sxs-lookup"><span data-stu-id="40127-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40127-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40127-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40127-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40127-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40127-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="40127-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="40127-130">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="40127-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="40127-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="40127-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="40127-132">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="40127-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="40127-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="40127-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





