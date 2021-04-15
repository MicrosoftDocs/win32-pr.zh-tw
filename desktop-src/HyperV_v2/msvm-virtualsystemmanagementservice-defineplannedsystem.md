---
description: 定義已規劃的虛擬系統。
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Msvm_VirtualSystemManagementService 類別的 DefinePlannedSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510997"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="17e01-103">Msvm VirtualSystemManagementService 類別的 DefinePlannedSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="17e01-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="17e01-104">定義已規劃的虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="17e01-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="17e01-105">未完全指定的輸入可能會以預設值填入。</span><span class="sxs-lookup"><span data-stu-id="17e01-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e01-106">語法</span><span class="sxs-lookup"><span data-stu-id="17e01-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="17e01-107">參數</span><span class="sxs-lookup"><span data-stu-id="17e01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e01-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17e01-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e01-109">虛擬系統的系統設定。</span><span class="sxs-lookup"><span data-stu-id="17e01-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-110">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17e01-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e01-111">虛擬系統的資源設定。</span><span class="sxs-lookup"><span data-stu-id="17e01-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-112">*ReferenceConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17e01-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e01-113">包含參考設定的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="17e01-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-114">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17e01-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17e01-115">包含所產生系統的 [**CIM \_**](cim-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="17e01-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17e01-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17e01-117">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="17e01-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e01-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="17e01-118">Return value</span></span>

<span data-ttu-id="17e01-119">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="17e01-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="17e01-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="17e01-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-121">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="17e01-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-122">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="17e01-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-123">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="17e01-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-124">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="17e01-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-125">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="17e01-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-126">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="17e01-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-127">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="17e01-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="17e01-128">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="17e01-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17e01-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="17e01-129">Requirements</span></span>



| <span data-ttu-id="17e01-130">需求</span><span class="sxs-lookup"><span data-stu-id="17e01-130">Requirement</span></span> | <span data-ttu-id="17e01-131">值</span><span class="sxs-lookup"><span data-stu-id="17e01-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e01-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17e01-132">Minimum supported client</span></span><br/> | <span data-ttu-id="17e01-133">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17e01-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="17e01-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17e01-134">Minimum supported server</span></span><br/> | <span data-ttu-id="17e01-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="17e01-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="17e01-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="17e01-136">Namespace</span></span><br/>                | <span data-ttu-id="17e01-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="17e01-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="17e01-138">MOF</span><span class="sxs-lookup"><span data-stu-id="17e01-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17e01-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="17e01-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17e01-140">DLL</span><span class="sxs-lookup"><span data-stu-id="17e01-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e01-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17e01-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17e01-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17e01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e01-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="17e01-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

