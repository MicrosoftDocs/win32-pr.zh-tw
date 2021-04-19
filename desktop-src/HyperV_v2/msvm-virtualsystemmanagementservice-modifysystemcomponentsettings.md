---
description: 修改一般系統元件設定。
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Msvm_VirtualSystemManagementService 類別的 ModifySystemComponentSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970957"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1cefc-103">Msvm VirtualSystemManagementService 類別的 ModifySystemComponentSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1cefc-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1cefc-104">修改一般系統元件設定。</span><span class="sxs-lookup"><span data-stu-id="1cefc-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cefc-105">語法</span><span class="sxs-lookup"><span data-stu-id="1cefc-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1cefc-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cefc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cefc-107">*ComponentSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cefc-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cefc-108">要更新之元件設定的陣列。</span><span class="sxs-lookup"><span data-stu-id="1cefc-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="1cefc-109">*ResultingComponentSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cefc-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cefc-110">成功時，會傳回 [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) 的陣列，參考所產生的元件設定。</span><span class="sxs-lookup"><span data-stu-id="1cefc-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="1cefc-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cefc-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cefc-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1cefc-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cefc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cefc-113">Return value</span></span>

<span data-ttu-id="1cefc-114">成功時，會傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1cefc-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1cefc-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="1cefc-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="1cefc-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-117">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="1cefc-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="1cefc-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-119">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="1cefc-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-120">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="1cefc-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-121"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="1cefc-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1cefc-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="1cefc-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="1cefc-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1cefc-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="1cefc-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1cefc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cefc-126">Requirements</span></span>



| <span data-ttu-id="1cefc-127">需求</span><span class="sxs-lookup"><span data-stu-id="1cefc-127">Requirement</span></span> | <span data-ttu-id="1cefc-128">值</span><span class="sxs-lookup"><span data-stu-id="1cefc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cefc-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cefc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1cefc-130">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cefc-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1cefc-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cefc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1cefc-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1cefc-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1cefc-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="1cefc-133">Namespace</span></span><br/>                | <span data-ttu-id="1cefc-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1cefc-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1cefc-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1cefc-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cefc-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1cefc-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cefc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1cefc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cefc-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cefc-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cefc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cefc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cefc-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1cefc-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

