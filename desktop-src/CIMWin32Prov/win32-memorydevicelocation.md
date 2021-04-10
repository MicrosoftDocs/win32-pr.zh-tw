---
description: Win32 \_ MemoryDeviceLocation 關聯 WMI 類別會將記憶體裝置和其所在的實體記憶體產生關聯。
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Win32_MemoryDeviceLocation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936138"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="aef84-103">Win32 \_ MemoryDeviceLocation 類別</span><span class="sxs-lookup"><span data-stu-id="aef84-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="aef84-104">**Win32 \_ MemoryDeviceLocation** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將記憶體裝置和其所在的實體記憶體產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aef84-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="aef84-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aef84-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aef84-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="aef84-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef84-107">語法</span><span class="sxs-lookup"><span data-stu-id="aef84-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="aef84-108">成員</span><span class="sxs-lookup"><span data-stu-id="aef84-108">Members</span></span>

<span data-ttu-id="aef84-109">**Win32 \_ MemoryDeviceLocation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aef84-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="aef84-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aef84-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aef84-111">屬性</span><span class="sxs-lookup"><span data-stu-id="aef84-111">Properties</span></span>

<span data-ttu-id="aef84-112">**Win32 \_ MemoryDeviceLocation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aef84-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aef84-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="aef84-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef84-114">資料類型： **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="aef84-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="aef84-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef84-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef84-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ PhysicalMemory" ) </span><span class="sxs-lookup"><span data-stu-id="aef84-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="aef84-117">[**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) ，代表包含記憶體裝置的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="aef84-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="aef84-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="aef84-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef84-119">資料類型： **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="aef84-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="aef84-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef84-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef84-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 MemoryDevice」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="aef84-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="aef84-122">**Win32 \_ MemoryDeviceLocation** ，表示實體記憶體中現有的記憶體裝置。</span><span class="sxs-lookup"><span data-stu-id="aef84-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aef84-123">備註</span><span class="sxs-lookup"><span data-stu-id="aef84-123">Remarks</span></span>

<span data-ttu-id="aef84-124">**Win32 \_ MemoryDeviceLocation** 類別衍生自 [**CIM \_**](cim-realizes.md)。</span><span class="sxs-lookup"><span data-stu-id="aef84-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aef84-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="aef84-125">Requirements</span></span>



| <span data-ttu-id="aef84-126">需求</span><span class="sxs-lookup"><span data-stu-id="aef84-126">Requirement</span></span> | <span data-ttu-id="aef84-127">值</span><span class="sxs-lookup"><span data-stu-id="aef84-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aef84-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aef84-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aef84-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aef84-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aef84-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aef84-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aef84-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aef84-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aef84-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="aef84-132">Namespace</span></span><br/>                | <span data-ttu-id="aef84-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aef84-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aef84-134">MOF</span><span class="sxs-lookup"><span data-stu-id="aef84-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef84-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aef84-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef84-136">DLL</span><span class="sxs-lookup"><span data-stu-id="aef84-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef84-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef84-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef84-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aef84-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef84-139">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="aef84-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="aef84-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="aef84-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

