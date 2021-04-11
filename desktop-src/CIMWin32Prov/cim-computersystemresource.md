---
description: CIM \_ ComputerSystemResource 類別代表電腦系統與其可用系統資源之間的關聯。
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: CIM_ComputerSystemResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025951"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="0d1a0-103">CIM \_ ComputerSystemResource 類別</span><span class="sxs-lookup"><span data-stu-id="0d1a0-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="0d1a0-104">**CIM \_ ComputerSystemResource** 類別代表電腦系統與其可用系統資源之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d1a0-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d1a0-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d1a0-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0d1a0-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1a0-109">語法</span><span class="sxs-lookup"><span data-stu-id="0d1a0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="0d1a0-110">成員</span><span class="sxs-lookup"><span data-stu-id="0d1a0-110">Members</span></span>

<span data-ttu-id="0d1a0-111">**CIM \_ ComputerSystemResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d1a0-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="0d1a0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0d1a0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d1a0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0d1a0-113">Properties</span></span>

<span data-ttu-id="0d1a0-114">**CIM \_ ComputerSystemResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d1a0-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d1a0-116">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="0d1a0-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0d1a0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d1a0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d1a0-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="0d1a0-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0d1a0-119">描述 [**電腦 \_ 系統的 CIM**](cim-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="0d1a0-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d1a0-121">資料類型： **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="0d1a0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d1a0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d1a0-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="0d1a0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0d1a0-124">描述電腦系統之系統資源的 [**CIM \_ SystemResource**](cim-systemresource.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d1a0-125">備註</span><span class="sxs-lookup"><span data-stu-id="0d1a0-125">Remarks</span></span>

<span data-ttu-id="0d1a0-126">**Cim \_ ComputerSystemResource** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="0d1a0-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-127">WMI does not implement this class.</span></span> <span data-ttu-id="0d1a0-128">如需衍生自 **CIM \_ ComputerSystemResource** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0d1a0-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d1a0-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1a0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d1a0-131">Requirements</span></span>



| <span data-ttu-id="0d1a0-132">需求</span><span class="sxs-lookup"><span data-stu-id="0d1a0-132">Requirement</span></span> | <span data-ttu-id="0d1a0-133">值</span><span class="sxs-lookup"><span data-stu-id="0d1a0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1a0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d1a0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1a0-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d1a0-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d1a0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d1a0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1a0-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d1a0-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d1a0-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d1a0-138">Namespace</span></span><br/>                | <span data-ttu-id="0d1a0-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d1a0-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d1a0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0d1a0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d1a0-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d1a0-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d1a0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0d1a0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d1a0-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1a0-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1a0-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d1a0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1a0-145">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="0d1a0-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

