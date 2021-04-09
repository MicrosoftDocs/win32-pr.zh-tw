---
description: 修改來賓服務設定。
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Msvm_VirtualSystemManagementService 類別的 ModifyGuestServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847763"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c76f1-103">Msvm VirtualSystemManagementService 類別的 ModifyGuestServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c76f1-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c76f1-104">修改來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="c76f1-104">Modifies guest service settings.</span></span>

<span data-ttu-id="c76f1-105">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="c76f1-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76f1-106">語法</span><span class="sxs-lookup"><span data-stu-id="c76f1-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c76f1-107">參數</span><span class="sxs-lookup"><span data-stu-id="c76f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76f1-108">*GuestServiceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c76f1-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76f1-109">陣列，其中包含新的來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="c76f1-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="c76f1-110">*ResultingGuestServiceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c76f1-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c76f1-111">成功時，contiains 可參考所產生之來賓服務設定的 [**CIM \_ SettingData**](cim-settingdata.md) 陣列。</span><span class="sxs-lookup"><span data-stu-id="c76f1-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="c76f1-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c76f1-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c76f1-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c76f1-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76f1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c76f1-114">Return value</span></span>

<span data-ttu-id="c76f1-115">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="c76f1-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c76f1-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c76f1-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c76f1-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="c76f1-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="c76f1-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="c76f1-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c76f1-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="c76f1-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c76f1-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="c76f1-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="c76f1-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c76f1-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="c76f1-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c76f1-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c76f1-127">Requirements</span></span>



| <span data-ttu-id="c76f1-128">需求</span><span class="sxs-lookup"><span data-stu-id="c76f1-128">Requirement</span></span> | <span data-ttu-id="c76f1-129">值</span><span class="sxs-lookup"><span data-stu-id="c76f1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c76f1-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c76f1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c76f1-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c76f1-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c76f1-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c76f1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c76f1-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c76f1-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c76f1-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="c76f1-134">Namespace</span></span><br/>                | <span data-ttu-id="c76f1-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c76f1-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c76f1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c76f1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c76f1-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c76f1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c76f1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c76f1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c76f1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c76f1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c76f1-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c76f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76f1-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="c76f1-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

