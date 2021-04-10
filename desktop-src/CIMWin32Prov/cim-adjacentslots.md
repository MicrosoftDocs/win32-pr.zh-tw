---
description: CIM \_ AdjacentSlots 關聯描述主控電路板或介面卡卡上的位置版面配置。
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111105"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="1a50f-103">CIM \_ AdjacentSlots 類別</span><span class="sxs-lookup"><span data-stu-id="1a50f-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="1a50f-104">**CIM \_ AdjacentSlots** 關聯描述主控電路板或介面卡卡上的位置版面配置。</span><span class="sxs-lookup"><span data-stu-id="1a50f-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="1a50f-105">資訊，例如位置之間的距離，以及它們是否為「共用」 (如果已填入，則無法使用另一個位置，) 會將它傳達為關聯屬性。</span><span class="sxs-lookup"><span data-stu-id="1a50f-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a50f-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1a50f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1a50f-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1a50f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1a50f-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a50f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1a50f-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1a50f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a50f-110">語法</span><span class="sxs-lookup"><span data-stu-id="1a50f-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="1a50f-111">成員</span><span class="sxs-lookup"><span data-stu-id="1a50f-111">Members</span></span>

<span data-ttu-id="1a50f-112">**CIM \_ AdjacentSlots** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1a50f-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="1a50f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1a50f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a50f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1a50f-114">Properties</span></span>

<span data-ttu-id="1a50f-115">**CIM \_ AdjacentSlots** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1a50f-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a50f-116">**DistanceBetweenSlots**</span><span class="sxs-lookup"><span data-stu-id="1a50f-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50f-117">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="1a50f-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1a50f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a50f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a50f-119">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="1a50f-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1a50f-120">相鄰插槽之間的距離（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a50f-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1a50f-121">**SharedSlots**</span><span class="sxs-lookup"><span data-stu-id="1a50f-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50f-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1a50f-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a50f-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a50f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50f-124">若 **為 TRUE**，則介面卡會填入其中一個位置，另一個位置必須保留空白。</span><span class="sxs-lookup"><span data-stu-id="1a50f-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="1a50f-125">**SlotA**</span><span class="sxs-lookup"><span data-stu-id="1a50f-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50f-126">資料類型： **CIM \_** 位置</span><span class="sxs-lookup"><span data-stu-id="1a50f-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1a50f-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a50f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50f-128">參考其中一個連續的位置。</span><span class="sxs-lookup"><span data-stu-id="1a50f-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1a50f-129">**SlotB**</span><span class="sxs-lookup"><span data-stu-id="1a50f-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50f-130">資料類型： **CIM \_** 位置</span><span class="sxs-lookup"><span data-stu-id="1a50f-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1a50f-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a50f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50f-132">「其他」相鄰位置的參考。</span><span class="sxs-lookup"><span data-stu-id="1a50f-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a50f-133">備註</span><span class="sxs-lookup"><span data-stu-id="1a50f-133">Remarks</span></span>

<span data-ttu-id="1a50f-134">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1a50f-134">WMI does not implement this class.</span></span>

<span data-ttu-id="1a50f-135">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1a50f-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1a50f-136">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1a50f-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a50f-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a50f-137">Requirements</span></span>



| <span data-ttu-id="1a50f-138">需求</span><span class="sxs-lookup"><span data-stu-id="1a50f-138">Requirement</span></span> | <span data-ttu-id="1a50f-139">值</span><span class="sxs-lookup"><span data-stu-id="1a50f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a50f-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a50f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1a50f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a50f-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a50f-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a50f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1a50f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a50f-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a50f-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="1a50f-144">Namespace</span></span><br/>                | <span data-ttu-id="1a50f-145">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1a50f-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a50f-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1a50f-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a50f-147"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a50f-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a50f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1a50f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a50f-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a50f-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a50f-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a50f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a50f-151">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="1a50f-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

