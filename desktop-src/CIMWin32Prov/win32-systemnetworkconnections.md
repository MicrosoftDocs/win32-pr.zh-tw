---
description: Win32 \_ SystemNetworkConnections 關聯 WMI 類別會將網路連線及其所在的電腦系統建立關聯。
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Win32_SystemNetworkConnections 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111496"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="adc3a-103">Win32 \_ SystemNetworkConnections 類別</span><span class="sxs-lookup"><span data-stu-id="adc3a-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="adc3a-104">**Win32 \_ SystemNetworkConnections** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將網路連線及其所在的電腦系統建立關聯。</span><span class="sxs-lookup"><span data-stu-id="adc3a-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="adc3a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="adc3a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="adc3a-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="adc3a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc3a-107">語法</span><span class="sxs-lookup"><span data-stu-id="adc3a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="adc3a-108">成員</span><span class="sxs-lookup"><span data-stu-id="adc3a-108">Members</span></span>

<span data-ttu-id="adc3a-109">**Win32 \_ SystemNetworkConnections** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="adc3a-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="adc3a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="adc3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adc3a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="adc3a-111">Properties</span></span>

<span data-ttu-id="adc3a-112">**Win32 \_ SystemNetworkConnections** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="adc3a-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adc3a-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="adc3a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc3a-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="adc3a-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="adc3a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="adc3a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc3a-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="adc3a-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="adc3a-117">代表連接到網路之電腦系統的實例參考。</span><span class="sxs-lookup"><span data-stu-id="adc3a-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="adc3a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="adc3a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc3a-119">資料類型： **Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="adc3a-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="adc3a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="adc3a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc3a-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkConnection" ) </span><span class="sxs-lookup"><span data-stu-id="adc3a-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="adc3a-122">代表此電腦系統的網路連接之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="adc3a-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adc3a-123">備註</span><span class="sxs-lookup"><span data-stu-id="adc3a-123">Remarks</span></span>

<span data-ttu-id="adc3a-124">**Win32 \_ SystemNetworkConnections** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="adc3a-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adc3a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="adc3a-125">Requirements</span></span>



| <span data-ttu-id="adc3a-126">需求</span><span class="sxs-lookup"><span data-stu-id="adc3a-126">Requirement</span></span> | <span data-ttu-id="adc3a-127">值</span><span class="sxs-lookup"><span data-stu-id="adc3a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adc3a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adc3a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="adc3a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adc3a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="adc3a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adc3a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="adc3a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adc3a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="adc3a-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="adc3a-132">Namespace</span></span><br/>                | <span data-ttu-id="adc3a-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="adc3a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="adc3a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="adc3a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adc3a-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="adc3a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="adc3a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="adc3a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adc3a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc3a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc3a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adc3a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc3a-139">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="adc3a-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="adc3a-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="adc3a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
