---
description: CIM \_ AssociateMemory 類別會將已安裝或相關聯的記憶體（例如快取記憶體）與邏輯裝置產生關聯。
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: CIM_AssociatedMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468405"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="26c6c-103">CIM \_ AssociatedMemory 類別</span><span class="sxs-lookup"><span data-stu-id="26c6c-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="26c6c-104">**CIM \_ AssociateMemory** 類別會將已安裝或相關聯的記憶體（例如快取記憶體）與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="26c6c-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26c6c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="26c6c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26c6c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="26c6c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26c6c-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="26c6c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="26c6c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="26c6c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c6c-109">語法</span><span class="sxs-lookup"><span data-stu-id="26c6c-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="26c6c-110">成員</span><span class="sxs-lookup"><span data-stu-id="26c6c-110">Members</span></span>

<span data-ttu-id="26c6c-111">**CIM \_ AssociatedMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26c6c-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="26c6c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="26c6c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26c6c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="26c6c-113">Properties</span></span>

<span data-ttu-id="26c6c-114">**CIM \_ AssociatedMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="26c6c-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26c6c-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="26c6c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26c6c-116">資料類型： **CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="26c6c-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="26c6c-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26c6c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26c6c-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="26c6c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="26c6c-119">[**CIM \_ 記憶體**](cim-memory.md)，描述安裝在裝置上或與裝置相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="26c6c-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="26c6c-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="26c6c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26c6c-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="26c6c-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="26c6c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26c6c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26c6c-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="26c6c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="26c6c-124">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="26c6c-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26c6c-125">備註</span><span class="sxs-lookup"><span data-stu-id="26c6c-125">Remarks</span></span>

<span data-ttu-id="26c6c-126">**Cim \_ AssociatedMemory** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="26c6c-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="26c6c-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="26c6c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="26c6c-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="26c6c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26c6c-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="26c6c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26c6c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="26c6c-130">Requirements</span></span>



| <span data-ttu-id="26c6c-131">需求</span><span class="sxs-lookup"><span data-stu-id="26c6c-131">Requirement</span></span> | <span data-ttu-id="26c6c-132">值</span><span class="sxs-lookup"><span data-stu-id="26c6c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26c6c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26c6c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26c6c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26c6c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26c6c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26c6c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26c6c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26c6c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26c6c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="26c6c-137">Namespace</span></span><br/>                | <span data-ttu-id="26c6c-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="26c6c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26c6c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="26c6c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26c6c-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="26c6c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26c6c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="26c6c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c6c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c6c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c6c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26c6c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c6c-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="26c6c-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

