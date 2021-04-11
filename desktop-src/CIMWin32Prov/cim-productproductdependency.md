---
description: CIM \_ ProductProductDependency 類別代表兩項產品之間的關聯，這表示必須安裝或不存在才能讓另一個產品運作。 這在概念上相當於 CIM \_ ServiceServiceDependency 關聯。
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: CIM_ProductProductDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025865"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="46c70-104">CIM \_ ProductProductDependency 類別</span><span class="sxs-lookup"><span data-stu-id="46c70-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="46c70-105">**CIM \_ ProductProductDependency** 類別代表兩項產品之間的關聯，這表示必須安裝或不存在才能讓另一個產品運作。</span><span class="sxs-lookup"><span data-stu-id="46c70-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="46c70-106">這在概念上相當於 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="46c70-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46c70-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="46c70-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="46c70-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="46c70-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="46c70-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="46c70-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="46c70-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="46c70-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c70-111">語法</span><span class="sxs-lookup"><span data-stu-id="46c70-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="46c70-112">成員</span><span class="sxs-lookup"><span data-stu-id="46c70-112">Members</span></span>

<span data-ttu-id="46c70-113">**CIM \_ ProductProductDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46c70-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="46c70-114">屬性</span><span class="sxs-lookup"><span data-stu-id="46c70-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46c70-115">屬性</span><span class="sxs-lookup"><span data-stu-id="46c70-115">Properties</span></span>

<span data-ttu-id="46c70-116">**CIM \_ ProductProductDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="46c70-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46c70-117">**DependentProduct**</span><span class="sxs-lookup"><span data-stu-id="46c70-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c70-118">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="46c70-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="46c70-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46c70-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46c70-120">參考相依于其他產品的產品。</span><span class="sxs-lookup"><span data-stu-id="46c70-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="46c70-121">**RequiredProduct**</span><span class="sxs-lookup"><span data-stu-id="46c70-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c70-122">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="46c70-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="46c70-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46c70-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46c70-124">參考所需的產品。</span><span class="sxs-lookup"><span data-stu-id="46c70-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="46c70-125">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="46c70-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c70-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="46c70-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46c70-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46c70-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46c70-128">產品相依性的本質。</span><span class="sxs-lookup"><span data-stu-id="46c70-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46c70-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="46c70-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46c70-130">不明。</span><span class="sxs-lookup"><span data-stu-id="46c70-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46c70-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="46c70-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46c70-132">其他。</span><span class="sxs-lookup"><span data-stu-id="46c70-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="46c70-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**產品必須安裝** (2) </span><span class="sxs-lookup"><span data-stu-id="46c70-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="46c70-134">必須安裝產品。</span><span class="sxs-lookup"><span data-stu-id="46c70-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="46c70-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**產品不得安裝** (3) </span><span class="sxs-lookup"><span data-stu-id="46c70-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46c70-136">不得安裝產品。</span><span class="sxs-lookup"><span data-stu-id="46c70-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46c70-137">備註</span><span class="sxs-lookup"><span data-stu-id="46c70-137">Remarks</span></span>

<span data-ttu-id="46c70-138">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="46c70-138">WMI does not implement this class.</span></span>

<span data-ttu-id="46c70-139">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="46c70-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="46c70-140">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="46c70-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c70-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="46c70-141">Requirements</span></span>



| <span data-ttu-id="46c70-142">需求</span><span class="sxs-lookup"><span data-stu-id="46c70-142">Requirement</span></span> | <span data-ttu-id="46c70-143">值</span><span class="sxs-lookup"><span data-stu-id="46c70-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46c70-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46c70-144">Minimum supported client</span></span><br/> | <span data-ttu-id="46c70-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46c70-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46c70-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46c70-146">Minimum supported server</span></span><br/> | <span data-ttu-id="46c70-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46c70-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46c70-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="46c70-148">Namespace</span></span><br/>                | <span data-ttu-id="46c70-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46c70-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46c70-150">MOF</span><span class="sxs-lookup"><span data-stu-id="46c70-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46c70-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="46c70-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46c70-152">DLL</span><span class="sxs-lookup"><span data-stu-id="46c70-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c70-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c70-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




