---
description: 設定 Vm 的初始電腦設定資料。
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Msvm_VirtualSystemManagementService 類別的 SetInitialMachineConfigurationData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689767"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="68822-103">Msvm VirtualSystemManagementService 類別的 SetInitialMachineConfigurationData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="68822-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="68822-104">設定 VM 的初始電腦設定資料。</span><span class="sxs-lookup"><span data-stu-id="68822-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="68822-105">語法</span><span class="sxs-lookup"><span data-stu-id="68822-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="68822-106">參數</span><span class="sxs-lookup"><span data-stu-id="68822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68822-107">*TargetSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68822-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68822-108">將設定 IMC 資料的虛擬電腦系統參考。</span><span class="sxs-lookup"><span data-stu-id="68822-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="68822-109">*ImcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68822-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68822-110">要設定的 IMC 資料。</span><span class="sxs-lookup"><span data-stu-id="68822-110">The IMC data to set.</span></span> <span data-ttu-id="68822-111">前四個位元組必須是陣列的長度（以位元組由大到小的順序）</span><span class="sxs-lookup"><span data-stu-id="68822-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="68822-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68822-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68822-113">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="68822-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="68822-114">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="68822-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68822-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="68822-115">Return value</span></span>

<span data-ttu-id="68822-116">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="68822-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="68822-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="68822-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68822-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="68822-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="68822-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="68822-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="68822-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="68822-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="68822-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="68822-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="68822-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="68822-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="68822-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="68822-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="68822-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="68822-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="68822-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="68822-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="68822-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="68822-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="68822-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="68822-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="68822-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="68822-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="68822-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="68822-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="68822-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="68822-130">Requirements</span></span>



| <span data-ttu-id="68822-131">需求</span><span class="sxs-lookup"><span data-stu-id="68822-131">Requirement</span></span> | <span data-ttu-id="68822-132">值</span><span class="sxs-lookup"><span data-stu-id="68822-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68822-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68822-133">Minimum supported client</span></span><br/> | <span data-ttu-id="68822-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68822-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="68822-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68822-135">Minimum supported server</span></span><br/> | <span data-ttu-id="68822-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68822-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="68822-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="68822-137">Namespace</span></span><br/>                | <span data-ttu-id="68822-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="68822-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="68822-139">MOF</span><span class="sxs-lookup"><span data-stu-id="68822-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68822-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="68822-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68822-141">DLL</span><span class="sxs-lookup"><span data-stu-id="68822-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68822-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68822-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68822-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68822-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68822-144">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="68822-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




