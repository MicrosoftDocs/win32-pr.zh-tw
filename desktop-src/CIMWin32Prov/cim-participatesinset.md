---
description: CIM \_ ParticipatesInSet 類別會識別應該一起取代的實體元素。
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: CIM_ParticipatesInSet 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847428"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="b9ada-103">CIM \_ ParticipatesInSet 類別</span><span class="sxs-lookup"><span data-stu-id="b9ada-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="b9ada-104">**CIM \_ ParticipatesInSet** 類別會識別應該一起取代的實體元素。</span><span class="sxs-lookup"><span data-stu-id="b9ada-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9ada-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b9ada-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9ada-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b9ada-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9ada-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9ada-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b9ada-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b9ada-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ada-109">語法</span><span class="sxs-lookup"><span data-stu-id="b9ada-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="b9ada-110">成員</span><span class="sxs-lookup"><span data-stu-id="b9ada-110">Members</span></span>

<span data-ttu-id="b9ada-111">**CIM \_ ParticipatesInSet** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b9ada-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="b9ada-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b9ada-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9ada-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b9ada-113">Properties</span></span>

<span data-ttu-id="b9ada-114">**CIM \_ ParticipatesInSet** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b9ada-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9ada-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9ada-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ada-116">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="b9ada-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="b9ada-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b9ada-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9ada-118">實體專案的參考，該實體專案應以其他元素取代，做為集合。</span><span class="sxs-lookup"><span data-stu-id="b9ada-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="b9ada-119">**設定**</span><span class="sxs-lookup"><span data-stu-id="b9ada-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ada-120">資料類型： **CIM \_ ReplacementSet**</span><span class="sxs-lookup"><span data-stu-id="b9ada-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="b9ada-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b9ada-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9ada-122">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b9ada-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b9ada-123">取代元素集的參考。</span><span class="sxs-lookup"><span data-stu-id="b9ada-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9ada-124">備註</span><span class="sxs-lookup"><span data-stu-id="b9ada-124">Remarks</span></span>

<span data-ttu-id="b9ada-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b9ada-125">WMI does not implement this class.</span></span>

<span data-ttu-id="b9ada-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b9ada-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9ada-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b9ada-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ada-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9ada-128">Requirements</span></span>



| <span data-ttu-id="b9ada-129">需求</span><span class="sxs-lookup"><span data-stu-id="b9ada-129">Requirement</span></span> | <span data-ttu-id="b9ada-130">值</span><span class="sxs-lookup"><span data-stu-id="b9ada-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ada-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9ada-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ada-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9ada-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9ada-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9ada-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ada-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9ada-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9ada-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9ada-135">Namespace</span></span><br/>                | <span data-ttu-id="b9ada-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b9ada-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9ada-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b9ada-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9ada-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9ada-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9ada-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b9ada-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9ada-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ada-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

