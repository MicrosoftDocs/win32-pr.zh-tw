---
title: Win32_RdvhManagement 類別的 RdvSetupVMPermissions 方法
description: 在虛擬機器上設定目前使用者的許可權。
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- RdvSetupVMPermissions 方法遠端桌面服務
- RdvSetupVMPermissions 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvSetupVMPermissions 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465305"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="f82e6-106">Win32 RdvhManagement 類別的 RdvSetupVMPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f82e6-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="f82e6-107">在虛擬機器上設定目前使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="f82e6-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="f82e6-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="f82e6-109">參數</span><span class="sxs-lookup"><span data-stu-id="f82e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f82e6-110">*VmName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f82e6-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f82e6-111">要設定許可權的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="f82e6-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f82e6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f82e6-112">Return value</span></span>

<span data-ttu-id="f82e6-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f82e6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f82e6-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="f82e6-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f82e6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f82e6-115">Requirements</span></span>



| <span data-ttu-id="f82e6-116">需求</span><span class="sxs-lookup"><span data-stu-id="f82e6-116">Requirement</span></span> | <span data-ttu-id="f82e6-117">值</span><span class="sxs-lookup"><span data-stu-id="f82e6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82e6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f82e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f82e6-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="f82e6-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="f82e6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f82e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f82e6-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f82e6-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="f82e6-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="f82e6-122">Namespace</span></span><br/>                | <span data-ttu-id="f82e6-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f82e6-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="f82e6-124">MOF</span><span class="sxs-lookup"><span data-stu-id="f82e6-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f82e6-125"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="f82e6-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f82e6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f82e6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f82e6-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f82e6-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f82e6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f82e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f82e6-129">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="f82e6-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





