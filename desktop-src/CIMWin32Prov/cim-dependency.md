---
description: CIM 相依性 \_ 類別代表在物件之間建立相依性關聯性的關聯。
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: 'CIM_Dependency 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688927"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="0c43c-103">CIM_Dependency 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="0c43c-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0c43c-104">**CIM 相依 \_** 性類別代表在物件之間建立相依性關聯性的關聯。</span><span class="sxs-lookup"><span data-stu-id="0c43c-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c43c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0c43c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0c43c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0c43c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0c43c-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c43c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c43c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0c43c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c43c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0c43c-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0c43c-110">成員</span><span class="sxs-lookup"><span data-stu-id="0c43c-110">Members</span></span>

<span data-ttu-id="0c43c-111">**CIM 相依 \_** 性類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0c43c-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0c43c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0c43c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c43c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0c43c-113">Properties</span></span>

<span data-ttu-id="0c43c-114">**CIM 相依 \_** 性類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0c43c-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c43c-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="0c43c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c43c-116">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="0c43c-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="0c43c-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c43c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c43c-118">參考此關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="0c43c-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="0c43c-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="0c43c-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c43c-120">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="0c43c-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="0c43c-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c43c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c43c-122">相依于 **Antecedent** 屬性之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="0c43c-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c43c-123">備註</span><span class="sxs-lookup"><span data-stu-id="0c43c-123">Remarks</span></span>

<span data-ttu-id="0c43c-124">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0c43c-124">WMI does not implement this class.</span></span> <span data-ttu-id="0c43c-125">如需衍生自 CIM 相依性之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。 **\_**</span><span class="sxs-lookup"><span data-stu-id="0c43c-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0c43c-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0c43c-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0c43c-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0c43c-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c43c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c43c-128">Requirements</span></span>



| <span data-ttu-id="0c43c-129">需求</span><span class="sxs-lookup"><span data-stu-id="0c43c-129">Requirement</span></span> | <span data-ttu-id="0c43c-130">值</span><span class="sxs-lookup"><span data-stu-id="0c43c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c43c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c43c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0c43c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c43c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c43c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c43c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0c43c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c43c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c43c-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c43c-135">Namespace</span></span><br/>                | <span data-ttu-id="0c43c-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0c43c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c43c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0c43c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c43c-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c43c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c43c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0c43c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c43c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c43c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




