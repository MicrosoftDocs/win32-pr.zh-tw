---
description: CIM \_ CollectionOfSensors 關聯代表組成 multistate 感應器的二元感應器。
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: CIM_CollectionOfSensors 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936360"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="f1015-103">CIM \_ CollectionOfSensors 類別</span><span class="sxs-lookup"><span data-stu-id="f1015-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="f1015-104">**CIM \_ CollectionOfSensors** 關聯代表組成 multistate 感應器的二元感應器。</span><span class="sxs-lookup"><span data-stu-id="f1015-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1015-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f1015-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1015-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f1015-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1015-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1015-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f1015-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f1015-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1015-109">語法</span><span class="sxs-lookup"><span data-stu-id="f1015-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f1015-110">成員</span><span class="sxs-lookup"><span data-stu-id="f1015-110">Members</span></span>

<span data-ttu-id="f1015-111">**CIM \_ CollectionOfSensors** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f1015-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="f1015-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f1015-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1015-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f1015-113">Properties</span></span>

<span data-ttu-id="f1015-114">**CIM \_ CollectionOfSensors** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1015-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1015-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f1015-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1015-116">資料類型： **CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="f1015-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="f1015-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1015-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1015-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="f1015-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1015-119">描述多重狀態感應器的 [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) 。</span><span class="sxs-lookup"><span data-stu-id="f1015-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="f1015-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f1015-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1015-121">資料類型： **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="f1015-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="f1015-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1015-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1015-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="f1015-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1015-124">[**CIM \_ BinarySensor**](cim-binarysensor.md) ，描述屬於多重狀態感應器一部分的二進位感應器。</span><span class="sxs-lookup"><span data-stu-id="f1015-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1015-125">備註</span><span class="sxs-lookup"><span data-stu-id="f1015-125">Remarks</span></span>

<span data-ttu-id="f1015-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f1015-126">WMI does not implement this class.</span></span>

<span data-ttu-id="f1015-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f1015-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1015-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f1015-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1015-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1015-129">Requirements</span></span>



| <span data-ttu-id="f1015-130">需求</span><span class="sxs-lookup"><span data-stu-id="f1015-130">Requirement</span></span> | <span data-ttu-id="f1015-131">值</span><span class="sxs-lookup"><span data-stu-id="f1015-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1015-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1015-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f1015-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1015-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1015-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1015-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f1015-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1015-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1015-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1015-136">Namespace</span></span><br/>                | <span data-ttu-id="f1015-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1015-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1015-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f1015-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1015-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1015-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1015-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f1015-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1015-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1015-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1015-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1015-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1015-143">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="f1015-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

