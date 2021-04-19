---
description: 修改虛擬交換器的資源設定。
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Msvm_VirtualEthernetSwitchManagementService 類別的 ModifyResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979947"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="628d4-103">Msvm VirtualEthernetSwitchManagementService 類別的 ModifyResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="628d4-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="628d4-104">修改虛擬交換器的資源設定。</span><span class="sxs-lookup"><span data-stu-id="628d4-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="628d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="628d4-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="628d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="628d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="628d4-107">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="628d4-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628d4-108">字串陣列，其中包含衍生自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)之類別的內嵌實例，其中包含現有虛擬資源的已修改部分。</span><span class="sxs-lookup"><span data-stu-id="628d4-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="628d4-109">每個實例的 **InstanceID** 屬性會識別要修改的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="628d4-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="628d4-110">*ResultingResourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="628d4-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="628d4-111">從 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 衍生的物件之實例的參考陣列，代表已修改之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="628d4-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="628d4-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="628d4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="628d4-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="628d4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="628d4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="628d4-114">Return value</span></span>

<span data-ttu-id="628d4-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="628d4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="628d4-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="628d4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="628d4-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="628d4-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="628d4-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="628d4-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="628d4-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="628d4-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="628d4-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="628d4-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="628d4-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="628d4-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="628d4-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="628d4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="628d4-127">Requirements</span></span>



| <span data-ttu-id="628d4-128">需求</span><span class="sxs-lookup"><span data-stu-id="628d4-128">Requirement</span></span> | <span data-ttu-id="628d4-129">值</span><span class="sxs-lookup"><span data-stu-id="628d4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="628d4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="628d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="628d4-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="628d4-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="628d4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="628d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="628d4-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="628d4-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="628d4-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="628d4-134">Namespace</span></span><br/>                | <span data-ttu-id="628d4-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="628d4-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="628d4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="628d4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="628d4-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="628d4-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="628d4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="628d4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="628d4-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="628d4-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="628d4-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="628d4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628d4-141">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="628d4-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="628d4-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="628d4-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="628d4-143">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="628d4-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

