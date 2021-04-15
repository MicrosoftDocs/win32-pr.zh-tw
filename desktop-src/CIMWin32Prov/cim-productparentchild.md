---
description: CIM \_ ProductParentChild 關聯會定義產品之間的父子式階層。 例如，產品可以與其他產品配套。
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: CIM_ProductParentChild 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510464"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="a290e-104">CIM \_ ProductParentChild 類別</span><span class="sxs-lookup"><span data-stu-id="a290e-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="a290e-105">**CIM \_ ProductParentChild** 關聯會定義產品之間的父子式階層。</span><span class="sxs-lookup"><span data-stu-id="a290e-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="a290e-106">例如，產品可以與其他產品配套。</span><span class="sxs-lookup"><span data-stu-id="a290e-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a290e-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a290e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a290e-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a290e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a290e-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a290e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a290e-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a290e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a290e-111">語法</span><span class="sxs-lookup"><span data-stu-id="a290e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="a290e-112">成員</span><span class="sxs-lookup"><span data-stu-id="a290e-112">Members</span></span>

<span data-ttu-id="a290e-113">**CIM \_ ProductParentChild** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a290e-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="a290e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a290e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a290e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a290e-115">Properties</span></span>

<span data-ttu-id="a290e-116">**CIM \_ ProductParentChild** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a290e-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a290e-117">**子系**</span><span class="sxs-lookup"><span data-stu-id="a290e-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a290e-118">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="a290e-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="a290e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a290e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a290e-120">關聯中子產品的參考。</span><span class="sxs-lookup"><span data-stu-id="a290e-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a290e-121">**父系**</span><span class="sxs-lookup"><span data-stu-id="a290e-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a290e-122">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="a290e-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="a290e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a290e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a290e-124">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a290e-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a290e-125">關聯中父產品的參考。</span><span class="sxs-lookup"><span data-stu-id="a290e-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a290e-126">備註</span><span class="sxs-lookup"><span data-stu-id="a290e-126">Remarks</span></span>

<span data-ttu-id="a290e-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a290e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a290e-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a290e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a290e-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a290e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a290e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a290e-130">Requirements</span></span>



| <span data-ttu-id="a290e-131">需求</span><span class="sxs-lookup"><span data-stu-id="a290e-131">Requirement</span></span> | <span data-ttu-id="a290e-132">值</span><span class="sxs-lookup"><span data-stu-id="a290e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a290e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a290e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a290e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a290e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a290e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a290e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a290e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a290e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a290e-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="a290e-137">Namespace</span></span><br/>                | <span data-ttu-id="a290e-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a290e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a290e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a290e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a290e-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a290e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a290e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a290e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a290e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a290e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

