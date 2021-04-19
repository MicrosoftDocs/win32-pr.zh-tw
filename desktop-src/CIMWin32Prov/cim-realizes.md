---
description: CIM \_ 認識類別代表定義邏輯裝置與執行裝置之實體元件之間對應的關聯。
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: CIM_Realizes 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972771"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="f04a1-103">CIM \_ 意識類別</span><span class="sxs-lookup"><span data-stu-id="f04a1-103">CIM\_Realizes class</span></span>

<span data-ttu-id="f04a1-104">**CIM \_ 認識** 類別代表定義邏輯裝置與執行裝置之實體元件之間對應的關聯。</span><span class="sxs-lookup"><span data-stu-id="f04a1-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f04a1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f04a1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f04a1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f04a1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f04a1-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f04a1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f04a1-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f04a1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04a1-109">語法</span><span class="sxs-lookup"><span data-stu-id="f04a1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f04a1-110">成員</span><span class="sxs-lookup"><span data-stu-id="f04a1-110">Members</span></span>

<span data-ttu-id="f04a1-111">**CIM \_ 認識** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f04a1-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="f04a1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f04a1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f04a1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f04a1-113">Properties</span></span>

<span data-ttu-id="f04a1-114">**CIM \_ 認識** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f04a1-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f04a1-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="f04a1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04a1-116">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="f04a1-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="f04a1-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f04a1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04a1-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="f04a1-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f04a1-119">[**CIM \_ PhysicalElement**](cim-physicalelement.md) ，描述可執行裝置的實體元件。</span><span class="sxs-lookup"><span data-stu-id="f04a1-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="f04a1-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="f04a1-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04a1-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f04a1-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f04a1-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f04a1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04a1-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="f04a1-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f04a1-124">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="f04a1-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f04a1-125">備註</span><span class="sxs-lookup"><span data-stu-id="f04a1-125">Remarks</span></span>

<span data-ttu-id="f04a1-126">**Cim \_ 認識** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="f04a1-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f04a1-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f04a1-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f04a1-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f04a1-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f04a1-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f04a1-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04a1-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f04a1-130">Requirements</span></span>



| <span data-ttu-id="f04a1-131">需求</span><span class="sxs-lookup"><span data-stu-id="f04a1-131">Requirement</span></span> | <span data-ttu-id="f04a1-132">值</span><span class="sxs-lookup"><span data-stu-id="f04a1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f04a1-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f04a1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f04a1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f04a1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f04a1-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f04a1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f04a1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f04a1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f04a1-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="f04a1-137">Namespace</span></span><br/>                | <span data-ttu-id="f04a1-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f04a1-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f04a1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f04a1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f04a1-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f04a1-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f04a1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f04a1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f04a1-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f04a1-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f04a1-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f04a1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04a1-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="f04a1-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

