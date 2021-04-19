---
description: 從虛擬機器乙太網路連接移除功能設定。
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Msvm_VirtualSystemManagementService 類別的 RemoveFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975354"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="742ae-103">Msvm VirtualSystemManagementService 類別的 RemoveFeatureSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="742ae-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="742ae-104">從虛擬機器乙太網路連接移除功能設定。</span><span class="sxs-lookup"><span data-stu-id="742ae-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="742ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="742ae-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="742ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="742ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="742ae-107">*FeatureSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="742ae-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="742ae-108">字串的陣列，其中包含衍生自 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) 類別之類別的內嵌實例，此類別會定義要移除的功能設定。</span><span class="sxs-lookup"><span data-stu-id="742ae-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="742ae-109">每個實例的 **InstanceID** 屬性都會識別要移除的功能設定。</span><span class="sxs-lookup"><span data-stu-id="742ae-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="742ae-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="742ae-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="742ae-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="742ae-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="742ae-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="742ae-112">Return value</span></span>

<span data-ttu-id="742ae-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="742ae-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="742ae-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="742ae-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="742ae-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="742ae-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="742ae-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="742ae-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="742ae-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="742ae-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="742ae-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="742ae-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="742ae-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="742ae-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="742ae-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="742ae-124">Requirements</span></span>



| <span data-ttu-id="742ae-125">需求</span><span class="sxs-lookup"><span data-stu-id="742ae-125">Requirement</span></span> | <span data-ttu-id="742ae-126">值</span><span class="sxs-lookup"><span data-stu-id="742ae-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742ae-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="742ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="742ae-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="742ae-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="742ae-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="742ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="742ae-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="742ae-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="742ae-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="742ae-131">Namespace</span></span><br/>                | <span data-ttu-id="742ae-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="742ae-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="742ae-133">MOF</span><span class="sxs-lookup"><span data-stu-id="742ae-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="742ae-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="742ae-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="742ae-135">DLL</span><span class="sxs-lookup"><span data-stu-id="742ae-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="742ae-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="742ae-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="742ae-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="742ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742ae-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="742ae-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

