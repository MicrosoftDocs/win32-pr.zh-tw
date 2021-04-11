---
description: Win32 \_ MemoryDeviceArray 關聯 WMI 類別會將記憶體裝置和其所在的記憶體陣列產生關聯。
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Win32_MemoryDeviceArray 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847080"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="ded96-103">Win32 \_ MemoryDeviceArray 類別</span><span class="sxs-lookup"><span data-stu-id="ded96-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="ded96-104">**Win32 \_ MemoryDeviceArray** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將記憶體裝置和其所在的記憶體陣列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ded96-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="ded96-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ded96-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ded96-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ded96-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded96-107">語法</span><span class="sxs-lookup"><span data-stu-id="ded96-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ded96-108">成員</span><span class="sxs-lookup"><span data-stu-id="ded96-108">Members</span></span>

<span data-ttu-id="ded96-109">**Win32 \_ MemoryDeviceArray** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ded96-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="ded96-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ded96-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ded96-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ded96-111">Properties</span></span>

<span data-ttu-id="ded96-112">**Win32 \_ MemoryDeviceArray** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ded96-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ded96-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ded96-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ded96-114">資料類型： **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="ded96-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="ded96-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ded96-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ded96-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ MemoryArray" ) </span><span class="sxs-lookup"><span data-stu-id="ded96-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="ded96-117">[**Win32 \_ MemoryArray**](win32-memoryarray.md) ，表示 win32 MemoryDeviceArray 關聯的記憶體陣列部分 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ded96-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="ded96-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ded96-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ded96-119">資料類型： **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="ded96-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ded96-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ded96-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ded96-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ MemoryDevice" ) </span><span class="sxs-lookup"><span data-stu-id="ded96-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="ded96-122">[**Win32 \_ MemoryDevice**](win32-memorydevice.md) ，代表 win32 MemoryDeviceArray 關聯的記憶體裝置部分 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ded96-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ded96-123">備註</span><span class="sxs-lookup"><span data-stu-id="ded96-123">Remarks</span></span>

<span data-ttu-id="ded96-124">**Win32 \_ MemoryDeviceArray** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="ded96-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ded96-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ded96-125">Requirements</span></span>



| <span data-ttu-id="ded96-126">需求</span><span class="sxs-lookup"><span data-stu-id="ded96-126">Requirement</span></span> | <span data-ttu-id="ded96-127">值</span><span class="sxs-lookup"><span data-stu-id="ded96-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ded96-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ded96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ded96-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ded96-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ded96-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ded96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ded96-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ded96-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ded96-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ded96-132">Namespace</span></span><br/>                | <span data-ttu-id="ded96-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ded96-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ded96-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ded96-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ded96-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ded96-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ded96-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ded96-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ded96-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ded96-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded96-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ded96-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded96-139">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="ded96-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="ded96-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="ded96-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

