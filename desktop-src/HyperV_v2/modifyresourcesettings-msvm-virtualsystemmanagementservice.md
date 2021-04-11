---
description: 修改虛擬資源設定。
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Msvm_VirtualSystemManagementService 類別的 ModifyResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 872e81926f717671b741a89c9bf954e452803b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850947"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5bc4c-103">Msvm VirtualSystemManagementService 類別的 ModifyResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5bc4c-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5bc4c-104">修改虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="5bc4c-105">套用至目前虛擬機器設定的元件時，可能會修改作用中虛擬機器的資源。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc4c-106">語法</span><span class="sxs-lookup"><span data-stu-id="5bc4c-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5bc4c-107">參數</span><span class="sxs-lookup"><span data-stu-id="5bc4c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc4c-108">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bc4c-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc4c-109">字串陣列，其中包含衍生自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)之類別的內嵌實例，其中包含現有虛擬資源的已修改部分。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="5bc4c-110">每個實例的 **InstanceID** 屬性會識別要修改的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="5bc4c-111">*ResultingResourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bc4c-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc4c-112">從 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 衍生的物件之實例的參考陣列，代表已修改之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="5bc4c-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bc4c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc4c-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc4c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bc4c-115">Return value</span></span>

<span data-ttu-id="5bc4c-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5bc4c-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5bc4c-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-122">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-123"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="5bc4c-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-124">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-125">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-126">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5bc4c-127">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="5bc4c-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5bc4c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bc4c-128">Requirements</span></span>



| <span data-ttu-id="5bc4c-129">需求</span><span class="sxs-lookup"><span data-stu-id="5bc4c-129">Requirement</span></span> | <span data-ttu-id="5bc4c-130">值</span><span class="sxs-lookup"><span data-stu-id="5bc4c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc4c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bc4c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc4c-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bc4c-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5bc4c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bc4c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc4c-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bc4c-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5bc4c-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="5bc4c-135">Namespace</span></span><br/>                | <span data-ttu-id="5bc4c-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5bc4c-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5bc4c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5bc4c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bc4c-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5bc4c-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bc4c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc4c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc4c-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bc4c-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5bc4c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bc4c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc4c-142">**ModifyVirtualSystemResources (V1)**</span><span class="sxs-lookup"><span data-stu-id="5bc4c-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="5bc4c-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="5bc4c-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

