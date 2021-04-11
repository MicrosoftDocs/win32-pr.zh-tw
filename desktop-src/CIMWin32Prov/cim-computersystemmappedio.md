---
description: CIM \_ ComputerSystemMappedIO 類別代表電腦系統與其可用記憶體對應 i/o 埠之間的關聯。
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: CIM_ComputerSystemMappedIO 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110989"
---
# <a name="cim_computersystemmappedio-class"></a><span data-ttu-id="e684c-103">CIM \_ ComputerSystemMappedIO 類別</span><span class="sxs-lookup"><span data-stu-id="e684c-103">CIM\_ComputerSystemMappedIO class</span></span>

<span data-ttu-id="e684c-104">**CIM \_ ComputerSystemMappedIO** 類別代表電腦系統與其可用記憶體對應 i/o 埠之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="e684c-104">The **CIM\_ComputerSystemMappedIO** class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e684c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e684c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e684c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e684c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e684c-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e684c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e684c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e684c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e684c-109">語法</span><span class="sxs-lookup"><span data-stu-id="e684c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e684c-110">成員</span><span class="sxs-lookup"><span data-stu-id="e684c-110">Members</span></span>

<span data-ttu-id="e684c-111">**CIM \_ ComputerSystemMappedIO** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e684c-111">The **CIM\_ComputerSystemMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="e684c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e684c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e684c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e684c-113">Properties</span></span>

<span data-ttu-id="e684c-114">**CIM \_ ComputerSystemMappedIO** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e684c-114">The **CIM\_ComputerSystemMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e684c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e684c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e684c-116">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="e684c-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e684c-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e684c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e684c-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (的 GroupComponent) </span><span class="sxs-lookup"><span data-stu-id="e684c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="e684c-119">CIM 電腦系統，描述對應到 i/o 埠的電腦系統。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="e684c-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system mapped to the I/O port.</span></span>

<span data-ttu-id="e684c-120">這個屬性繼承自 [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="e684c-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="e684c-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e684c-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e684c-122">資料類型： **CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="e684c-122">Data type: **CIM\_MemoryMappedIO**</span></span>
</dt> <dt>

<span data-ttu-id="e684c-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e684c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e684c-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="e684c-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e684c-125">[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) ，描述電腦系統的記憶體對應 i/o 埠。</span><span class="sxs-lookup"><span data-stu-id="e684c-125">A [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) that describes a memory mapped I/O port of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e684c-126">備註</span><span class="sxs-lookup"><span data-stu-id="e684c-126">Remarks</span></span>

<span data-ttu-id="e684c-127">**Cim \_ ComputerSystemMappedIO** 類別衍生自 [**cim \_ ComputerSystemResource**](cim-computersystemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="e684c-127">The **CIM\_ComputerSystemMappedIO** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="e684c-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e684c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="e684c-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e684c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e684c-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e684c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e684c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e684c-131">Requirements</span></span>



| <span data-ttu-id="e684c-132">需求</span><span class="sxs-lookup"><span data-stu-id="e684c-132">Requirement</span></span> | <span data-ttu-id="e684c-133">值</span><span class="sxs-lookup"><span data-stu-id="e684c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e684c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e684c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e684c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e684c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e684c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e684c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e684c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e684c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e684c-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="e684c-138">Namespace</span></span><br/>                | <span data-ttu-id="e684c-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e684c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e684c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e684c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e684c-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e684c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e684c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e684c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e684c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e684c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e684c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e684c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e684c-145">**CIM \_ ComputerSystemResource**</span><span class="sxs-lookup"><span data-stu-id="e684c-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

