---
description: 從虛擬系統移轉服務移除遷移網路子網。
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Msvm_VirtualSystemMigrationService 類別的 RemoveNetworkSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974122"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="07d13-103">Msvm VirtualSystemMigrationService 類別的 RemoveNetworkSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="07d13-103">RemoveNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="07d13-104">從虛擬系統移轉服務移除遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="07d13-104">Removes migration network subnets from the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d13-105">語法</span><span class="sxs-lookup"><span data-stu-id="07d13-105">Syntax</span></span>


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="07d13-106">參數</span><span class="sxs-lookup"><span data-stu-id="07d13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d13-107">*NetworkSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07d13-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d13-108">[**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md)類別的內嵌實例陣列，代表要移除的網路子網。</span><span class="sxs-lookup"><span data-stu-id="07d13-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represent the network subnets to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="07d13-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07d13-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07d13-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="07d13-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d13-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="07d13-111">Return value</span></span>

<span data-ttu-id="07d13-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="07d13-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="07d13-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="07d13-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="07d13-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="07d13-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="07d13-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="07d13-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="07d13-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="07d13-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="07d13-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="07d13-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="07d13-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="07d13-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="07d13-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="07d13-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="07d13-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="07d13-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="07d13-126">Requirements</span></span>



| <span data-ttu-id="07d13-127">需求</span><span class="sxs-lookup"><span data-stu-id="07d13-127">Requirement</span></span> | <span data-ttu-id="07d13-128">值</span><span class="sxs-lookup"><span data-stu-id="07d13-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d13-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07d13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="07d13-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d13-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="07d13-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07d13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="07d13-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d13-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07d13-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="07d13-133">Namespace</span></span><br/>                | <span data-ttu-id="07d13-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="07d13-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="07d13-135">MOF</span><span class="sxs-lookup"><span data-stu-id="07d13-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07d13-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="07d13-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07d13-137">DLL</span><span class="sxs-lookup"><span data-stu-id="07d13-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d13-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07d13-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="07d13-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07d13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d13-140">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="07d13-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="07d13-141">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="07d13-141">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="07d13-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="07d13-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

