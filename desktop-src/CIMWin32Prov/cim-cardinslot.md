---
description: CIM \_ CardInSlot 類別會將介面卡卡片與插入它的容器產生關聯。
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: CIM_CardInSlot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847411"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="e85c0-103">CIM \_ CardInSlot 類別</span><span class="sxs-lookup"><span data-stu-id="e85c0-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="e85c0-104">**CIM \_ CardInSlot** 類別會將介面卡卡片與插入它的容器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e85c0-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e85c0-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e85c0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e85c0-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e85c0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e85c0-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e85c0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e85c0-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e85c0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85c0-109">語法</span><span class="sxs-lookup"><span data-stu-id="e85c0-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e85c0-110">成員</span><span class="sxs-lookup"><span data-stu-id="e85c0-110">Members</span></span>

<span data-ttu-id="e85c0-111">**CIM \_ CardInSlot** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e85c0-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="e85c0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e85c0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e85c0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e85c0-113">Properties</span></span>

<span data-ttu-id="e85c0-114">**CIM \_ CardInSlot** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e85c0-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e85c0-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="e85c0-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85c0-116">資料類型： **CIM \_** 位置</span><span class="sxs-lookup"><span data-stu-id="e85c0-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="e85c0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e85c0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e85c0-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="e85c0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e85c0-119">[**CIM 位置 \_**](cim-slot.md) ，描述卡片插入的位置。</span><span class="sxs-lookup"><span data-stu-id="e85c0-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="e85c0-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e85c0-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85c0-121">資料類型： **CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="e85c0-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="e85c0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e85c0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e85c0-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="e85c0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e85c0-124">一種 [**CIM \_ 卡片**](cim-card.md) ，可描述插槽中的卡片。</span><span class="sxs-lookup"><span data-stu-id="e85c0-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e85c0-125">備註</span><span class="sxs-lookup"><span data-stu-id="e85c0-125">Remarks</span></span>

<span data-ttu-id="e85c0-126">**Cim \_ CardInSlot** 類別衍生自 [**cim \_ PackageInSlot**](cim-packageinslot.md)。</span><span class="sxs-lookup"><span data-stu-id="e85c0-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="e85c0-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e85c0-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e85c0-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e85c0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e85c0-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e85c0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e85c0-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e85c0-130">Requirements</span></span>



| <span data-ttu-id="e85c0-131">需求</span><span class="sxs-lookup"><span data-stu-id="e85c0-131">Requirement</span></span> | <span data-ttu-id="e85c0-132">值</span><span class="sxs-lookup"><span data-stu-id="e85c0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e85c0-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e85c0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e85c0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e85c0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e85c0-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e85c0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e85c0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e85c0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e85c0-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="e85c0-137">Namespace</span></span><br/>                | <span data-ttu-id="e85c0-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e85c0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e85c0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e85c0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e85c0-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e85c0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e85c0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e85c0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e85c0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e85c0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85c0-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e85c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85c0-144">**CIM \_ PackageInSlot**</span><span class="sxs-lookup"><span data-stu-id="e85c0-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

