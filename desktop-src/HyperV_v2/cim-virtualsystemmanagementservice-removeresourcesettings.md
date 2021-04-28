---
description: CIM_VirtualSystemManagementService 類別的 RemoveResourceSettings 方法-從虛擬系統設定移除虛擬資源設定。
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: CIM_VirtualSystemManagementService 類別的 RemoveResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112256"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="8f37b-103">CIM VirtualSystemManagementService 類別的 RemoveResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8f37b-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8f37b-104">從虛擬系統組態移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="8f37b-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="8f37b-105">套用至「目前」虛擬系統設定的元件時，可能會移除作用中虛擬系統的副作用資源。</span><span class="sxs-lookup"><span data-stu-id="8f37b-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f37b-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f37b-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8f37b-107">參數</span><span class="sxs-lookup"><span data-stu-id="8f37b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f37b-108">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f37b-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f37b-109">類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例的參考陣列，其中每個實例代表要移除之虛擬系統設定內的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="8f37b-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="8f37b-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f37b-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f37b-111">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="8f37b-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f37b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f37b-112">Return value</span></span>

<span data-ttu-id="8f37b-113">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8f37b-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8f37b-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8f37b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8f37b-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="8f37b-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8f37b-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="8f37b-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8f37b-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8f37b-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8f37b-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="8f37b-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8f37b-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8f37b-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8f37b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f37b-124">Requirements</span></span>



| <span data-ttu-id="8f37b-125">需求</span><span class="sxs-lookup"><span data-stu-id="8f37b-125">Requirement</span></span> | <span data-ttu-id="8f37b-126">值</span><span class="sxs-lookup"><span data-stu-id="8f37b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f37b-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f37b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8f37b-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8f37b-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8f37b-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f37b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8f37b-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8f37b-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8f37b-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f37b-131">Namespace</span></span><br/>                | <span data-ttu-id="8f37b-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8f37b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8f37b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8f37b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f37b-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8f37b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f37b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8f37b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f37b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f37b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f37b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f37b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f37b-138">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="8f37b-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




