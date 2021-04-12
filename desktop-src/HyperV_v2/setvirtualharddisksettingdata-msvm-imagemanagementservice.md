---
description: 更新虛擬硬碟的設定。
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Msvm_ImageManagementService 類別的 SetVirtualHardDiskSettingData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320588"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e492a-103">Msvm ImageManagementService 類別的 SetVirtualHardDiskSettingData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e492a-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e492a-104">更新虛擬硬碟的設定。</span><span class="sxs-lookup"><span data-stu-id="e492a-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="e492a-105">語法</span><span class="sxs-lookup"><span data-stu-id="e492a-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e492a-106">參數</span><span class="sxs-lookup"><span data-stu-id="e492a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e492a-107">*VirtualDiskSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e492a-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e492a-108">[**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)類別的字串表示，這個類別會指定要更新的虛擬硬碟，以及包含新的設定資料。</span><span class="sxs-lookup"><span data-stu-id="e492a-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="e492a-109">只有 **ParentPath**、 **PhysicalSectorSize** 或 **VirtualDiskId** 屬性可以使用這個方法來更新。</span><span class="sxs-lookup"><span data-stu-id="e492a-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="e492a-110">您無法使用一個方法呼叫來更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e492a-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="e492a-111">您只能以單一方法呼叫來更新其中一個屬性。</span><span class="sxs-lookup"><span data-stu-id="e492a-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="e492a-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e492a-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e492a-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e492a-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e492a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e492a-114">Return value</span></span>

<span data-ttu-id="e492a-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e492a-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e492a-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e492a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e492a-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e492a-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e492a-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e492a-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e492a-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e492a-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e492a-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="e492a-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e492a-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e492a-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e492a-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e492a-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e492a-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="e492a-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e492a-130">備註</span><span class="sxs-lookup"><span data-stu-id="e492a-130">Remarks</span></span>

<span data-ttu-id="e492a-131">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="e492a-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e492a-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="e492a-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e492a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e492a-133">Requirements</span></span>



| <span data-ttu-id="e492a-134">需求</span><span class="sxs-lookup"><span data-stu-id="e492a-134">Requirement</span></span> | <span data-ttu-id="e492a-135">值</span><span class="sxs-lookup"><span data-stu-id="e492a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e492a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e492a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e492a-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e492a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e492a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e492a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e492a-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e492a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e492a-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="e492a-140">Namespace</span></span><br/>                | <span data-ttu-id="e492a-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e492a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e492a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e492a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e492a-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e492a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e492a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e492a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e492a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e492a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e492a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e492a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e492a-147">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="e492a-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

