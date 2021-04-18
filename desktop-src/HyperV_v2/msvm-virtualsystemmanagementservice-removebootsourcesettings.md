---
description: 從虛擬系統組態移除虛擬資源設定。
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Msvm_VirtualSystemManagementService 類別的 RemoveBootSourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2693be33d291ea5a975119a5478af580ef2bb3f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971357"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d4f52-103">Msvm VirtualSystemManagementService 類別的 RemoveBootSourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d4f52-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d4f52-104">從虛擬系統組態移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="d4f52-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="d4f52-105">套用至「目前」虛擬系統設定的元件時，可能會移除作用中虛擬系統的副作用資源。</span><span class="sxs-lookup"><span data-stu-id="d4f52-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f52-106">語法</span><span class="sxs-lookup"><span data-stu-id="d4f52-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d4f52-107">參數</span><span class="sxs-lookup"><span data-stu-id="d4f52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f52-108">*BootSourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4f52-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f52-109">參考 [**CIM \_ SettingData**](cim-settingdata.md) 陣列，其描述要移除的開機來源設定。</span><span class="sxs-lookup"><span data-stu-id="d4f52-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="d4f52-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d4f52-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f52-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d4f52-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f52-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4f52-112">Return value</span></span>

<span data-ttu-id="d4f52-113">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d4f52-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d4f52-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d4f52-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="d4f52-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="d4f52-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="d4f52-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="d4f52-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="d4f52-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d4f52-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d4f52-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="d4f52-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d4f52-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="d4f52-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d4f52-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4f52-124">Requirements</span></span>



| <span data-ttu-id="d4f52-125">需求</span><span class="sxs-lookup"><span data-stu-id="d4f52-125">Requirement</span></span> | <span data-ttu-id="d4f52-126">值</span><span class="sxs-lookup"><span data-stu-id="d4f52-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f52-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4f52-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f52-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4f52-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d4f52-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4f52-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f52-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d4f52-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d4f52-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="d4f52-131">Namespace</span></span><br/>                | <span data-ttu-id="d4f52-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d4f52-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d4f52-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d4f52-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4f52-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d4f52-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4f52-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f52-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f52-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4f52-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d4f52-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4f52-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f52-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d4f52-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

