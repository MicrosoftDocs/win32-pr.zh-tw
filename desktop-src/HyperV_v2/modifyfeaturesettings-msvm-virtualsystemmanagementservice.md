---
description: 修改虛擬機器乙太網路連接的目前功能設定。
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Msvm_VirtualSystemManagementService 類別的 ModifyFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319403"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="74adb-103">Msvm VirtualSystemManagementService 類別的 ModifyFeatureSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="74adb-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="74adb-104">修改虛擬機器乙太網路連接的目前功能設定。</span><span class="sxs-lookup"><span data-stu-id="74adb-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="74adb-105">語法</span><span class="sxs-lookup"><span data-stu-id="74adb-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="74adb-106">參數</span><span class="sxs-lookup"><span data-stu-id="74adb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74adb-107">*FeatureSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74adb-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74adb-108">字串的陣列，其中包含衍生自 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) 類別之類別的內嵌實例，以描述對現有乙太網路連接目前功能設定的修改。</span><span class="sxs-lookup"><span data-stu-id="74adb-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="74adb-109">每個實例的 **InstanceID** 屬性都會識別要修改的功能設定。</span><span class="sxs-lookup"><span data-stu-id="74adb-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="74adb-110">*ResultingFeatureSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="74adb-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74adb-111">[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)類別實例的參考陣列，表示修改過的功能設定。</span><span class="sxs-lookup"><span data-stu-id="74adb-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="74adb-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="74adb-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74adb-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="74adb-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74adb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="74adb-114">Return value</span></span>

<span data-ttu-id="74adb-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="74adb-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="74adb-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="74adb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="74adb-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="74adb-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="74adb-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="74adb-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="74adb-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="74adb-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="74adb-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="74adb-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="74adb-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="74adb-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="74adb-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="74adb-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="74adb-127">Requirements</span></span>



| <span data-ttu-id="74adb-128">需求</span><span class="sxs-lookup"><span data-stu-id="74adb-128">Requirement</span></span> | <span data-ttu-id="74adb-129">值</span><span class="sxs-lookup"><span data-stu-id="74adb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74adb-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74adb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74adb-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74adb-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74adb-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74adb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74adb-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74adb-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74adb-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="74adb-134">Namespace</span></span><br/>                | <span data-ttu-id="74adb-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="74adb-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74adb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="74adb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74adb-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="74adb-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74adb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="74adb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74adb-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74adb-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74adb-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74adb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74adb-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="74adb-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

