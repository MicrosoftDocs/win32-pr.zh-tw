---
description: CIM \_ PhysicalCapacity 類別是一種抽象類別，代表實體元素的最小和最大需求，以及其支援不同硬體類型的能力。
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: CIM_PhysicalCapacity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936354"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="220a7-103">CIM \_ PhysicalCapacity 類別</span><span class="sxs-lookup"><span data-stu-id="220a7-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="220a7-104">**CIM \_ PhysicalCapacity** 類別是一種抽象類別，代表實體元素的最小和最大需求，以及其支援不同硬體類型的能力。</span><span class="sxs-lookup"><span data-stu-id="220a7-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="220a7-105">例如，最小和最大記憶體需求可以模型化為 **CIM \_ PhysicalCapacity** 的子類別。</span><span class="sxs-lookup"><span data-stu-id="220a7-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="220a7-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="220a7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="220a7-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="220a7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="220a7-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="220a7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="220a7-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="220a7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="220a7-110">語法</span><span class="sxs-lookup"><span data-stu-id="220a7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="220a7-111">成員</span><span class="sxs-lookup"><span data-stu-id="220a7-111">Members</span></span>

<span data-ttu-id="220a7-112">**CIM \_ PhysicalCapacity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="220a7-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="220a7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="220a7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="220a7-114">屬性</span><span class="sxs-lookup"><span data-stu-id="220a7-114">Properties</span></span>

<span data-ttu-id="220a7-115">**CIM \_ PhysicalCapacity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="220a7-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="220a7-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="220a7-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="220a7-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="220a7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="220a7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="220a7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="220a7-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="220a7-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="220a7-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="220a7-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="220a7-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="220a7-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="220a7-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="220a7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="220a7-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="220a7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="220a7-124">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="220a7-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="220a7-125">**名稱**</span><span class="sxs-lookup"><span data-stu-id="220a7-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="220a7-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="220a7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="220a7-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="220a7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="220a7-128">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="220a7-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="220a7-129">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="220a7-129">Label by which the object is known.</span></span> <span data-ttu-id="220a7-130">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="220a7-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="220a7-131">備註</span><span class="sxs-lookup"><span data-stu-id="220a7-131">Remarks</span></span>

<span data-ttu-id="220a7-132">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="220a7-132">WMI does not implement this class.</span></span>

<span data-ttu-id="220a7-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="220a7-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="220a7-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="220a7-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="220a7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="220a7-135">Requirements</span></span>



| <span data-ttu-id="220a7-136">需求</span><span class="sxs-lookup"><span data-stu-id="220a7-136">Requirement</span></span> | <span data-ttu-id="220a7-137">值</span><span class="sxs-lookup"><span data-stu-id="220a7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="220a7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="220a7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="220a7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="220a7-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="220a7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="220a7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="220a7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="220a7-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="220a7-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="220a7-142">Namespace</span></span><br/>                | <span data-ttu-id="220a7-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="220a7-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="220a7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="220a7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="220a7-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="220a7-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="220a7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="220a7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="220a7-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220a7-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

