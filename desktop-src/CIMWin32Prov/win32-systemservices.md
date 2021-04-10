---
description: Win32 \_ SystemServices 關聯 WMI 類別會將電腦系統和存在於系統上的服務程式產生關聯。
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Win32_SystemServices 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688872"
---
# <a name="win32_systemservices-class"></a><span data-ttu-id="8b54d-103">Win32 \_ SystemServices 類別</span><span class="sxs-lookup"><span data-stu-id="8b54d-103">Win32\_SystemServices class</span></span>

<span data-ttu-id="8b54d-104">**Win32 \_ SystemServices** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統和存在於系統上的服務程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8b54d-104">The **Win32\_SystemServices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a service program that exists on the system.</span></span>

<span data-ttu-id="8b54d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8b54d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8b54d-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="8b54d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b54d-107">語法</span><span class="sxs-lookup"><span data-stu-id="8b54d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8b54d-108">成員</span><span class="sxs-lookup"><span data-stu-id="8b54d-108">Members</span></span>

<span data-ttu-id="8b54d-109">**Win32 \_ SystemServices** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8b54d-109">The **Win32\_SystemServices** class has these types of members:</span></span>

-   [<span data-ttu-id="8b54d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8b54d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b54d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8b54d-111">Properties</span></span>

<span data-ttu-id="8b54d-112">**Win32 \_ SystemServices** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b54d-112">The **Win32\_SystemServices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b54d-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8b54d-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b54d-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="8b54d-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8b54d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b54d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b54d-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="8b54d-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="8b54d-117">代表服務所在電腦系統屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8b54d-117">Reference to the instance representing the properties of the computer system on which the service exists.</span></span>

</dd> <dt>

<span data-ttu-id="8b54d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8b54d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b54d-119">資料類型： **Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="8b54d-119">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="8b54d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b54d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b54d-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ 服務" ) </span><span class="sxs-lookup"><span data-stu-id="8b54d-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="8b54d-122">代表存在於電腦系統上之服務的實例參考。</span><span class="sxs-lookup"><span data-stu-id="8b54d-122">Reference to the instance representing the service that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b54d-123">備註</span><span class="sxs-lookup"><span data-stu-id="8b54d-123">Remarks</span></span>

<span data-ttu-id="8b54d-124">**Win32 \_ SystemServices** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="8b54d-124">The **Win32\_SystemServices** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b54d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b54d-125">Requirements</span></span>



| <span data-ttu-id="8b54d-126">需求</span><span class="sxs-lookup"><span data-stu-id="8b54d-126">Requirement</span></span> | <span data-ttu-id="8b54d-127">值</span><span class="sxs-lookup"><span data-stu-id="8b54d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b54d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b54d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b54d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b54d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b54d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b54d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b54d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b54d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b54d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="8b54d-132">Namespace</span></span><br/>                | <span data-ttu-id="8b54d-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b54d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b54d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8b54d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b54d-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b54d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b54d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8b54d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b54d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b54d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b54d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b54d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b54d-139">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="8b54d-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="8b54d-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="8b54d-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
