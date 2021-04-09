---
description: 當套用至 &\# 0034; 狀態&\# 0034; 虛擬系統設定時，將開機來源新增至虛擬系統設定。
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Msvm_VirtualSystemManagementService 類別的 AddBootSourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112288"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="48f85-103">Msvm VirtualSystemManagementService 類別的 AddBootSourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="48f85-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="48f85-104">在套用至「狀態」虛擬系統設定時，將開機來源新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="48f85-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f85-105">語法</span><span class="sxs-lookup"><span data-stu-id="48f85-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="48f85-106">參數</span><span class="sxs-lookup"><span data-stu-id="48f85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f85-107">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48f85-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48f85-108">包含受影響設定的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="48f85-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="48f85-109">*BootSourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48f85-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48f85-110">包含開機來源設定的陣列。</span><span class="sxs-lookup"><span data-stu-id="48f85-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="48f85-111">*ResultingBootSourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48f85-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f85-112">成功時，會傳回具有所產生開機來源設定的 [**CIM \_ SettingData**](cim-settingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="48f85-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="48f85-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48f85-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f85-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="48f85-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f85-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="48f85-115">Return value</span></span>

<span data-ttu-id="48f85-116">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="48f85-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="48f85-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="48f85-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="48f85-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="48f85-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="48f85-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="48f85-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="48f85-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="48f85-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="48f85-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="48f85-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="48f85-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="48f85-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="48f85-126">Requirements</span></span>



| <span data-ttu-id="48f85-127">需求</span><span class="sxs-lookup"><span data-stu-id="48f85-127">Requirement</span></span> | <span data-ttu-id="48f85-128">值</span><span class="sxs-lookup"><span data-stu-id="48f85-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f85-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48f85-129">Minimum supported client</span></span><br/> | <span data-ttu-id="48f85-130">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48f85-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="48f85-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48f85-131">Minimum supported server</span></span><br/> | <span data-ttu-id="48f85-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="48f85-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="48f85-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="48f85-133">Namespace</span></span><br/>                | <span data-ttu-id="48f85-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="48f85-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48f85-135">MOF</span><span class="sxs-lookup"><span data-stu-id="48f85-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48f85-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="48f85-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48f85-137">DLL</span><span class="sxs-lookup"><span data-stu-id="48f85-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f85-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48f85-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48f85-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48f85-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f85-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="48f85-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

