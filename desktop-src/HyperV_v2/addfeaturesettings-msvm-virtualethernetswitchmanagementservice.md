---
description: 將功能設定新增至乙太網路交換器埠的設定。
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Msvm_VirtualEthernetSwitchManagementService 類別的 AddFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944303"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="cbb3c-103">Msvm VirtualEthernetSwitchManagementService 類別的 AddFeatureSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cbb3c-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="cbb3c-104">將功能設定新增至乙太網路交換器埠的設定。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb3c-105">語法</span><span class="sxs-lookup"><span data-stu-id="cbb3c-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cbb3c-106">參數</span><span class="sxs-lookup"><span data-stu-id="cbb3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb3c-107">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb3c-108">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))衍生類別的參考，代表受影響的乙太網路交換器埠或乙太網路交換器設定。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cbb3c-109">*FeatureSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb3c-110">字串的陣列，其中包含衍生自 [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) 類別之類別的內嵌實例，以描述要新增至交換器埠設定的功能設定。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cbb3c-111">*ResultingFeatureSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb3c-112">[**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)類別實例的參考陣列，代表已加入的功能設定。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="cbb3c-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb3c-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb3c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbb3c-115">Return value</span></span>

<span data-ttu-id="cbb3c-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cbb3c-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cbb3c-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="cbb3c-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="cbb3c-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cbb3c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbb3c-126">Requirements</span></span>



| <span data-ttu-id="cbb3c-127">需求</span><span class="sxs-lookup"><span data-stu-id="cbb3c-127">Requirement</span></span> | <span data-ttu-id="cbb3c-128">值</span><span class="sxs-lookup"><span data-stu-id="cbb3c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb3c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbb3c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb3c-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbb3c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbb3c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb3c-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbb3c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbb3c-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="cbb3c-133">Namespace</span></span><br/>                | <span data-ttu-id="cbb3c-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="cbb3c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbb3c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cbb3c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbb3c-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbb3c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cbb3c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb3c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbb3c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbb3c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb3c-140">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="cbb3c-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="cbb3c-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="cbb3c-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="cbb3c-142">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="cbb3c-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

