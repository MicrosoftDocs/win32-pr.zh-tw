---
description: CIM \_ ElementsLinked 關聯表示以實體連結連接在一起的實體元素。
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: CIM_ElementsLinked 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986260"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="7b4b3-103">CIM \_ ElementsLinked 類別</span><span class="sxs-lookup"><span data-stu-id="7b4b3-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="7b4b3-104">**CIM \_ ElementsLinked** 關聯表示以實體連結連接在一起的實體元素。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b4b3-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b4b3-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b4b3-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b4b3-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4b3-109">語法</span><span class="sxs-lookup"><span data-stu-id="7b4b3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7b4b3-110">成員</span><span class="sxs-lookup"><span data-stu-id="7b4b3-110">Members</span></span>

<span data-ttu-id="7b4b3-111">**CIM \_ ElementsLinked** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b4b3-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="7b4b3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7b4b3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b4b3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7b4b3-113">Properties</span></span>

<span data-ttu-id="7b4b3-114">**CIM \_ ElementsLinked** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b4b3-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="7b4b3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b4b3-116">資料類型： **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="7b4b3-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="7b4b3-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b4b3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b4b3-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="7b4b3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7b4b3-119">描述實體連結的 [**CIM \_ PhysicalLink**](cim-physicallink.md) 。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="7b4b3-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="7b4b3-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b4b3-121">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="7b4b3-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="7b4b3-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b4b3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b4b3-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="7b4b3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7b4b3-124">[**CIM \_ PhysicalElement**](cim-physicalelement.md) ，描述已連結的實體元素。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b4b3-125">備註</span><span class="sxs-lookup"><span data-stu-id="7b4b3-125">Remarks</span></span>

<span data-ttu-id="7b4b3-126">**Cim \_ ElementsLinked** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7b4b3-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7b4b3-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b4b3-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7b4b3-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4b3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b4b3-130">Requirements</span></span>



| <span data-ttu-id="7b4b3-131">需求</span><span class="sxs-lookup"><span data-stu-id="7b4b3-131">Requirement</span></span> | <span data-ttu-id="7b4b3-132">值</span><span class="sxs-lookup"><span data-stu-id="7b4b3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4b3-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b4b3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4b3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b4b3-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b4b3-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b4b3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4b3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b4b3-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b4b3-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b4b3-137">Namespace</span></span><br/>                | <span data-ttu-id="7b4b3-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b4b3-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b4b3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7b4b3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b4b3-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b4b3-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b4b3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4b3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b4b3-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4b3-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4b3-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b4b3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4b3-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="7b4b3-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

