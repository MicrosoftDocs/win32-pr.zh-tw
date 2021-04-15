---
title: Win32_TerminalServiceSetting 類別的 EmptySpecifiedLicenseServerList 方法
description: 從指定的授權伺服器清單中移除所有授權伺服器。
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- EmptySpecifiedLicenseServerList 方法遠端桌面服務
- EmptySpecifiedLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，EmptySpecifiedLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467044"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0e251-106">Win32 TerminalServiceSetting 類別的 EmptySpecifiedLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0e251-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0e251-107">從指定的授權伺服器清單中移除所有授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e251-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e251-108">語法</span><span class="sxs-lookup"><span data-stu-id="0e251-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="0e251-109">參數</span><span class="sxs-lookup"><span data-stu-id="0e251-109">Parameters</span></span>

<span data-ttu-id="0e251-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0e251-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e251-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e251-111">Return value</span></span>

<span data-ttu-id="0e251-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0e251-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0e251-113">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e251-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e251-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e251-114">Requirements</span></span>



| <span data-ttu-id="0e251-115">需求</span><span class="sxs-lookup"><span data-stu-id="0e251-115">Requirement</span></span> | <span data-ttu-id="0e251-116">值</span><span class="sxs-lookup"><span data-stu-id="0e251-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e251-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e251-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e251-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e251-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0e251-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e251-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e251-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e251-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="0e251-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="0e251-121">Namespace</span></span><br/>                | <span data-ttu-id="0e251-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0e251-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0e251-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0e251-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e251-124"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e251-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e251-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0e251-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e251-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e251-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e251-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e251-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e251-128">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="0e251-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="0e251-129">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e251-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="0e251-130">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e251-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="0e251-131">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e251-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="0e251-132">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e251-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





