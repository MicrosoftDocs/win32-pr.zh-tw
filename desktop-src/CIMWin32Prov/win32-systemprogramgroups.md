---
description: Win32 \_ SystemProgramGroups 關聯 WMI 類別會建立電腦系統和邏輯程式群組的關聯。
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Win32_SystemProgramGroups 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111480"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="7c854-103">Win32 \_ SystemProgramGroups 類別</span><span class="sxs-lookup"><span data-stu-id="7c854-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="7c854-104">**Win32 \_ SystemProgramGroups** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立電腦系統和邏輯程式群組的關聯。</span><span class="sxs-lookup"><span data-stu-id="7c854-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="7c854-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7c854-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7c854-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="7c854-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c854-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c854-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="7c854-108">成員</span><span class="sxs-lookup"><span data-stu-id="7c854-108">Members</span></span>

<span data-ttu-id="7c854-109">**Win32 \_ SystemProgramGroups** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7c854-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="7c854-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7c854-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c854-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7c854-111">Properties</span></span>

<span data-ttu-id="7c854-112">**Win32 \_ SystemProgramGroups** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7c854-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c854-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c854-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c854-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="7c854-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7c854-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7c854-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c854-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI Win32 \| \_ " ) </span><span class="sxs-lookup"><span data-stu-id="7c854-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7c854-117">代表包含邏輯程式群組之電腦系統的實例參考。</span><span class="sxs-lookup"><span data-stu-id="7c854-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="7c854-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="7c854-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c854-119">資料類型： **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="7c854-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="7c854-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7c854-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c854-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ LogicalProgramGroup" ) </span><span class="sxs-lookup"><span data-stu-id="7c854-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="7c854-122">代表電腦系統上的邏輯程式群組之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="7c854-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c854-123">備註</span><span class="sxs-lookup"><span data-stu-id="7c854-123">Remarks</span></span>

<span data-ttu-id="7c854-124">**Win32 \_ SystemProgramGroups** 類別衍生自 [**win32 \_ SystemSetting**](win32-systemsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="7c854-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c854-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c854-125">Requirements</span></span>



| <span data-ttu-id="7c854-126">需求</span><span class="sxs-lookup"><span data-stu-id="7c854-126">Requirement</span></span> | <span data-ttu-id="7c854-127">值</span><span class="sxs-lookup"><span data-stu-id="7c854-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c854-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c854-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c854-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c854-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c854-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c854-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c854-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c854-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c854-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="7c854-132">Namespace</span></span><br/>                | <span data-ttu-id="7c854-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7c854-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c854-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7c854-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c854-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c854-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c854-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c854-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c854-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c854-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c854-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c854-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c854-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="7c854-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="7c854-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="7c854-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
