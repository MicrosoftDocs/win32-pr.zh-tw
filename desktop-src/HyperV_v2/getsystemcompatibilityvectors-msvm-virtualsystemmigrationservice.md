---
description: 取得 \_ 可用來檢查虛擬機器 (VM) 以裝載相容性的 Msvm CompatibilityVector 實例清單。
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService：： GetSystemCompatibilityVectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943246"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="88223-103">Msvm \_ VirtualSystemMigrationService：： GetSystemCompatibilityVectors 方法</span><span class="sxs-lookup"><span data-stu-id="88223-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="88223-104">取得可用來檢查虛擬機器 (VM) 以裝載相容性的 [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) 實例清單。</span><span class="sxs-lookup"><span data-stu-id="88223-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="88223-105">語法</span><span class="sxs-lookup"><span data-stu-id="88223-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="88223-106">參數</span><span class="sxs-lookup"><span data-stu-id="88223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88223-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="88223-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88223-108">[**Msvm \_**](msvm-computersystem.md)的同機類別的參考，代表要取得其相容性向量的 VM。</span><span class="sxs-lookup"><span data-stu-id="88223-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="88223-109">如果此參數參考主控電腦系統，則 *CompatibilityVectors* 參數中所傳回的資料可以用來判斷主控電腦系統上的任何 vm 是否可以快速遷移到另一個主控電腦系統。</span><span class="sxs-lookup"><span data-stu-id="88223-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="88223-110">*CompatibilityVectors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88223-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88223-111">[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)實例的陣列，其中包含 vm 或主控電腦系統的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="88223-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88223-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="88223-112">Return value</span></span>

<span data-ttu-id="88223-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88223-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="88223-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="88223-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88223-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="88223-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="88223-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="88223-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="88223-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="88223-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="88223-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="88223-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="88223-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="88223-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="88223-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="88223-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="88223-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="88223-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="88223-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="88223-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="88223-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="88223-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="88223-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="88223-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="88223-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="88223-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="88223-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="88223-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="88223-127">備註</span><span class="sxs-lookup"><span data-stu-id="88223-127">Remarks</span></span>

<span data-ttu-id="88223-128">當虛擬機器在 VM 電腦系統上執行時， **GetSystemCompatibilityVectors** 會取得虛擬機器的相容性資訊 (vm)  () 或在主機電腦系統上執行 (時的主機) 。</span><span class="sxs-lookup"><span data-stu-id="88223-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="88223-129">用戶端的相容性資訊會保持不變，而資訊會提供方法來比較主機相容性資訊與 VM 的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="88223-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="88223-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="88223-130">Requirements</span></span>



| <span data-ttu-id="88223-131">需求</span><span class="sxs-lookup"><span data-stu-id="88223-131">Requirement</span></span> | <span data-ttu-id="88223-132">值</span><span class="sxs-lookup"><span data-stu-id="88223-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88223-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88223-133">Minimum supported client</span></span><br/> | <span data-ttu-id="88223-134">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88223-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="88223-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88223-135">Minimum supported server</span></span><br/> | <span data-ttu-id="88223-136">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88223-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88223-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="88223-137">Namespace</span></span><br/>                | <span data-ttu-id="88223-138">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="88223-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="88223-139">MOF</span><span class="sxs-lookup"><span data-stu-id="88223-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88223-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="88223-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88223-141">DLL</span><span class="sxs-lookup"><span data-stu-id="88223-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88223-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88223-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88223-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88223-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88223-144">**Msvm \_ CompatibilityVector**</span><span class="sxs-lookup"><span data-stu-id="88223-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="88223-145">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="88223-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




