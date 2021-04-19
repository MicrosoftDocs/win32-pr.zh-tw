---
title: Win32_SessionBrokerFarmAccount 類別的 DeleteEx 方法
description: Win32 \_ SessionBrokerFarmAccount 類別無法再供 Windows Server 2012 使用。 |Win32_SessionBrokerFarmAccount 類別的 DeleteEx 方法
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- DeleteEx 方法遠端桌面服務
- DeleteEx 方法遠端桌面服務，Win32_SessionBrokerFarmAccount 類別
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務，DeleteEx 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989140"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="bf27b-107">Win32 SessionBrokerFarmAccount 類別的 DeleteEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bf27b-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="bf27b-108">\[[**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)類別無法再供 Windows Server 2012 使用。\]</span><span class="sxs-lookup"><span data-stu-id="bf27b-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="bf27b-109">刪除伺服器陣列帳戶。</span><span class="sxs-lookup"><span data-stu-id="bf27b-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf27b-110">語法</span><span class="sxs-lookup"><span data-stu-id="bf27b-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="bf27b-111">參數</span><span class="sxs-lookup"><span data-stu-id="bf27b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf27b-112">*DeleteComputerObject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf27b-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf27b-113">指出是否要從 Active Directory 移除與伺服器陣列相關聯的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="bf27b-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf27b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf27b-114">Return value</span></span>

<span data-ttu-id="bf27b-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf27b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bf27b-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="bf27b-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf27b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf27b-117">Requirements</span></span>



| <span data-ttu-id="bf27b-118">需求</span><span class="sxs-lookup"><span data-stu-id="bf27b-118">Requirement</span></span> | <span data-ttu-id="bf27b-119">值</span><span class="sxs-lookup"><span data-stu-id="bf27b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf27b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf27b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf27b-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="bf27b-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bf27b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf27b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf27b-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf27b-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="bf27b-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bf27b-124">End of client support</span></span><br/>    | <span data-ttu-id="bf27b-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="bf27b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bf27b-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="bf27b-126">End of server support</span></span><br/>    | <span data-ttu-id="bf27b-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf27b-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="bf27b-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf27b-128">Namespace</span></span><br/>                | <span data-ttu-id="bf27b-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="bf27b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="bf27b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="bf27b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf27b-131"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf27b-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf27b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bf27b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf27b-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf27b-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf27b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf27b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf27b-135">**Win32 \_ SessionBrokerFarmAccount**</span><span class="sxs-lookup"><span data-stu-id="bf27b-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





