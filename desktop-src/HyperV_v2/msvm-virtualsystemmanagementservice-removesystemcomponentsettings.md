---
description: 從虛擬系統組態中移除一般元件設定。
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Msvm_VirtualSystemManagementService 類別的 RemoveSystemComponentSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973224"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a31c7-103">Msvm VirtualSystemManagementService 類別的 RemoveSystemComponentSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a31c7-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a31c7-104">從虛擬系統組態中移除一般元件設定。</span><span class="sxs-lookup"><span data-stu-id="a31c7-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a31c7-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a31c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a31c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a31c7-107">*ComponentSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a31c7-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-108">參考要移除之元件設定的 [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) 陣列。</span><span class="sxs-lookup"><span data-stu-id="a31c7-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a31c7-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a31c7-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31c7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a31c7-111">Return value</span></span>

<span data-ttu-id="a31c7-112">成功時傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a31c7-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a31c7-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a31c7-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a31c7-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-115">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="a31c7-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-116">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="a31c7-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-117">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="a31c7-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-118">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="a31c7-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-119">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a31c7-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a31c7-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-121">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="a31c7-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a31c7-122">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a31c7-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a31c7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31c7-123">Requirements</span></span>



| <span data-ttu-id="a31c7-124">需求</span><span class="sxs-lookup"><span data-stu-id="a31c7-124">Requirement</span></span> | <span data-ttu-id="a31c7-125">值</span><span class="sxs-lookup"><span data-stu-id="a31c7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31c7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a31c7-127">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31c7-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a31c7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a31c7-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a31c7-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a31c7-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="a31c7-130">Namespace</span></span><br/>                | <span data-ttu-id="a31c7-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a31c7-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a31c7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a31c7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a31c7-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a31c7-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a31c7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a31c7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a31c7-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a31c7-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a31c7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a31c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31c7-137">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a31c7-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

