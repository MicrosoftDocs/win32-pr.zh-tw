---
description: 將乙太網路功能設定新增至虛擬機器 Ethernet 連接的設定。
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Msvm_VirtualSystemManagementService 類別的 AddFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319200"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="4a275-103">Msvm VirtualSystemManagementService 類別的 AddFeatureSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4a275-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4a275-104">將乙太網路功能設定新增至虛擬機器 Ethernet 連接的設定。</span><span class="sxs-lookup"><span data-stu-id="4a275-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a275-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a275-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4a275-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a275-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a275-107">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a275-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a275-108">參考 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 類別的實例，該類別代表受影響的乙太網路連接。</span><span class="sxs-lookup"><span data-stu-id="4a275-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="4a275-109">*FeatureSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a275-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a275-110">字串陣列，其中包含一個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) 類別的內嵌實例，其中描述要加入至連線設定的功能設定。</span><span class="sxs-lookup"><span data-stu-id="4a275-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4a275-111">*ResultingFeatureSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a275-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a275-112">[**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)類別實例的參考陣列，代表已加入的功能設定。</span><span class="sxs-lookup"><span data-stu-id="4a275-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="4a275-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a275-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a275-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="4a275-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a275-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a275-115">Return value</span></span>

<span data-ttu-id="4a275-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4a275-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4a275-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="4a275-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="4a275-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="4a275-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="4a275-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="4a275-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4a275-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="4a275-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="4a275-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4a275-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="4a275-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4a275-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a275-126">Requirements</span></span>



| <span data-ttu-id="4a275-127">需求</span><span class="sxs-lookup"><span data-stu-id="4a275-127">Requirement</span></span> | <span data-ttu-id="4a275-128">值</span><span class="sxs-lookup"><span data-stu-id="4a275-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a275-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a275-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a275-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a275-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a275-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a275-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a275-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a275-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a275-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a275-133">Namespace</span></span><br/>                | <span data-ttu-id="4a275-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4a275-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4a275-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4a275-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a275-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4a275-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a275-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4a275-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a275-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a275-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a275-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a275-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a275-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="4a275-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

