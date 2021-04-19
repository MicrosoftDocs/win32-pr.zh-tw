---
description: 升級虛擬系統。
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Msvm_VirtualSystemManagementService 類別的 UpgradeSystemVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972175"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6f40c-103">Msvm VirtualSystemManagementService 類別的 UpgradeSystemVersion 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6f40c-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6f40c-104">升級虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="6f40c-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="6f40c-105">套用至「目前」虛擬系統組態的系統設定時</span><span class="sxs-lookup"><span data-stu-id="6f40c-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="6f40c-106">語法</span><span class="sxs-lookup"><span data-stu-id="6f40c-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6f40c-107">參數</span><span class="sxs-lookup"><span data-stu-id="6f40c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f40c-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f40c-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f40c-109">CIM 系統類型的 [**參考 \_**](cim-computersystem.md) ，代表要升級的虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="6f40c-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="6f40c-110">*UpgradeSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f40c-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f40c-111">升級設定資料。</span><span class="sxs-lookup"><span data-stu-id="6f40c-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="6f40c-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f40c-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f40c-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="6f40c-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f40c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f40c-114">Return value</span></span>

<span data-ttu-id="6f40c-115">成功時，會傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6f40c-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6f40c-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6f40c-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6f40c-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="6f40c-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="6f40c-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="6f40c-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="6f40c-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="6f40c-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6f40c-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="6f40c-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="6f40c-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6f40c-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="6f40c-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6f40c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f40c-127">Requirements</span></span>



| <span data-ttu-id="6f40c-128">需求</span><span class="sxs-lookup"><span data-stu-id="6f40c-128">Requirement</span></span> | <span data-ttu-id="6f40c-129">值</span><span class="sxs-lookup"><span data-stu-id="6f40c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f40c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f40c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6f40c-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f40c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6f40c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f40c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6f40c-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6f40c-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6f40c-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f40c-134">Namespace</span></span><br/>                | <span data-ttu-id="6f40c-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f40c-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f40c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6f40c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f40c-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6f40c-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f40c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6f40c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f40c-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f40c-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f40c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f40c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f40c-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6f40c-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

