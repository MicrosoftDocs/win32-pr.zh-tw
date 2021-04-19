---
title: Win32_TerminalServiceSetting 類別的 SetSpecifiedLicenseServerList 方法
description: 更新指定授權伺服器的清單，並取代任何現有的指定授權伺服器。
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- SetSpecifiedLicenseServerList 方法遠端桌面服務
- SetSpecifiedLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetSpecifiedLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967981"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c71dd-106">Win32 TerminalServiceSetting 類別的 SetSpecifiedLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c71dd-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c71dd-107">更新指定授權伺服器的清單，並取代任何現有的指定授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="c71dd-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71dd-108">語法</span><span class="sxs-lookup"><span data-stu-id="c71dd-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="c71dd-109">參數</span><span class="sxs-lookup"><span data-stu-id="c71dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71dd-110">*SpecifiedLSList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c71dd-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71dd-111">字串陣列，包含指定之授權伺服器的新清單。</span><span class="sxs-lookup"><span data-stu-id="c71dd-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71dd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c71dd-112">Return value</span></span>

<span data-ttu-id="c71dd-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c71dd-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c71dd-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c71dd-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71dd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c71dd-115">Requirements</span></span>



| <span data-ttu-id="c71dd-116">需求</span><span class="sxs-lookup"><span data-stu-id="c71dd-116">Requirement</span></span> | <span data-ttu-id="c71dd-117">值</span><span class="sxs-lookup"><span data-stu-id="c71dd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c71dd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c71dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c71dd-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="c71dd-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c71dd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c71dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c71dd-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c71dd-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c71dd-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="c71dd-122">Namespace</span></span><br/>                | <span data-ttu-id="c71dd-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c71dd-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c71dd-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c71dd-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c71dd-125"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c71dd-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c71dd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c71dd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71dd-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71dd-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71dd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c71dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71dd-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="c71dd-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c71dd-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c71dd-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c71dd-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c71dd-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c71dd-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c71dd-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c71dd-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c71dd-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





