---
description: CIM \_ CardOnCard 關聯描述的是可插入主機板/主機板、介面卡 daughtercards 或卡片的關聯性，以支援特殊的卡片型模組。
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: CIM_CardOnCard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385954"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="e299e-103">CIM \_ CardOnCard 類別</span><span class="sxs-lookup"><span data-stu-id="e299e-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="e299e-104">**CIM \_ CardOnCard** 關聯描述的是可插入主機板/主機板、介面卡 daughtercards 或卡片的關聯性，以支援特殊的卡片型模組。</span><span class="sxs-lookup"><span data-stu-id="e299e-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e299e-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e299e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e299e-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e299e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e299e-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e299e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e299e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e299e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e299e-109">語法</span><span class="sxs-lookup"><span data-stu-id="e299e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="e299e-110">成員</span><span class="sxs-lookup"><span data-stu-id="e299e-110">Members</span></span>

<span data-ttu-id="e299e-111">**CIM \_ CardOnCard** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e299e-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="e299e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e299e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e299e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e299e-113">Properties</span></span>

<span data-ttu-id="e299e-114">**CIM \_ CardOnCard** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e299e-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e299e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e299e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e299e-116">資料類型： **CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="e299e-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="e299e-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e299e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e299e-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="e299e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e299e-119">一種 [**CIM \_ 卡片**](cim-card.md) ，可描述主控另一張卡片的卡片。</span><span class="sxs-lookup"><span data-stu-id="e299e-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="e299e-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="e299e-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e299e-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e299e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e299e-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e299e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e299e-123">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="e299e-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="e299e-124">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="e299e-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="e299e-125">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="e299e-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="e299e-126">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="e299e-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="e299e-127">**MountOrSlotDescription**</span><span class="sxs-lookup"><span data-stu-id="e299e-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e299e-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e299e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e299e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e299e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e299e-130">描述及識別如何在「其他」卡片上掛接或插入卡。</span><span class="sxs-lookup"><span data-stu-id="e299e-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="e299e-131">位置資訊可以包含在此欄位中，而且可能足以滿足特定的管理目的，這可避免建立連接器/位置物件的具現化，只是要建立卡片與主控面板或其他介面卡的關聯性模型。</span><span class="sxs-lookup"><span data-stu-id="e299e-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="e299e-132">相反地，如果有可用的位置和連接器資訊，此欄位可用來提供詳細的裝載或位置插入資料。</span><span class="sxs-lookup"><span data-stu-id="e299e-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="e299e-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e299e-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e299e-134">資料類型： **CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="e299e-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="e299e-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e299e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e299e-136">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="e299e-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e299e-137">一種 [**CIM \_ 卡片**](cim-card.md) ，描述插入或其他卡上的插卡。</span><span class="sxs-lookup"><span data-stu-id="e299e-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e299e-138">備註</span><span class="sxs-lookup"><span data-stu-id="e299e-138">Remarks</span></span>

<span data-ttu-id="e299e-139">**Cim \_ CardOnCard** 類別衍生自 [**cim \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="e299e-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="e299e-140">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e299e-140">WMI does not implement this class.</span></span>

<span data-ttu-id="e299e-141">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e299e-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e299e-142">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e299e-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e299e-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e299e-143">Requirements</span></span>



| <span data-ttu-id="e299e-144">需求</span><span class="sxs-lookup"><span data-stu-id="e299e-144">Requirement</span></span> | <span data-ttu-id="e299e-145">值</span><span class="sxs-lookup"><span data-stu-id="e299e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e299e-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e299e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e299e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e299e-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e299e-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e299e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e299e-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e299e-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e299e-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="e299e-150">Namespace</span></span><br/>                | <span data-ttu-id="e299e-151">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e299e-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e299e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e299e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e299e-153"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e299e-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e299e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e299e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e299e-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e299e-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e299e-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e299e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e299e-157">**CIM \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="e299e-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

