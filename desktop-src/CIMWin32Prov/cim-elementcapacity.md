---
description: CIM \_ ElementCapacity 類別會將 cim \_ PhysicalCapacity 物件與一或多個實體元素產生關聯。 它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468273"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="4f865-104">CIM \_ ElementCapacity 類別</span><span class="sxs-lookup"><span data-stu-id="4f865-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="4f865-105">**Cim \_ ElementCapacity** 類別會將 [**cim \_ PhysicalCapacity**](cim-physicalcapacity.md)物件與一或多個實體元素產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4f865-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="4f865-106">它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。</span><span class="sxs-lookup"><span data-stu-id="4f865-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f865-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4f865-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f865-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4f865-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4f865-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f865-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4f865-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4f865-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f865-111">語法</span><span class="sxs-lookup"><span data-stu-id="4f865-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="4f865-112">成員</span><span class="sxs-lookup"><span data-stu-id="4f865-112">Members</span></span>

<span data-ttu-id="4f865-113">**CIM \_ ElementCapacity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f865-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="4f865-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4f865-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f865-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4f865-115">Properties</span></span>

<span data-ttu-id="4f865-116">**CIM \_ ElementCapacity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f865-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f865-117">**容量**</span><span class="sxs-lookup"><span data-stu-id="4f865-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f865-118">資料類型： **CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="4f865-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="4f865-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f865-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f865-120">參考 [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) 類別，其描述最小和最大需求，以及支援實體元素的不同硬體類型的能力。</span><span class="sxs-lookup"><span data-stu-id="4f865-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="4f865-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f865-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f865-122">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="4f865-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="4f865-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f865-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f865-124">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="4f865-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4f865-125">所述實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="4f865-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f865-126">備註</span><span class="sxs-lookup"><span data-stu-id="4f865-126">Remarks</span></span>

<span data-ttu-id="4f865-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4f865-127">WMI does not implement this class.</span></span>

<span data-ttu-id="4f865-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4f865-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f865-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4f865-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f865-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f865-130">Requirements</span></span>



| <span data-ttu-id="4f865-131">需求</span><span class="sxs-lookup"><span data-stu-id="4f865-131">Requirement</span></span> | <span data-ttu-id="4f865-132">值</span><span class="sxs-lookup"><span data-stu-id="4f865-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f865-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f865-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4f865-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f865-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f865-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f865-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4f865-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f865-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f865-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="4f865-137">Namespace</span></span><br/>                | <span data-ttu-id="4f865-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4f865-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f865-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4f865-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f865-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f865-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f865-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4f865-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f865-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f865-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

