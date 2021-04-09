---
description: Win32 \_ SystemBIOS 關聯 WMI 類別會將電腦系統 (，包括啟動屬性、時區、開機設定或系統管理密碼) ，以及系統 BIOS (服務、語言和系統管理屬性) 。
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847519"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="f4609-103">Win32 \_ SystemBIOS 類別</span><span class="sxs-lookup"><span data-stu-id="f4609-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="f4609-104">**Win32 \_ SystemBIOS** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統 (，包括啟動屬性、時區、開機設定或系統管理密碼) ，以及系統 BIOS (服務、語言和系統管理屬性) 。</span><span class="sxs-lookup"><span data-stu-id="f4609-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="f4609-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4609-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f4609-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f4609-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4609-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4609-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f4609-108">成員</span><span class="sxs-lookup"><span data-stu-id="f4609-108">Members</span></span>

<span data-ttu-id="f4609-109">**Win32 \_ SystemBIOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f4609-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="f4609-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f4609-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4609-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f4609-111">Properties</span></span>

<span data-ttu-id="f4609-112">**Win32 \_ SystemBIOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f4609-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4609-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f4609-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4609-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="f4609-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f4609-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4609-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4609-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="f4609-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="f4609-117">包含關聯 BIOS 的 [**Win32 \_**](win32-computersystemprocessor.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="f4609-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="f4609-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f4609-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4609-119">資料類型： **Win32 \_ BIOS**</span><span class="sxs-lookup"><span data-stu-id="f4609-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="f4609-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4609-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4609-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ BIOS" ) </span><span class="sxs-lookup"><span data-stu-id="f4609-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="f4609-122">此關聯的電腦系統中包含的 [**Win32 \_ BIOS**](win32-bios.md) 。</span><span class="sxs-lookup"><span data-stu-id="f4609-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4609-123">備註</span><span class="sxs-lookup"><span data-stu-id="f4609-123">Remarks</span></span>

<span data-ttu-id="f4609-124">**Win32 \_ SystemBIOS** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="f4609-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4609-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4609-125">Requirements</span></span>



| <span data-ttu-id="f4609-126">需求</span><span class="sxs-lookup"><span data-stu-id="f4609-126">Requirement</span></span> | <span data-ttu-id="f4609-127">值</span><span class="sxs-lookup"><span data-stu-id="f4609-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4609-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4609-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4609-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4609-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4609-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4609-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4609-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4609-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4609-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="f4609-132">Namespace</span></span><br/>                | <span data-ttu-id="f4609-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f4609-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4609-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f4609-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4609-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4609-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4609-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f4609-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4609-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4609-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4609-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4609-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4609-139">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="f4609-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="f4609-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="f4609-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
