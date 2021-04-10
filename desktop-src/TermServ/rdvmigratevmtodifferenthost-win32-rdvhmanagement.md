---
title: Win32_RdvhManagement 類別的 RdvMigrateVmToDifferentHost 方法
description: 起始虛擬機器到指定主機的即時移轉。
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- RdvMigrateVmToDifferentHost 方法遠端桌面服務
- RdvMigrateVmToDifferentHost 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvMigrateVmToDifferentHost 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685906"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="c438b-106">Win32 RdvhManagement 類別的 RdvMigrateVmToDifferentHost 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c438b-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="c438b-107">起始虛擬機器到指定主機的即時移轉。</span><span class="sxs-lookup"><span data-stu-id="c438b-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="c438b-108">語法</span><span class="sxs-lookup"><span data-stu-id="c438b-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="c438b-109">參數</span><span class="sxs-lookup"><span data-stu-id="c438b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c438b-110">*VmName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c438b-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c438b-111">要遷移的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c438b-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="c438b-112">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c438b-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c438b-113">目的地主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="c438b-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c438b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c438b-114">Return value</span></span>

<span data-ttu-id="c438b-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c438b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c438b-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c438b-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c438b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c438b-117">Requirements</span></span>



| <span data-ttu-id="c438b-118">需求</span><span class="sxs-lookup"><span data-stu-id="c438b-118">Requirement</span></span> | <span data-ttu-id="c438b-119">值</span><span class="sxs-lookup"><span data-stu-id="c438b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c438b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c438b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c438b-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="c438b-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="c438b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c438b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c438b-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c438b-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="c438b-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="c438b-124">Namespace</span></span><br/>                | <span data-ttu-id="c438b-125">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c438b-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="c438b-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c438b-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c438b-127"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="c438b-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c438b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c438b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c438b-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c438b-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c438b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c438b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c438b-131">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="c438b-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





