---
description: CIM \_ ProductSoftwareFeatures 關聯會識別特定產品的軟體功能。
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: CIM_ProductSoftwareFeatures 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973567"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="9db22-103">CIM \_ ProductSoftwareFeatures 類別</span><span class="sxs-lookup"><span data-stu-id="9db22-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="9db22-104">**CIM \_ ProductSoftwareFeatures** 關聯會識別特定產品的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="9db22-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9db22-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9db22-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9db22-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9db22-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9db22-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9db22-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9db22-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9db22-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db22-109">語法</span><span class="sxs-lookup"><span data-stu-id="9db22-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="9db22-110">成員</span><span class="sxs-lookup"><span data-stu-id="9db22-110">Members</span></span>

<span data-ttu-id="9db22-111">**CIM \_ ProductSoftwareFeatures** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9db22-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="9db22-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9db22-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9db22-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9db22-113">Properties</span></span>

<span data-ttu-id="9db22-114">**CIM \_ ProductSoftwareFeatures** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9db22-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9db22-115">**元件**</span><span class="sxs-lookup"><span data-stu-id="9db22-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9db22-116">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="9db22-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="9db22-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9db22-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9db22-118">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="9db22-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9db22-119">元件的參考。</span><span class="sxs-lookup"><span data-stu-id="9db22-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="9db22-120">**產品**</span><span class="sxs-lookup"><span data-stu-id="9db22-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9db22-121">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="9db22-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="9db22-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9db22-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9db22-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9db22-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9db22-124">產品的參考。</span><span class="sxs-lookup"><span data-stu-id="9db22-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9db22-125">備註</span><span class="sxs-lookup"><span data-stu-id="9db22-125">Remarks</span></span>

<span data-ttu-id="9db22-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9db22-126">WMI does not implement this class.</span></span> <span data-ttu-id="9db22-127">針對衍生自 **CIM \_ PRODUCTSOFTWAREFEATURES** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9db22-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9db22-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9db22-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9db22-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9db22-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db22-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9db22-130">Requirements</span></span>



| <span data-ttu-id="9db22-131">需求</span><span class="sxs-lookup"><span data-stu-id="9db22-131">Requirement</span></span> | <span data-ttu-id="9db22-132">值</span><span class="sxs-lookup"><span data-stu-id="9db22-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db22-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9db22-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9db22-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9db22-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9db22-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9db22-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9db22-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9db22-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9db22-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="9db22-137">Namespace</span></span><br/>                | <span data-ttu-id="9db22-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9db22-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9db22-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9db22-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9db22-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9db22-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9db22-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9db22-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db22-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db22-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

