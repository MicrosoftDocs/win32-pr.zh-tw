---
description: 從虛擬交換器設定移除虛擬資源設定。
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Msvm_VirtualEthernetSwitchManagementService 類別的 RemoveResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026295"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="93ed6-103">Msvm VirtualEthernetSwitchManagementService 類別的 RemoveResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="93ed6-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="93ed6-104">從虛擬交換器設定移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="93ed6-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ed6-105">語法</span><span class="sxs-lookup"><span data-stu-id="93ed6-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="93ed6-106">參數</span><span class="sxs-lookup"><span data-stu-id="93ed6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ed6-107">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93ed6-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ed6-108">[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)類別實例的參考陣列，其中每個實例代表要移除之虛擬交換器設定內的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="93ed6-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="93ed6-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93ed6-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93ed6-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="93ed6-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ed6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="93ed6-111">Return value</span></span>

<span data-ttu-id="93ed6-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="93ed6-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="93ed6-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="93ed6-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="93ed6-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-115">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="93ed6-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-116">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="93ed6-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-117">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="93ed6-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-118">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="93ed6-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-119">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="93ed6-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="93ed6-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-121">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="93ed6-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="93ed6-122">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="93ed6-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="93ed6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="93ed6-123">Requirements</span></span>



| <span data-ttu-id="93ed6-124">需求</span><span class="sxs-lookup"><span data-stu-id="93ed6-124">Requirement</span></span> | <span data-ttu-id="93ed6-125">值</span><span class="sxs-lookup"><span data-stu-id="93ed6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ed6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93ed6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93ed6-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93ed6-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93ed6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93ed6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93ed6-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93ed6-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93ed6-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="93ed6-130">Namespace</span></span><br/>                | <span data-ttu-id="93ed6-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="93ed6-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93ed6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="93ed6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ed6-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="93ed6-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ed6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="93ed6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ed6-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93ed6-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93ed6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ed6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ed6-137">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="93ed6-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="93ed6-138">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="93ed6-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="93ed6-139">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="93ed6-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

