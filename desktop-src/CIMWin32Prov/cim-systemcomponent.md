---
description: 通用訊息模型 (CIM) 關聯類別，可建立系統與其組成之 managed 系統元素之間的關聯性。
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: 'CIM_SystemComponent 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110985"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="a6f4f-103">CIM_SystemComponent 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="a6f4f-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a6f4f-104">**Cim \_ SystemComponent** 類別是一種通用訊息模型 (CIM) 關聯類別，可建立系統與其組成之 managed 系統專案之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6f4f-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a6f4f-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a6f4f-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a6f4f-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f4f-109">語法</span><span class="sxs-lookup"><span data-stu-id="a6f4f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a6f4f-110">成員</span><span class="sxs-lookup"><span data-stu-id="a6f4f-110">Members</span></span>

<span data-ttu-id="a6f4f-111">**CIM \_ SystemComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a6f4f-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a6f4f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a6f4f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6f4f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a6f4f-113">Properties</span></span>

<span data-ttu-id="a6f4f-114">**CIM \_ SystemComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6f4f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a6f4f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f4f-116">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="a6f4f-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="a6f4f-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6f4f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f4f-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="a6f4f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a6f4f-119">在關聯中描述父系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a6f4f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a6f4f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f4f-121">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a6f4f-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="a6f4f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6f4f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f4f-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="a6f4f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a6f4f-124">[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ，描述屬於系統元件的子項目。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6f4f-125">備註</span><span class="sxs-lookup"><span data-stu-id="a6f4f-125">Remarks</span></span>

<span data-ttu-id="a6f4f-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-126">WMI does not implement this class.</span></span> <span data-ttu-id="a6f4f-127">針對衍生自 **CIM \_ SYSTEMCOMPONENT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a6f4f-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a6f4f-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a6f4f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f4f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6f4f-130">Requirements</span></span>



| <span data-ttu-id="a6f4f-131">需求</span><span class="sxs-lookup"><span data-stu-id="a6f4f-131">Requirement</span></span> | <span data-ttu-id="a6f4f-132">值</span><span class="sxs-lookup"><span data-stu-id="a6f4f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f4f-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6f4f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f4f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6f4f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6f4f-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6f4f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f4f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6f4f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6f4f-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="a6f4f-137">Namespace</span></span><br/>                | <span data-ttu-id="a6f4f-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a6f4f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6f4f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a6f4f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6f4f-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6f4f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6f4f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f4f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6f4f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6f4f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f4f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6f4f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f4f-144">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="a6f4f-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

