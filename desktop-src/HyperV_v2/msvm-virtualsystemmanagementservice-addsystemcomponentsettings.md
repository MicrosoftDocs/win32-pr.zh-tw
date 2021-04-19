---
description: 將一般設定新增至虛擬系統設定。
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Msvm_VirtualSystemManagementService 類別的 AddSystemComponentSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970376"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="18bcd-103">Msvm VirtualSystemManagementService 類別的 AddSystemComponentSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="18bcd-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="18bcd-104">將一般設定新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="18bcd-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bcd-105">語法</span><span class="sxs-lookup"><span data-stu-id="18bcd-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="18bcd-106">參數</span><span class="sxs-lookup"><span data-stu-id="18bcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bcd-107">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18bcd-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="18bcd-108">*ComponentSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18bcd-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bcd-109">要加入的元件設定。</span><span class="sxs-lookup"><span data-stu-id="18bcd-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="18bcd-110">*ResultingComponentSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18bcd-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18bcd-111">成功時，會參考包含所產生元件設定的 [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="18bcd-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="18bcd-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18bcd-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18bcd-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="18bcd-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bcd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="18bcd-114">Return value</span></span>

<span data-ttu-id="18bcd-115">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="18bcd-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="18bcd-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="18bcd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="18bcd-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="18bcd-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="18bcd-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="18bcd-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18bcd-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="18bcd-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="18bcd-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="18bcd-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="18bcd-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="18bcd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="18bcd-125">Requirements</span></span>



| <span data-ttu-id="18bcd-126">需求</span><span class="sxs-lookup"><span data-stu-id="18bcd-126">Requirement</span></span> | <span data-ttu-id="18bcd-127">值</span><span class="sxs-lookup"><span data-stu-id="18bcd-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18bcd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18bcd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18bcd-129">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18bcd-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="18bcd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18bcd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18bcd-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="18bcd-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="18bcd-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="18bcd-132">Namespace</span></span><br/>                | <span data-ttu-id="18bcd-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="18bcd-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18bcd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="18bcd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18bcd-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18bcd-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18bcd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="18bcd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18bcd-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18bcd-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18bcd-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18bcd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18bcd-139">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="18bcd-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

