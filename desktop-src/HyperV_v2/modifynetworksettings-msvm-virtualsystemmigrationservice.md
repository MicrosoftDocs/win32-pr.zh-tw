---
description: 修改虛擬系統移轉服務的遷移網路子網。
ms.assetid: 54ea230a-cda9-4fff-8f79-88f2922b2b15
title: Msvm_VirtualSystemMigrationService 類別的 ModifyNetworkSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b57cd3ee594bda704c1bd3b6c344c90eb6a1f7fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944768"
---
# <a name="modifynetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="41145-103">Msvm VirtualSystemMigrationService 類別的 ModifyNetworkSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="41145-103">ModifyNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="41145-104">修改虛擬系統移轉服務的遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="41145-104">Modifies migration network subnets of the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="41145-105">語法</span><span class="sxs-lookup"><span data-stu-id="41145-105">Syntax</span></span>


```mof
uint32 ModifyNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="41145-106">參數</span><span class="sxs-lookup"><span data-stu-id="41145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41145-107">*NetworkSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41145-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41145-108">包含遷移網路設定之 [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) 類別的內嵌實例陣列。</span><span class="sxs-lookup"><span data-stu-id="41145-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="41145-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41145-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41145-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="41145-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41145-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="41145-111">Return value</span></span>

<span data-ttu-id="41145-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41145-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="41145-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="41145-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41145-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="41145-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="41145-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="41145-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="41145-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="41145-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="41145-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="41145-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="41145-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="41145-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="41145-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="41145-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="41145-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="41145-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="41145-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="41145-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="41145-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="41145-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="41145-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="41145-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="41145-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="41145-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="41145-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="41145-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="41145-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="41145-126">Requirements</span></span>



| <span data-ttu-id="41145-127">需求</span><span class="sxs-lookup"><span data-stu-id="41145-127">Requirement</span></span> | <span data-ttu-id="41145-128">值</span><span class="sxs-lookup"><span data-stu-id="41145-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41145-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41145-129">Minimum supported client</span></span><br/> | <span data-ttu-id="41145-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41145-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41145-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41145-131">Minimum supported server</span></span><br/> | <span data-ttu-id="41145-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41145-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41145-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="41145-133">Namespace</span></span><br/>                | <span data-ttu-id="41145-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="41145-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41145-135">MOF</span><span class="sxs-lookup"><span data-stu-id="41145-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41145-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="41145-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41145-137">DLL</span><span class="sxs-lookup"><span data-stu-id="41145-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41145-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41145-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41145-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41145-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41145-140">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="41145-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="41145-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="41145-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="41145-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="41145-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

