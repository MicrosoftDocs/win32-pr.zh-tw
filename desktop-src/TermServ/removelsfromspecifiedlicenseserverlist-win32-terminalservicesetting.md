---
title: Win32_TerminalServiceSetting 類別的 RemoveLSFromSpecifiedLicenseServerList 方法
description: 從指定的授權伺服器清單中移除指定的授權伺服器。
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- RemoveLSFromSpecifiedLicenseServerList 方法遠端桌面服務
- RemoveLSFromSpecifiedLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，RemoveLSFromSpecifiedLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843584"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="26320-106">Win32 TerminalServiceSetting 類別的 RemoveLSFromSpecifiedLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="26320-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="26320-107">從指定的授權伺服器清單中移除指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="26320-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="26320-108">語法</span><span class="sxs-lookup"><span data-stu-id="26320-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="26320-109">參數</span><span class="sxs-lookup"><span data-stu-id="26320-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26320-110">*LicenseServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26320-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26320-111">要移除之授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="26320-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26320-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="26320-112">Return value</span></span>

<span data-ttu-id="26320-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="26320-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="26320-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="26320-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="26320-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="26320-115">Requirements</span></span>



| <span data-ttu-id="26320-116">需求</span><span class="sxs-lookup"><span data-stu-id="26320-116">Requirement</span></span> | <span data-ttu-id="26320-117">值</span><span class="sxs-lookup"><span data-stu-id="26320-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26320-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26320-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26320-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="26320-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="26320-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26320-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26320-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26320-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="26320-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="26320-122">Namespace</span></span><br/>                | <span data-ttu-id="26320-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="26320-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="26320-124">MOF</span><span class="sxs-lookup"><span data-stu-id="26320-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26320-125"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="26320-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="26320-126">DLL</span><span class="sxs-lookup"><span data-stu-id="26320-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26320-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26320-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26320-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26320-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26320-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="26320-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="26320-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="26320-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="26320-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="26320-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="26320-132">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="26320-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="26320-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="26320-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





