---
description: CIM \_ ComputerSystemIRQ 類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: CIM_ComputerSystemIRQ 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972139"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="fa662-103">CIM \_ ComputerSystemIRQ 類別</span><span class="sxs-lookup"><span data-stu-id="fa662-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="fa662-104">**CIM \_ ComputerSystemIRQ** 類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="fa662-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa662-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fa662-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa662-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fa662-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa662-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa662-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa662-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="fa662-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa662-109">語法</span><span class="sxs-lookup"><span data-stu-id="fa662-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fa662-110">成員</span><span class="sxs-lookup"><span data-stu-id="fa662-110">Members</span></span>

<span data-ttu-id="fa662-111">**CIM \_ ComputerSystemIRQ** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa662-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="fa662-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fa662-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa662-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fa662-113">Properties</span></span>

<span data-ttu-id="fa662-114">**CIM \_ ComputerSystemIRQ** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa662-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa662-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fa662-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa662-116">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="fa662-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fa662-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa662-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa662-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (的 GroupComponent) </span><span class="sxs-lookup"><span data-stu-id="fa662-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="fa662-119">CIM 的電腦，其描述與 IRQ 相關聯的電腦。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="fa662-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="fa662-120">這個屬性繼承自 [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="fa662-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="fa662-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fa662-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa662-122">資料類型： **CIM \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="fa662-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="fa662-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa662-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa662-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="fa662-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa662-125">描述電腦系統之 IRQ 的 [**CIM \_ IRQ**](cim-irq.md) 。</span><span class="sxs-lookup"><span data-stu-id="fa662-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa662-126">備註</span><span class="sxs-lookup"><span data-stu-id="fa662-126">Remarks</span></span>

<span data-ttu-id="fa662-127">**Cim \_ ComputerSystemIRQ** 類別衍生自 [**cim \_ ComputerSystemResource**](cim-computersystemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="fa662-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="fa662-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="fa662-128">WMI does not implement this class.</span></span>

<span data-ttu-id="fa662-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="fa662-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa662-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fa662-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa662-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa662-131">Requirements</span></span>



| <span data-ttu-id="fa662-132">需求</span><span class="sxs-lookup"><span data-stu-id="fa662-132">Requirement</span></span> | <span data-ttu-id="fa662-133">值</span><span class="sxs-lookup"><span data-stu-id="fa662-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa662-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa662-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fa662-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa662-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa662-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa662-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fa662-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa662-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa662-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa662-138">Namespace</span></span><br/>                | <span data-ttu-id="fa662-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fa662-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa662-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fa662-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa662-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa662-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa662-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fa662-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa662-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa662-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa662-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa662-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa662-145">**CIM \_ ComputerSystemResource**</span><span class="sxs-lookup"><span data-stu-id="fa662-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

