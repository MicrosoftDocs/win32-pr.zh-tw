---
description: CIM \_ ProductPhysicalElements 類別代表組成產品的實體元素。
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: CIM_ProductPhysicalElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110369"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="44123-103">CIM \_ ProductPhysicalElements 類別</span><span class="sxs-lookup"><span data-stu-id="44123-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="44123-104">**CIM \_ ProductPhysicalElements** 類別代表組成產品的實體元素。</span><span class="sxs-lookup"><span data-stu-id="44123-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44123-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="44123-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44123-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="44123-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44123-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="44123-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="44123-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="44123-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44123-109">語法</span><span class="sxs-lookup"><span data-stu-id="44123-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="44123-110">成員</span><span class="sxs-lookup"><span data-stu-id="44123-110">Members</span></span>

<span data-ttu-id="44123-111">**CIM \_ ProductPhysicalElements** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="44123-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="44123-112">屬性</span><span class="sxs-lookup"><span data-stu-id="44123-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44123-113">屬性</span><span class="sxs-lookup"><span data-stu-id="44123-113">Properties</span></span>

<span data-ttu-id="44123-114">**CIM \_ ProductPhysicalElements** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="44123-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44123-115">**元件**</span><span class="sxs-lookup"><span data-stu-id="44123-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44123-116">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="44123-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="44123-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44123-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44123-118">屬於產品一部分之實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="44123-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="44123-119">**產品**</span><span class="sxs-lookup"><span data-stu-id="44123-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44123-120">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="44123-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="44123-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44123-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44123-122">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="44123-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="44123-123">產品的參考。</span><span class="sxs-lookup"><span data-stu-id="44123-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44123-124">備註</span><span class="sxs-lookup"><span data-stu-id="44123-124">Remarks</span></span>

<span data-ttu-id="44123-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="44123-125">WMI does not implement this class.</span></span>

<span data-ttu-id="44123-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="44123-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44123-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="44123-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44123-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="44123-128">Requirements</span></span>



| <span data-ttu-id="44123-129">需求</span><span class="sxs-lookup"><span data-stu-id="44123-129">Requirement</span></span> | <span data-ttu-id="44123-130">值</span><span class="sxs-lookup"><span data-stu-id="44123-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44123-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44123-131">Minimum supported client</span></span><br/> | <span data-ttu-id="44123-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44123-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44123-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44123-133">Minimum supported server</span></span><br/> | <span data-ttu-id="44123-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44123-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44123-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="44123-135">Namespace</span></span><br/>                | <span data-ttu-id="44123-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44123-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44123-137">MOF</span><span class="sxs-lookup"><span data-stu-id="44123-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44123-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="44123-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44123-139">DLL</span><span class="sxs-lookup"><span data-stu-id="44123-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44123-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44123-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

