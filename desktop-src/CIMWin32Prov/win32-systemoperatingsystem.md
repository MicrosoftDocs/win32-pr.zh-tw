---
description: Win32 \_ SystemOperatingSystem 關聯 WMI 類別會將電腦系統與其作業系統建立關聯。
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Win32_SystemOperatingSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111493"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="3b428-103">Win32 \_ SystemOperatingSystem 類別</span><span class="sxs-lookup"><span data-stu-id="3b428-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="3b428-104">**Win32 \_ SystemOperatingSystem** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統與其作業系統建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3b428-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="3b428-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b428-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3b428-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="3b428-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b428-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b428-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3b428-108">成員</span><span class="sxs-lookup"><span data-stu-id="3b428-108">Members</span></span>

<span data-ttu-id="3b428-109">**Win32 \_ SystemOperatingSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b428-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="3b428-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3b428-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b428-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3b428-111">Properties</span></span>

<span data-ttu-id="3b428-112">**Win32 \_ SystemOperatingSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b428-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b428-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b428-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b428-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="3b428-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3b428-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b428-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b428-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="3b428-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3b428-117">[**Win32 的 \_**](win32-computersystemprocessor.md)系統程式描述，描述安裝作業系統的電腦系統屬性。</span><span class="sxs-lookup"><span data-stu-id="3b428-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="3b428-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b428-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b428-119">資料類型： **Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="3b428-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3b428-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b428-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b428-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ 作業系統" ) </span><span class="sxs-lookup"><span data-stu-id="3b428-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3b428-122">[**Win32 \_ 作業系統**](win32-operatingsystem.md)，描述在此電腦系統上執行之作業系統的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b428-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3b428-123">**PrimaryOS**</span><span class="sxs-lookup"><span data-stu-id="3b428-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b428-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b428-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b428-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b428-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b428-126">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 作業系統 \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="3b428-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="3b428-127">若 **為 TRUE**，則表示已安裝的作業系統是電腦系統的預設作業系統。</span><span class="sxs-lookup"><span data-stu-id="3b428-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="3b428-128">這個屬性繼承自 [**CIM \_ InstalledOS**](cim-installedos.md)。</span><span class="sxs-lookup"><span data-stu-id="3b428-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b428-129">備註</span><span class="sxs-lookup"><span data-stu-id="3b428-129">Remarks</span></span>

<span data-ttu-id="3b428-130">**Win32 \_ SystemOperatingSystem** 類別衍生自 [**CIM \_ InstalledOS**](cim-installedos.md)。</span><span class="sxs-lookup"><span data-stu-id="3b428-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b428-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b428-131">Requirements</span></span>



| <span data-ttu-id="3b428-132">需求</span><span class="sxs-lookup"><span data-stu-id="3b428-132">Requirement</span></span> | <span data-ttu-id="3b428-133">值</span><span class="sxs-lookup"><span data-stu-id="3b428-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b428-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b428-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3b428-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b428-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b428-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b428-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3b428-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b428-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b428-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b428-138">Namespace</span></span><br/>                | <span data-ttu-id="3b428-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b428-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b428-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3b428-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b428-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b428-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b428-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3b428-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b428-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b428-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b428-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b428-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b428-145">**CIM \_ InstalledOS**</span><span class="sxs-lookup"><span data-stu-id="3b428-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="3b428-146">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="3b428-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
