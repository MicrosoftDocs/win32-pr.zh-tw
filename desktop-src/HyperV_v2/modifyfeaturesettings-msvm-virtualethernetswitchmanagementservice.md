---
description: 修改 Ethernet 交換器埠的功能設定。
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Msvm_VirtualEthernetSwitchManagementService 類別的 ModifyFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984561"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="72a91-103">Msvm VirtualEthernetSwitchManagementService 類別的 ModifyFeatureSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="72a91-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="72a91-104">修改 Ethernet 交換器埠的功能設定。</span><span class="sxs-lookup"><span data-stu-id="72a91-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a91-105">語法</span><span class="sxs-lookup"><span data-stu-id="72a91-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72a91-106">參數</span><span class="sxs-lookup"><span data-stu-id="72a91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72a91-107">*FeatureSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72a91-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a91-108">字串的陣列，其中包含衍生自 [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) 類別之類別的內嵌實例，以描述要修改的切換埠功能設定。</span><span class="sxs-lookup"><span data-stu-id="72a91-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="72a91-109">*ResultingFeatureSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="72a91-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72a91-110">[**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)類別實例的參考陣列，表示修改過的功能設定。</span><span class="sxs-lookup"><span data-stu-id="72a91-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="72a91-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="72a91-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72a91-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="72a91-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72a91-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="72a91-113">Return value</span></span>

<span data-ttu-id="72a91-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="72a91-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72a91-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="72a91-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="72a91-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-117">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="72a91-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="72a91-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-119">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="72a91-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-120">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="72a91-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-121"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="72a91-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="72a91-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="72a91-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="72a91-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="72a91-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="72a91-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72a91-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="72a91-126">Requirements</span></span>



| <span data-ttu-id="72a91-127">需求</span><span class="sxs-lookup"><span data-stu-id="72a91-127">Requirement</span></span> | <span data-ttu-id="72a91-128">值</span><span class="sxs-lookup"><span data-stu-id="72a91-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a91-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72a91-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72a91-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72a91-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72a91-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72a91-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72a91-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72a91-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72a91-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="72a91-133">Namespace</span></span><br/>                | <span data-ttu-id="72a91-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="72a91-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72a91-135">MOF</span><span class="sxs-lookup"><span data-stu-id="72a91-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72a91-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="72a91-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72a91-137">DLL</span><span class="sxs-lookup"><span data-stu-id="72a91-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a91-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72a91-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72a91-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72a91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a91-140">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="72a91-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="72a91-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="72a91-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="72a91-142">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="72a91-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

