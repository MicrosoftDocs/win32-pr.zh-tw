---
title: Win32_TerminalServiceSetting 類別的 GetRegisteredLicenseServerList 方法
description: 取得已註冊授權伺服器的清單。
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- GetRegisteredLicenseServerList 方法遠端桌面服務
- GetRegisteredLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetRegisteredLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968595"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="72356-106">Win32 TerminalServiceSetting 類別的 GetRegisteredLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="72356-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="72356-107">取得已註冊授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="72356-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="72356-108">語法</span><span class="sxs-lookup"><span data-stu-id="72356-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="72356-109">參數</span><span class="sxs-lookup"><span data-stu-id="72356-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72356-110">*RegisteredLSList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="72356-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72356-111">接收已註冊授權伺服器清單的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="72356-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="72356-112">如果沒有已註冊的授權伺服器，此陣列將會是空的。</span><span class="sxs-lookup"><span data-stu-id="72356-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72356-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="72356-113">Return value</span></span>

<span data-ttu-id="72356-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="72356-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="72356-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="72356-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="72356-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="72356-116">Requirements</span></span>



| <span data-ttu-id="72356-117">需求</span><span class="sxs-lookup"><span data-stu-id="72356-117">Requirement</span></span> | <span data-ttu-id="72356-118">值</span><span class="sxs-lookup"><span data-stu-id="72356-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72356-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72356-119">Minimum supported client</span></span><br/> | <span data-ttu-id="72356-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="72356-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="72356-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72356-121">Minimum supported server</span></span><br/> | <span data-ttu-id="72356-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72356-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="72356-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="72356-123">Namespace</span></span><br/>                | <span data-ttu-id="72356-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="72356-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="72356-125">MOF</span><span class="sxs-lookup"><span data-stu-id="72356-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72356-126"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="72356-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="72356-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72356-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72356-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72356-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72356-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72356-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72356-130">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="72356-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





