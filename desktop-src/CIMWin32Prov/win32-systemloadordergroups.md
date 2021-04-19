---
description: Win32 \_ SystemLoadOrderGroups 關聯 WMI 類別會建立電腦系統和載入順序群組的關聯。
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Win32_SystemLoadOrderGroups 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970937"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="df36f-103">Win32 \_ SystemLoadOrderGroups 類別</span><span class="sxs-lookup"><span data-stu-id="df36f-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="df36f-104">**Win32 \_ SystemLoadOrderGroups** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立電腦系統和載入順序群組的關聯。</span><span class="sxs-lookup"><span data-stu-id="df36f-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="df36f-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="df36f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="df36f-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="df36f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df36f-107">語法</span><span class="sxs-lookup"><span data-stu-id="df36f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="df36f-108">成員</span><span class="sxs-lookup"><span data-stu-id="df36f-108">Members</span></span>

<span data-ttu-id="df36f-109">**Win32 \_ SystemLoadOrderGroups** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="df36f-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="df36f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="df36f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df36f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="df36f-111">Properties</span></span>

<span data-ttu-id="df36f-112">**Win32 \_ SystemLoadOrderGroups** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="df36f-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df36f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="df36f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df36f-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="df36f-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="df36f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="df36f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df36f-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="df36f-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="df36f-117">代表載入順序群組所在之電腦系統的實例參考。</span><span class="sxs-lookup"><span data-stu-id="df36f-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="df36f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="df36f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df36f-119">資料類型： **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="df36f-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="df36f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="df36f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df36f-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ LoadOrderGroup" ) </span><span class="sxs-lookup"><span data-stu-id="df36f-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="df36f-122">代表電腦系統上現有的載入順序群組之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="df36f-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df36f-123">備註</span><span class="sxs-lookup"><span data-stu-id="df36f-123">Remarks</span></span>

<span data-ttu-id="df36f-124">**Win32 \_ SystemLoadOrderGroups** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="df36f-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df36f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="df36f-125">Requirements</span></span>



| <span data-ttu-id="df36f-126">需求</span><span class="sxs-lookup"><span data-stu-id="df36f-126">Requirement</span></span> | <span data-ttu-id="df36f-127">值</span><span class="sxs-lookup"><span data-stu-id="df36f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df36f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df36f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df36f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df36f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df36f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df36f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df36f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df36f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df36f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="df36f-132">Namespace</span></span><br/>                | <span data-ttu-id="df36f-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="df36f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df36f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="df36f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df36f-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="df36f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df36f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="df36f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df36f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df36f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df36f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df36f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df36f-139">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="df36f-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="df36f-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="df36f-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
