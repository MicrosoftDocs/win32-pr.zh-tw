---
description: Win32 \_ SystemProcesses 關聯 WMI 類別會將電腦系統和在該系統上執行的處理常式產生關聯。
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Win32_SystemProcesses 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025927"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="e13bd-103">Win32 \_ SystemProcesses 類別</span><span class="sxs-lookup"><span data-stu-id="e13bd-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="e13bd-104">**Win32 \_ SystemProcesses** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統和在該系統上執行的處理常式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e13bd-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="e13bd-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e13bd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e13bd-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="e13bd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13bd-107">語法</span><span class="sxs-lookup"><span data-stu-id="e13bd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e13bd-108">成員</span><span class="sxs-lookup"><span data-stu-id="e13bd-108">Members</span></span>

<span data-ttu-id="e13bd-109">**Win32 \_ SystemProcesses** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e13bd-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="e13bd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e13bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e13bd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e13bd-111">Properties</span></span>

<span data-ttu-id="e13bd-112">**Win32 \_ SystemProcesses** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e13bd-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e13bd-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e13bd-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13bd-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="e13bd-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e13bd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e13bd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e13bd-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="e13bd-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="e13bd-117">代表執行進程之電腦系統的實例參考。</span><span class="sxs-lookup"><span data-stu-id="e13bd-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="e13bd-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e13bd-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13bd-119">資料類型： **Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="e13bd-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="e13bd-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e13bd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e13bd-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Process" ) </span><span class="sxs-lookup"><span data-stu-id="e13bd-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="e13bd-122">代表電腦系統上執行之進程的實例參考。</span><span class="sxs-lookup"><span data-stu-id="e13bd-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e13bd-123">備註</span><span class="sxs-lookup"><span data-stu-id="e13bd-123">Remarks</span></span>

<span data-ttu-id="e13bd-124">**Win32 \_ SystemProcesses** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e13bd-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e13bd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e13bd-125">Requirements</span></span>



| <span data-ttu-id="e13bd-126">需求</span><span class="sxs-lookup"><span data-stu-id="e13bd-126">Requirement</span></span> | <span data-ttu-id="e13bd-127">值</span><span class="sxs-lookup"><span data-stu-id="e13bd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e13bd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e13bd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e13bd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e13bd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e13bd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e13bd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e13bd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e13bd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e13bd-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="e13bd-132">Namespace</span></span><br/>                | <span data-ttu-id="e13bd-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e13bd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e13bd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e13bd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e13bd-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e13bd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e13bd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e13bd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13bd-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e13bd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13bd-139">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="e13bd-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="e13bd-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="e13bd-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
