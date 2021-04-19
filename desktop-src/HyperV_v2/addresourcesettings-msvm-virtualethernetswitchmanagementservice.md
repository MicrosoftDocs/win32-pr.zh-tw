---
description: 將資源新增至虛擬交換器設定。
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Msvm_VirtualEthernetSwitchManagementService 類別的 AddResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cc29376a03403949c57b831f40b2437ced30a51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975111"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="a1245-103">Msvm VirtualEthernetSwitchManagementService 類別的 AddResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a1245-103">AddResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="a1245-104">將資源新增至虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="a1245-104">Adds resources to a virtual switch configuration.</span></span> <span data-ttu-id="a1245-105">套用至「狀態」虛擬機器設定時，會將副作用資源新增至作用中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a1245-105">When applied to a "state" virtual machine configuration, as a side effect resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1245-106">語法</span><span class="sxs-lookup"><span data-stu-id="a1245-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a1245-107">參數</span><span class="sxs-lookup"><span data-stu-id="a1245-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1245-108">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1245-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1245-109">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))物件的參考，該物件代表受影響的虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="a1245-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a1245-110">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1245-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1245-111">字串陣列，其中包含一個 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 類別的內嵌實例，可描述要新增至虛擬交換器之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="a1245-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="a1245-112">*ResultingResourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1245-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1245-113">[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)類別實例的參考陣列，代表已新增之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="a1245-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="a1245-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1245-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1245-115">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a1245-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1245-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1245-116">Return value</span></span>

<span data-ttu-id="a1245-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a1245-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a1245-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a1245-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-119">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a1245-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-120">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="a1245-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-121">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="a1245-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-122">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="a1245-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a1245-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a1245-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="a1245-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a1245-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a1245-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a1245-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1245-127">Requirements</span></span>



| <span data-ttu-id="a1245-128">需求</span><span class="sxs-lookup"><span data-stu-id="a1245-128">Requirement</span></span> | <span data-ttu-id="a1245-129">值</span><span class="sxs-lookup"><span data-stu-id="a1245-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1245-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1245-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a1245-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1245-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1245-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1245-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a1245-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1245-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1245-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1245-134">Namespace</span></span><br/>                | <span data-ttu-id="a1245-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a1245-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1245-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a1245-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1245-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a1245-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1245-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a1245-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1245-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1245-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1245-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1245-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1245-141">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="a1245-141">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="a1245-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="a1245-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="a1245-143">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="a1245-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

