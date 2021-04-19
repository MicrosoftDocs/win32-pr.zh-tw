---
description: CIM \_ ProductSupport 類別代表產品與支援存取之間的關聯，可傳達如何取得產品的支援。
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973959"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="520f7-103">CIM \_ ProductSupport 類別</span><span class="sxs-lookup"><span data-stu-id="520f7-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="520f7-104">**CIM \_ ProductSupport** 類別代表產品與支援存取之間的關聯，可傳達如何取得產品的支援。</span><span class="sxs-lookup"><span data-stu-id="520f7-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="520f7-105">產品有各種類型的支援，相同的支持對象可以提供多項產品的協助。</span><span class="sxs-lookup"><span data-stu-id="520f7-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="520f7-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="520f7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="520f7-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="520f7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="520f7-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="520f7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="520f7-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="520f7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="520f7-110">語法</span><span class="sxs-lookup"><span data-stu-id="520f7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="520f7-111">成員</span><span class="sxs-lookup"><span data-stu-id="520f7-111">Members</span></span>

<span data-ttu-id="520f7-112">**CIM \_ ProductSupport** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="520f7-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="520f7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="520f7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="520f7-114">屬性</span><span class="sxs-lookup"><span data-stu-id="520f7-114">Properties</span></span>

<span data-ttu-id="520f7-115">**CIM \_ ProductSupport** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="520f7-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="520f7-116">**產品**</span><span class="sxs-lookup"><span data-stu-id="520f7-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520f7-117">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="520f7-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="520f7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="520f7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="520f7-119">產品的參考。</span><span class="sxs-lookup"><span data-stu-id="520f7-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="520f7-120">**支援**</span><span class="sxs-lookup"><span data-stu-id="520f7-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520f7-121">資料類型： **CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="520f7-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="520f7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="520f7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="520f7-123">產品支援的參考。</span><span class="sxs-lookup"><span data-stu-id="520f7-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="520f7-124">備註</span><span class="sxs-lookup"><span data-stu-id="520f7-124">Remarks</span></span>

<span data-ttu-id="520f7-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="520f7-125">WMI does not implement this class.</span></span>

<span data-ttu-id="520f7-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="520f7-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="520f7-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="520f7-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="520f7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="520f7-128">Requirements</span></span>



| <span data-ttu-id="520f7-129">需求</span><span class="sxs-lookup"><span data-stu-id="520f7-129">Requirement</span></span> | <span data-ttu-id="520f7-130">值</span><span class="sxs-lookup"><span data-stu-id="520f7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="520f7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="520f7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="520f7-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520f7-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="520f7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="520f7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="520f7-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="520f7-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="520f7-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="520f7-135">Namespace</span></span><br/>                | <span data-ttu-id="520f7-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="520f7-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="520f7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="520f7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="520f7-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="520f7-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="520f7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="520f7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520f7-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520f7-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




