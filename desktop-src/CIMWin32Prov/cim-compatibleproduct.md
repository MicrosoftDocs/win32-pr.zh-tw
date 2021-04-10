---
description: CIM \_ CompatibleProduct 類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847401"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="b5970-103">CIM \_ CompatibleProduct 類別</span><span class="sxs-lookup"><span data-stu-id="b5970-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="b5970-104">**CIM \_ CompatibleProduct** 類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。</span><span class="sxs-lookup"><span data-stu-id="b5970-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5970-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b5970-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5970-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b5970-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5970-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b5970-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5970-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b5970-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5970-109">語法</span><span class="sxs-lookup"><span data-stu-id="b5970-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="b5970-110">成員</span><span class="sxs-lookup"><span data-stu-id="b5970-110">Members</span></span>

<span data-ttu-id="b5970-111">**CIM \_ CompatibleProduct** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5970-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="b5970-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b5970-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5970-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b5970-113">Properties</span></span>

<span data-ttu-id="b5970-114">**CIM \_ CompatibleProduct** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b5970-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5970-115">**CompatibilityDescription**</span><span class="sxs-lookup"><span data-stu-id="b5970-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5970-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5970-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5970-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5970-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5970-118">自由格式的字串，可定義兩個參考的產品如何互通、相容，以及是否有相容性限制。</span><span class="sxs-lookup"><span data-stu-id="b5970-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="b5970-119">**CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="b5970-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5970-120">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="b5970-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="b5970-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5970-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5970-122">相容產品的參考。</span><span class="sxs-lookup"><span data-stu-id="b5970-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="b5970-123">**產品**</span><span class="sxs-lookup"><span data-stu-id="b5970-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5970-124">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="b5970-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="b5970-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5970-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5970-126">參考已定義相容產品的產品。</span><span class="sxs-lookup"><span data-stu-id="b5970-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5970-127">備註</span><span class="sxs-lookup"><span data-stu-id="b5970-127">Remarks</span></span>

<span data-ttu-id="b5970-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b5970-128">WMI does not implement this class.</span></span>

<span data-ttu-id="b5970-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b5970-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5970-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b5970-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5970-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5970-131">Requirements</span></span>



| <span data-ttu-id="b5970-132">需求</span><span class="sxs-lookup"><span data-stu-id="b5970-132">Requirement</span></span> | <span data-ttu-id="b5970-133">值</span><span class="sxs-lookup"><span data-stu-id="b5970-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5970-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5970-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5970-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5970-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5970-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5970-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5970-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5970-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5970-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="b5970-138">Namespace</span></span><br/>                | <span data-ttu-id="b5970-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5970-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5970-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b5970-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5970-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5970-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5970-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5970-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5970-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5970-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




