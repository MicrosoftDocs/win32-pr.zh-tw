---
description: Win32 \_ LoadOrderGroupServiceMembers 關聯 WMI 類別會關聯載入順序群組和基底服務。
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceMembers 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847557"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="bd591-103">Win32 \_ LoadOrderGroupServiceMembers 類別</span><span class="sxs-lookup"><span data-stu-id="bd591-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="bd591-104">**Win32 \_ LoadOrderGroupServiceMembers** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯載入順序群組和基底服務。</span><span class="sxs-lookup"><span data-stu-id="bd591-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="bd591-105">[**Win32 \_>systemdriver**](win32-systemdriver.md) 物件是該載入順序群組的成員。</span><span class="sxs-lookup"><span data-stu-id="bd591-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="bd591-106">並非所有的服務都是群組的成員，而且並非所有的群組都有服務。</span><span class="sxs-lookup"><span data-stu-id="bd591-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="bd591-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd591-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bd591-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bd591-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd591-109">語法</span><span class="sxs-lookup"><span data-stu-id="bd591-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="bd591-110">成員</span><span class="sxs-lookup"><span data-stu-id="bd591-110">Members</span></span>

<span data-ttu-id="bd591-111">**Win32 \_ LoadOrderGroupServiceMembers** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bd591-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="bd591-112">屬性</span><span class="sxs-lookup"><span data-stu-id="bd591-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd591-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bd591-113">Properties</span></span>

<span data-ttu-id="bd591-114">**Win32 \_ LoadOrderGroupServiceMembers** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bd591-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd591-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bd591-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd591-116">資料類型： **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="bd591-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="bd591-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd591-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd591-118">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LoadOrderGroup" ) </span><span class="sxs-lookup"><span data-stu-id="bd591-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="bd591-119">實例的參考，表示與基底服務相關聯的載入順序群組屬性。</span><span class="sxs-lookup"><span data-stu-id="bd591-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="bd591-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bd591-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd591-121">資料類型： **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="bd591-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="bd591-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd591-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd591-123">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ BaseService" ) </span><span class="sxs-lookup"><span data-stu-id="bd591-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="bd591-124">代表屬於載入順序群組成員之服務的實例參考。</span><span class="sxs-lookup"><span data-stu-id="bd591-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd591-125">備註</span><span class="sxs-lookup"><span data-stu-id="bd591-125">Remarks</span></span>

<span data-ttu-id="bd591-126">**Win32 \_ LoadOrderGroupServiceMembers** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="bd591-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd591-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd591-127">Requirements</span></span>



| <span data-ttu-id="bd591-128">需求</span><span class="sxs-lookup"><span data-stu-id="bd591-128">Requirement</span></span> | <span data-ttu-id="bd591-129">值</span><span class="sxs-lookup"><span data-stu-id="bd591-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd591-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd591-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd591-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd591-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd591-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd591-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd591-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd591-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd591-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd591-134">Namespace</span></span><br/>                | <span data-ttu-id="bd591-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bd591-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd591-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bd591-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd591-137"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd591-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd591-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bd591-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd591-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd591-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd591-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd591-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd591-141">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="bd591-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="bd591-142">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd591-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

