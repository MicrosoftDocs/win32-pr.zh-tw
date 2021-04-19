---
description: 依類別顯示度量。
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Msvm_MetricService 類別的 ShowMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996722"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="03b16-103">Msvm MetricService 類別的 ShowMetricsByClass 方法 \_</span><span class="sxs-lookup"><span data-stu-id="03b16-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="03b16-104">依類別顯示度量。</span><span class="sxs-lookup"><span data-stu-id="03b16-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b16-105">語法</span><span class="sxs-lookup"><span data-stu-id="03b16-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="03b16-106">參數</span><span class="sxs-lookup"><span data-stu-id="03b16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03b16-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="03b16-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03b16-108">識別 CIM 類別，其方法會將參考傳回給 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 的實例，以定義可針對類別的所有實例來捕捉的度量。</span><span class="sxs-lookup"><span data-stu-id="03b16-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="03b16-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03b16-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03b16-110">識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="03b16-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="03b16-111">方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。</span><span class="sxs-lookup"><span data-stu-id="03b16-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="03b16-112">*DefinitionList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03b16-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03b16-113">當方法成功完成時，可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的參考，而這些實例會定義可供 *主體* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)收集的計量。</span><span class="sxs-lookup"><span data-stu-id="03b16-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="03b16-114">*MetricNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03b16-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03b16-115">當方法成功完成時，每個陣列索引都包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的 **名稱** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="03b16-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="03b16-116">*MetricCollectionEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03b16-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03b16-117">指出是否要針對 managed 專案類別的所有實例收集度量。</span><span class="sxs-lookup"><span data-stu-id="03b16-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="03b16-118">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="03b16-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="03b16-119">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="03b16-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="03b16-120">**保留** (4) </span><span class="sxs-lookup"><span data-stu-id="03b16-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03b16-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="03b16-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="03b16-122">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="03b16-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="03b16-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03b16-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="03b16-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="03b16-124">Return value</span></span>

<span data-ttu-id="03b16-125">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="03b16-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="03b16-126">**成功** () </span><span class="sxs-lookup"><span data-stu-id="03b16-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="03b16-127">**不支援** () </span><span class="sxs-lookup"><span data-stu-id="03b16-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="03b16-128">**失敗** 的 () </span><span class="sxs-lookup"><span data-stu-id="03b16-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="03b16-129">**方法保留** () </span><span class="sxs-lookup"><span data-stu-id="03b16-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="03b16-130">**特定廠商** () </span><span class="sxs-lookup"><span data-stu-id="03b16-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="03b16-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="03b16-131">Requirements</span></span>



| <span data-ttu-id="03b16-132">需求</span><span class="sxs-lookup"><span data-stu-id="03b16-132">Requirement</span></span> | <span data-ttu-id="03b16-133">值</span><span class="sxs-lookup"><span data-stu-id="03b16-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b16-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03b16-134">Minimum supported client</span></span><br/> | <span data-ttu-id="03b16-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03b16-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="03b16-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03b16-136">Minimum supported server</span></span><br/> | <span data-ttu-id="03b16-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="03b16-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="03b16-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="03b16-138">Namespace</span></span><br/>                | <span data-ttu-id="03b16-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="03b16-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03b16-140">MOF</span><span class="sxs-lookup"><span data-stu-id="03b16-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03b16-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="03b16-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03b16-142">DLL</span><span class="sxs-lookup"><span data-stu-id="03b16-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b16-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03b16-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03b16-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03b16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b16-145">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="03b16-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




