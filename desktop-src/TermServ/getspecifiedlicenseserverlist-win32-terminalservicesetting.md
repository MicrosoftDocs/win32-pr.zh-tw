---
title: Win32_TerminalServiceSetting 類別的 GetSpecifiedLicenseServerList 方法
description: 抓取指定授權伺服器的清單。
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- GetSpecifiedLicenseServerList 方法遠端桌面服務
- GetSpecifiedLicenseServerList 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetSpecifiedLicenseServerList 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384049"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="66a1c-106">Win32 TerminalServiceSetting 類別的 GetSpecifiedLicenseServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="66a1c-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="66a1c-107">抓取指定授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="66a1c-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a1c-108">語法</span><span class="sxs-lookup"><span data-stu-id="66a1c-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="66a1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="66a1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a1c-110">*SpecifiedLSList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66a1c-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66a1c-111">接收授權伺服器清單的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="66a1c-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="66a1c-112">如果沒有授權伺服器，此陣列將會是空的。</span><span class="sxs-lookup"><span data-stu-id="66a1c-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a1c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="66a1c-113">Return value</span></span>

<span data-ttu-id="66a1c-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="66a1c-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="66a1c-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="66a1c-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a1c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="66a1c-116">Requirements</span></span>



| <span data-ttu-id="66a1c-117">需求</span><span class="sxs-lookup"><span data-stu-id="66a1c-117">Requirement</span></span> | <span data-ttu-id="66a1c-118">值</span><span class="sxs-lookup"><span data-stu-id="66a1c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a1c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66a1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66a1c-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="66a1c-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="66a1c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66a1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66a1c-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66a1c-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="66a1c-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="66a1c-123">Namespace</span></span><br/>                | <span data-ttu-id="66a1c-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="66a1c-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="66a1c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="66a1c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66a1c-126"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="66a1c-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="66a1c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66a1c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66a1c-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66a1c-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a1c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66a1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a1c-130">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="66a1c-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="66a1c-131">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="66a1c-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="66a1c-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="66a1c-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="66a1c-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="66a1c-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="66a1c-134">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="66a1c-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





