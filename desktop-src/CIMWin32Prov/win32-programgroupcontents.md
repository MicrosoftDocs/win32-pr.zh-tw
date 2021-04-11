---
description: Win32 \_ ProgramGroupContents 關聯 WMI 類別會關聯程式群組順序，以及其中包含的個別程式群組或專案。
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Win32_ProgramGroupContents 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025850"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="eacb6-103">Win32 \_ ProgramGroupContents 類別</span><span class="sxs-lookup"><span data-stu-id="eacb6-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="eacb6-104">**Win32 \_ ProgramGroupContents** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會關聯程式群組順序，以及其中包含的個別程式群組或專案。</span><span class="sxs-lookup"><span data-stu-id="eacb6-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="eacb6-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eacb6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eacb6-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="eacb6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eacb6-107">語法</span><span class="sxs-lookup"><span data-stu-id="eacb6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="eacb6-108">成員</span><span class="sxs-lookup"><span data-stu-id="eacb6-108">Members</span></span>

<span data-ttu-id="eacb6-109">**Win32 \_ ProgramGroupContents** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eacb6-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="eacb6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="eacb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eacb6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="eacb6-111">Properties</span></span>

<span data-ttu-id="eacb6-112">**Win32 \_ ProgramGroupContents** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eacb6-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eacb6-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eacb6-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eacb6-114">資料類型： **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="eacb6-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="eacb6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eacb6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eacb6-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ LogicalProgramGroup" ) </span><span class="sxs-lookup"><span data-stu-id="eacb6-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="eacb6-117">代表此關聯之邏輯程式群組的實例參考。</span><span class="sxs-lookup"><span data-stu-id="eacb6-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="eacb6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eacb6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eacb6-119">資料類型： **Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="eacb6-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="eacb6-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eacb6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eacb6-121">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ ProgramGroupOrItem" ) </span><span class="sxs-lookup"><span data-stu-id="eacb6-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="eacb6-122">代表此關聯之 [ **開始** ] 功能表群組或專案之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="eacb6-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eacb6-123">備註</span><span class="sxs-lookup"><span data-stu-id="eacb6-123">Remarks</span></span>

<span data-ttu-id="eacb6-124">**Win32 \_ ProgramGroupContents** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="eacb6-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eacb6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="eacb6-125">Requirements</span></span>



| <span data-ttu-id="eacb6-126">需求</span><span class="sxs-lookup"><span data-stu-id="eacb6-126">Requirement</span></span> | <span data-ttu-id="eacb6-127">值</span><span class="sxs-lookup"><span data-stu-id="eacb6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eacb6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eacb6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eacb6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eacb6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eacb6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eacb6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eacb6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eacb6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eacb6-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="eacb6-132">Namespace</span></span><br/>                | <span data-ttu-id="eacb6-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eacb6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eacb6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eacb6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eacb6-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eacb6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eacb6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eacb6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eacb6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eacb6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eacb6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eacb6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eacb6-139">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="eacb6-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="eacb6-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="eacb6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
