---
description: 建立新的虛擬交換器。
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Msvm_VirtualEthernetSwitchManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850960"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="8eae9-103">Msvm VirtualEthernetSwitchManagementService 類別的 DefineSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8eae9-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="8eae9-104">建立新的虛擬交換器。</span><span class="sxs-lookup"><span data-stu-id="8eae9-104">Creates a new virtual switch.</span></span> <span data-ttu-id="8eae9-105">未指定的屬性將會填入預設值。</span><span class="sxs-lookup"><span data-stu-id="8eae9-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eae9-106">語法</span><span class="sxs-lookup"><span data-stu-id="8eae9-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8eae9-107">參數</span><span class="sxs-lookup"><span data-stu-id="8eae9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eae9-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eae9-109">[**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md)類別的內嵌實例，可用來定義要建立之虛擬交換器的屬性。</span><span class="sxs-lookup"><span data-stu-id="8eae9-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="8eae9-110">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="8eae9-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="8eae9-111">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eae9-112">[**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)類別的內嵌實例陣列，描述要在新虛擬交換器範圍中建立之交換器埠的設定。</span><span class="sxs-lookup"><span data-stu-id="8eae9-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="8eae9-113">如果指定 **Null** ，則不會建立任何資源 (的虛擬交換器，亦即沒有任何交換器埠) 。</span><span class="sxs-lookup"><span data-stu-id="8eae9-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="8eae9-114">*ReferenceConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eae9-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8eae9-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8eae9-116">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eae9-117">如果已成功建立虛擬交換器，則為代表新定義虛擬交換器之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8eae9-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="8eae9-118">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eae9-119">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8eae9-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eae9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="8eae9-120">Return value</span></span>

<span data-ttu-id="8eae9-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8eae9-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8eae9-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8eae9-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-123">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8eae9-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-124">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="8eae9-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-125">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8eae9-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-126">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="8eae9-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-127">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8eae9-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-128">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8eae9-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-129">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="8eae9-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8eae9-130">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8eae9-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8eae9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="8eae9-131">Requirements</span></span>



| <span data-ttu-id="8eae9-132">需求</span><span class="sxs-lookup"><span data-stu-id="8eae9-132">Requirement</span></span> | <span data-ttu-id="8eae9-133">值</span><span class="sxs-lookup"><span data-stu-id="8eae9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eae9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8eae9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8eae9-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8eae9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8eae9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8eae9-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eae9-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8eae9-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="8eae9-138">Namespace</span></span><br/>                | <span data-ttu-id="8eae9-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8eae9-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8eae9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8eae9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eae9-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8eae9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eae9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8eae9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eae9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8eae9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8eae9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8eae9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eae9-145">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="8eae9-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

