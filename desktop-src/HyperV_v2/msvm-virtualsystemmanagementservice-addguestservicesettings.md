---
description: 將來賓服務設定新增至虛擬系統設定。
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Msvm_VirtualSystemManagementService 類別的 AddGuestServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510998"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="8b7ad-103">Msvm VirtualSystemManagementService 類別的 AddGuestServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8b7ad-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8b7ad-104">將來賓服務設定新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="8b7ad-105">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7ad-106">語法</span><span class="sxs-lookup"><span data-stu-id="8b7ad-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8b7ad-107">參數</span><span class="sxs-lookup"><span data-stu-id="8b7ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7ad-108">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b7ad-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7ad-109">參考描述受影響設定的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8b7ad-110">*GuestServiceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b7ad-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7ad-111">包含來賓服務設定的陣列。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="8b7ad-112">*ResultingGuestServiceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b7ad-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7ad-113">成功時，會包含 [**CIM \_ SettingData**](cim-settingdata.md) 的參考，以描述所產生的來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="8b7ad-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b7ad-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7ad-115">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7ad-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b7ad-116">Return value</span></span>

<span data-ttu-id="8b7ad-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8b7ad-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8b7ad-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-119">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-120">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-121">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-122">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8b7ad-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8b7ad-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8b7ad-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b7ad-127">Requirements</span></span>



| <span data-ttu-id="8b7ad-128">需求</span><span class="sxs-lookup"><span data-stu-id="8b7ad-128">Requirement</span></span> | <span data-ttu-id="8b7ad-129">值</span><span class="sxs-lookup"><span data-stu-id="8b7ad-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7ad-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b7ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7ad-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b7ad-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8b7ad-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b7ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7ad-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8b7ad-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8b7ad-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="8b7ad-134">Namespace</span></span><br/>                | <span data-ttu-id="8b7ad-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b7ad-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b7ad-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8b7ad-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b7ad-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8b7ad-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b7ad-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8b7ad-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b7ad-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b7ad-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b7ad-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b7ad-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7ad-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="8b7ad-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

