---
description: CIM \_ ReplacementSet 類別會匯總必須一起取代的實體元素。
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: CIM_ReplacementSet 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110253"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="b3eab-103">CIM \_ ReplacementSet 類別</span><span class="sxs-lookup"><span data-stu-id="b3eab-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="b3eab-104">**CIM \_ ReplacementSet** 類別會匯總必須一起取代的實體元素。</span><span class="sxs-lookup"><span data-stu-id="b3eab-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="b3eab-105">例如，更換記憶卡時，也可以移除並取代元件記憶體晶片。</span><span class="sxs-lookup"><span data-stu-id="b3eab-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="b3eab-106">或者，這個關聯可以用來取代或升級一組記憶體晶片。</span><span class="sxs-lookup"><span data-stu-id="b3eab-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3eab-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b3eab-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3eab-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b3eab-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3eab-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3eab-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3eab-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b3eab-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3eab-111">語法</span><span class="sxs-lookup"><span data-stu-id="b3eab-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b3eab-112">成員</span><span class="sxs-lookup"><span data-stu-id="b3eab-112">Members</span></span>

<span data-ttu-id="b3eab-113">**CIM \_ ReplacementSet** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b3eab-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="b3eab-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b3eab-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3eab-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b3eab-115">Properties</span></span>

<span data-ttu-id="b3eab-116">**CIM \_ ReplacementSet** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b3eab-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3eab-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="b3eab-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3eab-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3eab-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3eab-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3eab-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3eab-120">指定與這個類別相關之資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="b3eab-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="b3eab-121">集合的用途，或元件元素的取代相關資訊，可以包含在此屬性中。</span><span class="sxs-lookup"><span data-stu-id="b3eab-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="b3eab-122">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b3eab-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3eab-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3eab-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3eab-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3eab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3eab-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b3eab-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b3eab-126">為此屬性定義標籤的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="b3eab-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="b3eab-127">這個屬性是物件的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b3eab-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3eab-128">備註</span><span class="sxs-lookup"><span data-stu-id="b3eab-128">Remarks</span></span>

<span data-ttu-id="b3eab-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b3eab-129">WMI does not implement this class.</span></span>

<span data-ttu-id="b3eab-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b3eab-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3eab-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b3eab-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3eab-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3eab-132">Requirements</span></span>



| <span data-ttu-id="b3eab-133">需求</span><span class="sxs-lookup"><span data-stu-id="b3eab-133">Requirement</span></span> | <span data-ttu-id="b3eab-134">值</span><span class="sxs-lookup"><span data-stu-id="b3eab-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3eab-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3eab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3eab-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3eab-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3eab-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3eab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3eab-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3eab-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3eab-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3eab-139">Namespace</span></span><br/>                | <span data-ttu-id="b3eab-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b3eab-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3eab-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b3eab-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3eab-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3eab-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3eab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b3eab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3eab-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3eab-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

