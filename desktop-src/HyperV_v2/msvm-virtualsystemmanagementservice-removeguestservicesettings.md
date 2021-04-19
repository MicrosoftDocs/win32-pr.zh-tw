---
description: 從虛擬系統組態中移除來賓服務設定。
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Msvm_VirtualSystemManagementService 類別的 RemoveGuestServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970375"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bbedb-103">Msvm VirtualSystemManagementService 類別的 RemoveGuestServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bbedb-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bbedb-104">從虛擬系統組態中移除來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="bbedb-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="bbedb-105">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="bbedb-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbedb-106">語法</span><span class="sxs-lookup"><span data-stu-id="bbedb-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bbedb-107">參數</span><span class="sxs-lookup"><span data-stu-id="bbedb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbedb-108">*GuestServiceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbedb-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbedb-109">參考 [**CIM \_ SettingData**](cim-settingdata.md) 陣列，其描述要移除的來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="bbedb-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="bbedb-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bbedb-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbedb-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bbedb-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbedb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbedb-112">Return value</span></span>

<span data-ttu-id="bbedb-113">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="bbedb-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bbedb-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bbedb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="bbedb-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="bbedb-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="bbedb-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="bbedb-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="bbedb-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bbedb-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="bbedb-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="bbedb-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bbedb-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="bbedb-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bbedb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbedb-124">Requirements</span></span>



| <span data-ttu-id="bbedb-125">需求</span><span class="sxs-lookup"><span data-stu-id="bbedb-125">Requirement</span></span> | <span data-ttu-id="bbedb-126">值</span><span class="sxs-lookup"><span data-stu-id="bbedb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbedb-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbedb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bbedb-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbedb-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bbedb-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbedb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bbedb-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bbedb-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bbedb-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="bbedb-131">Namespace</span></span><br/>                | <span data-ttu-id="bbedb-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="bbedb-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bbedb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bbedb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbedb-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bbedb-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbedb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bbedb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbedb-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbedb-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbedb-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbedb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbedb-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bbedb-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

