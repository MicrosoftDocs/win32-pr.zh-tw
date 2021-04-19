---
description: 定義虛擬系統。
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: CIM_VirtualSystemManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974627"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="56bf9-103">CIM VirtualSystemManagementService 類別的 DefineSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="56bf9-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="56bf9-104">定義虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="56bf9-104">Defines a virtual system.</span></span>

<span data-ttu-id="56bf9-105">未完全指定的輸入可能會以預設值填入。</span><span class="sxs-lookup"><span data-stu-id="56bf9-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bf9-106">語法</span><span class="sxs-lookup"><span data-stu-id="56bf9-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="56bf9-107">參數</span><span class="sxs-lookup"><span data-stu-id="56bf9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bf9-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56bf9-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56bf9-109">字串，包含類別 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 的內嵌實例，可用來定義要建立之虛擬系統的屬性。</span><span class="sxs-lookup"><span data-stu-id="56bf9-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="56bf9-110">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56bf9-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56bf9-111">字串陣列，其中每個字串都包含類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 的內嵌實例，以描述要在新虛擬系統的範圍中建立之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="56bf9-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="56bf9-112">*ReferenceConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56bf9-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56bf9-113">參考虛擬系統組態的最上層物件之 [**CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) 物件實例的參考。</span><span class="sxs-lookup"><span data-stu-id="56bf9-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="56bf9-114">如果 *SystemSettings* 和 *ResourceSettings* 參數未提供個別的資訊，則會使用參考設定來補充新虛擬系統的設定。</span><span class="sxs-lookup"><span data-stu-id="56bf9-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="56bf9-115">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56bf9-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56bf9-116">如果已成功定義虛擬電腦系統，則會傳回代表新定義虛擬電腦 [**系統 \_ 之類別的實例的參考**](cim-computersystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="56bf9-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="56bf9-117">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56bf9-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56bf9-118">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="56bf9-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="56bf9-119">在此情況下，會透過關聯 [**cim \_ AffectedJobElement**](cim-affectedjobelement.md)來呈現代表新虛擬系統的類別 [**cim \_**](cim-computersystem.md)系統實例，並以屬性 **AffectedElement** 參考 Cim 的新實例，**並 \_** 將屬性 **ElementEffects** 設定為 5 (建立) 。</span><span class="sxs-lookup"><span data-stu-id="56bf9-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bf9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="56bf9-120">Return value</span></span>

<span data-ttu-id="56bf9-121">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="56bf9-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="56bf9-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="56bf9-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-123">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="56bf9-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-124">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="56bf9-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-125">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="56bf9-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-126">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="56bf9-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-127">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="56bf9-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-128">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="56bf9-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-129">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="56bf9-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="56bf9-130">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="56bf9-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="56bf9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="56bf9-131">Requirements</span></span>



| <span data-ttu-id="56bf9-132">需求</span><span class="sxs-lookup"><span data-stu-id="56bf9-132">Requirement</span></span> | <span data-ttu-id="56bf9-133">值</span><span class="sxs-lookup"><span data-stu-id="56bf9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bf9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56bf9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="56bf9-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="56bf9-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="56bf9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56bf9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="56bf9-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="56bf9-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="56bf9-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="56bf9-138">Namespace</span></span><br/>                | <span data-ttu-id="56bf9-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="56bf9-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="56bf9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="56bf9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56bf9-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="56bf9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56bf9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="56bf9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bf9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56bf9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56bf9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56bf9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bf9-145">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="56bf9-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




