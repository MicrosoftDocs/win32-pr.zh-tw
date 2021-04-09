---
description: Win32 \_ SystemDevices 關聯 WMI 類別會將電腦系統和安裝在該系統上的邏輯裝置產生關聯。
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847518"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="b67d9-103">Win32 \_ SystemDevices 類別</span><span class="sxs-lookup"><span data-stu-id="b67d9-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="b67d9-104">**Win32 \_ SystemDevices** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統和安裝在該系統上的邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b67d9-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="b67d9-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b67d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b67d9-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b67d9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67d9-107">語法</span><span class="sxs-lookup"><span data-stu-id="b67d9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b67d9-108">成員</span><span class="sxs-lookup"><span data-stu-id="b67d9-108">Members</span></span>

<span data-ttu-id="b67d9-109">**Win32 \_ SystemDevices** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b67d9-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="b67d9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b67d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b67d9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b67d9-111">Properties</span></span>

<span data-ttu-id="b67d9-112">**Win32 \_ SystemDevices** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b67d9-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b67d9-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b67d9-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b67d9-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="b67d9-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b67d9-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b67d9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b67d9-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="b67d9-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b67d9-117">代表邏輯裝置所在的電腦系統屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b67d9-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="b67d9-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b67d9-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b67d9-119">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b67d9-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b67d9-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b67d9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b67d9-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ LogicalDevice" ) </span><span class="sxs-lookup"><span data-stu-id="b67d9-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="b67d9-122">代表存在於電腦系統上的邏輯裝置屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b67d9-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b67d9-123">備註</span><span class="sxs-lookup"><span data-stu-id="b67d9-123">Remarks</span></span>

<span data-ttu-id="b67d9-124">**Win32 \_ SystemDevices** 類別衍生自 [**CIM \_ SystemDevice**](cim-systemdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b67d9-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b67d9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b67d9-125">Requirements</span></span>



| <span data-ttu-id="b67d9-126">需求</span><span class="sxs-lookup"><span data-stu-id="b67d9-126">Requirement</span></span> | <span data-ttu-id="b67d9-127">值</span><span class="sxs-lookup"><span data-stu-id="b67d9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b67d9-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b67d9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b67d9-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b67d9-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b67d9-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b67d9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b67d9-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b67d9-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b67d9-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b67d9-132">Namespace</span></span><br/>                | <span data-ttu-id="b67d9-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b67d9-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b67d9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b67d9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b67d9-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b67d9-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b67d9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b67d9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b67d9-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b67d9-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b67d9-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b67d9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67d9-139">**CIM \_ SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="b67d9-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="b67d9-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b67d9-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
