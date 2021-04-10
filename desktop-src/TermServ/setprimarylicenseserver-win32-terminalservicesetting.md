---
title: Win32_TerminalServiceSetting 類別的 SetPrimaryLicenseServer 方法
description: 將指定的授權伺服器設定為指定授權伺服器清單中的第一個專案。
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- SetPrimaryLicenseServer 方法遠端桌面服務
- SetPrimaryLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetPrimaryLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843252"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6b982-106">Win32 TerminalServiceSetting 類別的 SetPrimaryLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6b982-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6b982-107">將指定的授權伺服器設定為指定授權伺服器清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="6b982-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b982-108">語法</span><span class="sxs-lookup"><span data-stu-id="6b982-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="6b982-109">參數</span><span class="sxs-lookup"><span data-stu-id="6b982-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b982-110">*LicenseServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b982-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b982-111">授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b982-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b982-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b982-112">Return value</span></span>

<span data-ttu-id="6b982-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b982-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6b982-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="6b982-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b982-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b982-115">Requirements</span></span>



| <span data-ttu-id="6b982-116">需求</span><span class="sxs-lookup"><span data-stu-id="6b982-116">Requirement</span></span> | <span data-ttu-id="6b982-117">值</span><span class="sxs-lookup"><span data-stu-id="6b982-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b982-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b982-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b982-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6b982-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6b982-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b982-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b982-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b982-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6b982-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="6b982-122">Namespace</span></span><br/>                | <span data-ttu-id="6b982-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6b982-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6b982-124">MOF</span><span class="sxs-lookup"><span data-stu-id="6b982-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b982-125"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b982-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b982-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6b982-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b982-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b982-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b982-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b982-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b982-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="6b982-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





