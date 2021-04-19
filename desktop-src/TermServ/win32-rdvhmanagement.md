---
title: Win32_RdvhManagement 類別
description: 描述 (RDVH) 管理服務的遠端桌面虛擬主機。
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement 類別遠端桌面服務
- Win32_RdvhManagement 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967543"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="77d98-105">Win32 \_ RdvhManagement 類別</span><span class="sxs-lookup"><span data-stu-id="77d98-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="77d98-106">描述 (RDVH) 管理服務的遠端桌面虛擬主機。</span><span class="sxs-lookup"><span data-stu-id="77d98-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="77d98-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="77d98-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d98-108">語法</span><span class="sxs-lookup"><span data-stu-id="77d98-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="77d98-109">成員</span><span class="sxs-lookup"><span data-stu-id="77d98-109">Members</span></span>

<span data-ttu-id="77d98-110">**Win32 \_ RdvhManagement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="77d98-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="77d98-111">方法</span><span class="sxs-lookup"><span data-stu-id="77d98-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77d98-112">方法</span><span class="sxs-lookup"><span data-stu-id="77d98-112">Methods</span></span>

<span data-ttu-id="77d98-113">**Win32 \_ RdvhManagement** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="77d98-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="77d98-114">方法</span><span class="sxs-lookup"><span data-stu-id="77d98-114">Method</span></span>                                                                                  | <span data-ttu-id="77d98-115">描述</span><span class="sxs-lookup"><span data-stu-id="77d98-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d98-116">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="77d98-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="77d98-117">建立指定的大小上限和指定位置的使用者磁片範本。</span><span class="sxs-lookup"><span data-stu-id="77d98-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="77d98-118">所有建立的使用者磁片都會有符合範本大小上限的大小上限。</span><span class="sxs-lookup"><span data-stu-id="77d98-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="77d98-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="77d98-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="77d98-120">在 VDI 案例中起始虛擬機器的即時移轉</span><span class="sxs-lookup"><span data-stu-id="77d98-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="77d98-121">**RdvCopyBaseVmLocally**</span><span class="sxs-lookup"><span data-stu-id="77d98-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="77d98-122">在本機將基底 VM 位置複製到 RDV 主機伺服器</span><span class="sxs-lookup"><span data-stu-id="77d98-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="77d98-123">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="77d98-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="77d98-124">建立指定的大小上限和指定位置的使用者磁片範本。</span><span class="sxs-lookup"><span data-stu-id="77d98-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="77d98-125">所有建立的使用者磁片都會有符合範本大小上限的大小上限。</span><span class="sxs-lookup"><span data-stu-id="77d98-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="77d98-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="77d98-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="77d98-127">在 VDI 案例中起始虛擬機器的即時移轉。</span><span class="sxs-lookup"><span data-stu-id="77d98-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="77d98-128">**RdvSetupVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="77d98-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="77d98-129">在 VM 中設定呼叫端的許可權</span><span class="sxs-lookup"><span data-stu-id="77d98-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="77d98-130">**RdvUndoVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="77d98-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="77d98-131">在 RdvSetupVMPermissions 中還原 VM 所設定的許可權</span><span class="sxs-lookup"><span data-stu-id="77d98-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="77d98-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="77d98-132">Requirements</span></span>



| <span data-ttu-id="77d98-133">需求</span><span class="sxs-lookup"><span data-stu-id="77d98-133">Requirement</span></span> | <span data-ttu-id="77d98-134">值</span><span class="sxs-lookup"><span data-stu-id="77d98-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d98-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77d98-135">Minimum supported client</span></span><br/> | <span data-ttu-id="77d98-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="77d98-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="77d98-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77d98-137">Minimum supported server</span></span><br/> | <span data-ttu-id="77d98-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77d98-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="77d98-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="77d98-139">Namespace</span></span><br/>                | <span data-ttu-id="77d98-140">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="77d98-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="77d98-141">MOF</span><span class="sxs-lookup"><span data-stu-id="77d98-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77d98-142"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="77d98-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="77d98-143">DLL</span><span class="sxs-lookup"><span data-stu-id="77d98-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d98-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d98-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





