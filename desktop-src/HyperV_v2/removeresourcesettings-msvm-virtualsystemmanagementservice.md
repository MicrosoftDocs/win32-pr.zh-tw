---
description: 從虛擬機器設定移除虛擬資源設定。
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Msvm_VirtualSystemManagementService 類別的 RemoveResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970636"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2307f-103">Msvm VirtualSystemManagementService 類別的 RemoveResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2307f-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2307f-104">從虛擬機器設定移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="2307f-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="2307f-105">套用至目前虛擬機器設定的元件時，可能會移除作用中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2307f-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2307f-106">語法</span><span class="sxs-lookup"><span data-stu-id="2307f-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2307f-107">參數</span><span class="sxs-lookup"><span data-stu-id="2307f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2307f-108">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2307f-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2307f-109">[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)類別實例的參考陣列，其中每個實例代表要移除之虛擬機器設定內的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="2307f-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2307f-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2307f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2307f-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="2307f-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2307f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2307f-112">Return value</span></span>

<span data-ttu-id="2307f-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2307f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2307f-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2307f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2307f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="2307f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="2307f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="2307f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2307f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2307f-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2307f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="2307f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2307f-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="2307f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2307f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2307f-124">Requirements</span></span>



| <span data-ttu-id="2307f-125">需求</span><span class="sxs-lookup"><span data-stu-id="2307f-125">Requirement</span></span> | <span data-ttu-id="2307f-126">值</span><span class="sxs-lookup"><span data-stu-id="2307f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2307f-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2307f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2307f-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2307f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2307f-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2307f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2307f-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2307f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2307f-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="2307f-131">Namespace</span></span><br/>                | <span data-ttu-id="2307f-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2307f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2307f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2307f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2307f-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2307f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2307f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2307f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2307f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2307f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2307f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2307f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2307f-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="2307f-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

