---
description: CIM \_ 元件關聯表示 mse 之間關聯性的元件。
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: 'CIM_Component 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847400"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="b36eb-103">CIM_Component 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="b36eb-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b36eb-104">**CIM \_ 元件** 關聯表示 mse 之間關聯性的元件。</span><span class="sxs-lookup"><span data-stu-id="b36eb-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b36eb-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b36eb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b36eb-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b36eb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b36eb-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b36eb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b36eb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b36eb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b36eb-109">語法</span><span class="sxs-lookup"><span data-stu-id="b36eb-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b36eb-110">成員</span><span class="sxs-lookup"><span data-stu-id="b36eb-110">Members</span></span>

<span data-ttu-id="b36eb-111">**CIM \_ 元件** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b36eb-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="b36eb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b36eb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b36eb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b36eb-113">Properties</span></span>

<span data-ttu-id="b36eb-114">**CIM \_ 元件** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b36eb-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b36eb-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b36eb-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36eb-116">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b36eb-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b36eb-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b36eb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36eb-118">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b36eb-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b36eb-119">描述關聯中父元素的 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 。</span><span class="sxs-lookup"><span data-stu-id="b36eb-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="b36eb-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b36eb-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36eb-121">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b36eb-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b36eb-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b36eb-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36eb-123">[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ，描述關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="b36eb-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b36eb-124">備註</span><span class="sxs-lookup"><span data-stu-id="b36eb-124">Remarks</span></span>

<span data-ttu-id="b36eb-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b36eb-125">WMI does not implement this class.</span></span> <span data-ttu-id="b36eb-126">如需衍生自 **CIM \_ 元件** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b36eb-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b36eb-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b36eb-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b36eb-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b36eb-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36eb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b36eb-129">Requirements</span></span>



| <span data-ttu-id="b36eb-130">需求</span><span class="sxs-lookup"><span data-stu-id="b36eb-130">Requirement</span></span> | <span data-ttu-id="b36eb-131">值</span><span class="sxs-lookup"><span data-stu-id="b36eb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b36eb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b36eb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b36eb-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b36eb-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b36eb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b36eb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b36eb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b36eb-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b36eb-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="b36eb-136">Namespace</span></span><br/>                | <span data-ttu-id="b36eb-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b36eb-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b36eb-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b36eb-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b36eb-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b36eb-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b36eb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b36eb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b36eb-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b36eb-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

