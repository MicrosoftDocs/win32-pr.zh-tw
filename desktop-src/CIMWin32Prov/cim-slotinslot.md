---
description: CIM \_ SlotInSlot 關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972761"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="96872-103">CIM \_ SlotInSlot 類別</span><span class="sxs-lookup"><span data-stu-id="96872-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="96872-104">**CIM \_ SlotInSlot** 關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。</span><span class="sxs-lookup"><span data-stu-id="96872-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="96872-105">位置是一種特殊類型的連接器，通常會在其中插入介面卡。</span><span class="sxs-lookup"><span data-stu-id="96872-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="96872-106">介面卡可有效地建立新的位置，並可將其視為 (在概念上) 作為插槽中的位置。</span><span class="sxs-lookup"><span data-stu-id="96872-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="96872-107">如果是與現有插槽不相容的卡片，則可透過與介面卡所提供的插槽互動來支援。</span><span class="sxs-lookup"><span data-stu-id="96872-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="96872-108">例如，網路板的成本很高。</span><span class="sxs-lookup"><span data-stu-id="96872-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="96872-109">當有可用的新硬體時，會變更底座和卡片設定。</span><span class="sxs-lookup"><span data-stu-id="96872-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="96872-110">為了保護其客戶的投資，網路廠商會製造特殊的介面卡，以使用符合一或多個現有插槽的特殊介面卡，讓舊卡符合新的底座或主機面板或新卡片，並顯示可容納卡片的新位置。</span><span class="sxs-lookup"><span data-stu-id="96872-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96872-111">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="96872-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="96872-112">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="96872-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="96872-113">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="96872-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="96872-114">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="96872-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="96872-115">語法</span><span class="sxs-lookup"><span data-stu-id="96872-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="96872-116">成員</span><span class="sxs-lookup"><span data-stu-id="96872-116">Members</span></span>

<span data-ttu-id="96872-117">**CIM \_ SlotInSlot** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96872-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="96872-118">屬性</span><span class="sxs-lookup"><span data-stu-id="96872-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96872-119">屬性</span><span class="sxs-lookup"><span data-stu-id="96872-119">Properties</span></span>

<span data-ttu-id="96872-120">**CIM \_ SlotInSlot** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96872-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96872-121">**先行**</span><span class="sxs-lookup"><span data-stu-id="96872-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96872-122">資料類型： **CIM \_** 位置</span><span class="sxs-lookup"><span data-stu-id="96872-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="96872-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96872-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96872-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="96872-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="96872-125">[**CIM 位置 \_**](cim-slot.md) ，可描述主控面板的現有插槽 (s) ，或要調整以容納不會與它實際及/或電相容之卡片的框架。</span><span class="sxs-lookup"><span data-stu-id="96872-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="96872-126">**依賴**</span><span class="sxs-lookup"><span data-stu-id="96872-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96872-127">資料類型： **CIM \_** 位置</span><span class="sxs-lookup"><span data-stu-id="96872-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="96872-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96872-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96872-129">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="96872-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="96872-130">[**CIM 位置 \_**](cim-slot.md) ，描述介面卡面板所提供的新位置。</span><span class="sxs-lookup"><span data-stu-id="96872-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96872-131">備註</span><span class="sxs-lookup"><span data-stu-id="96872-131">Remarks</span></span>

<span data-ttu-id="96872-132">**Cim \_ SlotInSlot** 類別衍生自 [**cim \_ ConnectedTo**](cim-connectedto.md)。</span><span class="sxs-lookup"><span data-stu-id="96872-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="96872-133">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="96872-133">WMI does not implement this class.</span></span>

<span data-ttu-id="96872-134">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="96872-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="96872-135">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="96872-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="96872-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="96872-136">Requirements</span></span>



| <span data-ttu-id="96872-137">需求</span><span class="sxs-lookup"><span data-stu-id="96872-137">Requirement</span></span> | <span data-ttu-id="96872-138">值</span><span class="sxs-lookup"><span data-stu-id="96872-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96872-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96872-139">Minimum supported client</span></span><br/> | <span data-ttu-id="96872-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96872-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96872-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96872-141">Minimum supported server</span></span><br/> | <span data-ttu-id="96872-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96872-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96872-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="96872-143">Namespace</span></span><br/>                | <span data-ttu-id="96872-144">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="96872-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96872-145">MOF</span><span class="sxs-lookup"><span data-stu-id="96872-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96872-146"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="96872-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96872-147">DLL</span><span class="sxs-lookup"><span data-stu-id="96872-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96872-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96872-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96872-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96872-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96872-150">**CIM \_ ConnectedTo**</span><span class="sxs-lookup"><span data-stu-id="96872-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

