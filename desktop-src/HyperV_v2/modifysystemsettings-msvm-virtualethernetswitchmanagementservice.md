---
description: 修改虛擬交換器設定。
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Msvm_VirtualEthernetSwitchManagementService 類別的 ModifySystemSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998517"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="610aa-103">Msvm VirtualEthernetSwitchManagementService 類別的 ModifySystemSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="610aa-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="610aa-104">修改虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="610aa-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="610aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="610aa-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="610aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="610aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610aa-107">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="610aa-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610aa-108">[**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md)類別的內嵌實例，其中包含虛擬交換器的已修改部分。</span><span class="sxs-lookup"><span data-stu-id="610aa-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="610aa-109">**InstanceID** 屬性會識別要修改的虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="610aa-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="610aa-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="610aa-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610aa-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="610aa-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610aa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="610aa-112">Return value</span></span>

<span data-ttu-id="610aa-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="610aa-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="610aa-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="610aa-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="610aa-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="610aa-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="610aa-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="610aa-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="610aa-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-120"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="610aa-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="610aa-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="610aa-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="610aa-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="610aa-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="610aa-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="610aa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="610aa-125">Requirements</span></span>



| <span data-ttu-id="610aa-126">需求</span><span class="sxs-lookup"><span data-stu-id="610aa-126">Requirement</span></span> | <span data-ttu-id="610aa-127">值</span><span class="sxs-lookup"><span data-stu-id="610aa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610aa-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="610aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="610aa-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610aa-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="610aa-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="610aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="610aa-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610aa-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="610aa-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="610aa-132">Namespace</span></span><br/>                | <span data-ttu-id="610aa-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="610aa-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="610aa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="610aa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="610aa-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="610aa-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="610aa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="610aa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="610aa-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="610aa-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="610aa-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="610aa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610aa-139">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="610aa-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

