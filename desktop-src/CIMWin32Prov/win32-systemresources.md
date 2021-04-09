---
description: Win32 \_ SystemResources 關聯 WMI 類別會將系統資源與其所在的電腦系統產生關聯。
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Win32_SystemResources 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936284"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="54d2e-103">Win32 \_ SystemResources 類別</span><span class="sxs-lookup"><span data-stu-id="54d2e-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="54d2e-104">**Win32 \_ SystemResources** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將系統資源與其所在的電腦系統產生關聯。</span><span class="sxs-lookup"><span data-stu-id="54d2e-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="54d2e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="54d2e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="54d2e-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="54d2e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="54d2e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="54d2e-108">成員</span><span class="sxs-lookup"><span data-stu-id="54d2e-108">Members</span></span>

<span data-ttu-id="54d2e-109">**Win32 \_ SystemResources** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="54d2e-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="54d2e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="54d2e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54d2e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="54d2e-111">Properties</span></span>

<span data-ttu-id="54d2e-112">**Win32 \_ SystemResources** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="54d2e-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54d2e-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="54d2e-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2e-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="54d2e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="54d2e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="54d2e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d2e-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="54d2e-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="54d2e-117">此實例的參考，代表資源所在的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="54d2e-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="54d2e-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="54d2e-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2e-119">資料類型： **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="54d2e-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="54d2e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="54d2e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d2e-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ SystemResource" ) </span><span class="sxs-lookup"><span data-stu-id="54d2e-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="54d2e-122">代表資源 (（例如 i/o 服務和記憶體資源）之實例的參考，) 可在電腦系統上使用。</span><span class="sxs-lookup"><span data-stu-id="54d2e-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54d2e-123">備註</span><span class="sxs-lookup"><span data-stu-id="54d2e-123">Remarks</span></span>

<span data-ttu-id="54d2e-124">**Win32 \_ SystemResources** 類別衍生自 [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="54d2e-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54d2e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="54d2e-125">Requirements</span></span>



| <span data-ttu-id="54d2e-126">需求</span><span class="sxs-lookup"><span data-stu-id="54d2e-126">Requirement</span></span> | <span data-ttu-id="54d2e-127">值</span><span class="sxs-lookup"><span data-stu-id="54d2e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d2e-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54d2e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="54d2e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54d2e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54d2e-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54d2e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="54d2e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54d2e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54d2e-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="54d2e-132">Namespace</span></span><br/>                | <span data-ttu-id="54d2e-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="54d2e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54d2e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="54d2e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54d2e-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="54d2e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54d2e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54d2e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54d2e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d2e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d2e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54d2e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d2e-139">**CIM \_ ComputerSystemResource**</span><span class="sxs-lookup"><span data-stu-id="54d2e-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="54d2e-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="54d2e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
