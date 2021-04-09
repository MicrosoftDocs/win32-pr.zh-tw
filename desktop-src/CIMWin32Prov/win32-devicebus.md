---
description: Win32 \_ DeviceBus 關聯 WMI 類別會使用匯流排來建立系統匯流排和邏輯裝置的關聯。 此類別是用來探索哪些裝置在哪個匯流排上。
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Win32_DeviceBus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111605"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="72b36-104">Win32 \_ DeviceBus 類別</span><span class="sxs-lookup"><span data-stu-id="72b36-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="72b36-105">**Win32 \_ DeviceBus** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會使用匯流排來建立系統匯流排和邏輯裝置的關聯。</span><span class="sxs-lookup"><span data-stu-id="72b36-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="72b36-106">此類別是用來探索哪些裝置在哪個匯流排上。</span><span class="sxs-lookup"><span data-stu-id="72b36-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="72b36-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="72b36-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="72b36-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="72b36-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b36-109">語法</span><span class="sxs-lookup"><span data-stu-id="72b36-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="72b36-110">成員</span><span class="sxs-lookup"><span data-stu-id="72b36-110">Members</span></span>

<span data-ttu-id="72b36-111">**Win32 \_ DeviceBus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="72b36-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="72b36-112">屬性</span><span class="sxs-lookup"><span data-stu-id="72b36-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72b36-113">屬性</span><span class="sxs-lookup"><span data-stu-id="72b36-113">Properties</span></span>

<span data-ttu-id="72b36-114">**Win32 \_ DeviceBus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="72b36-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72b36-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="72b36-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b36-116">資料類型： **Win32 \_ 匯流排**</span><span class="sxs-lookup"><span data-stu-id="72b36-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="72b36-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72b36-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b36-118">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ Bus" ) </span><span class="sxs-lookup"><span data-stu-id="72b36-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="72b36-119">[**Win32 \_ 匯流排**](win32-bus.md)，描述邏輯裝置所使用的系統匯流排屬性。</span><span class="sxs-lookup"><span data-stu-id="72b36-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="72b36-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="72b36-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b36-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="72b36-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="72b36-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72b36-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b36-123">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="72b36-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="72b36-124">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述使用系統匯流排的邏輯裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="72b36-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72b36-125">備註</span><span class="sxs-lookup"><span data-stu-id="72b36-125">Remarks</span></span>

<span data-ttu-id="72b36-126">**Win32 \_ DeviceBus** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="72b36-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72b36-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="72b36-127">Requirements</span></span>



| <span data-ttu-id="72b36-128">需求</span><span class="sxs-lookup"><span data-stu-id="72b36-128">Requirement</span></span> | <span data-ttu-id="72b36-129">值</span><span class="sxs-lookup"><span data-stu-id="72b36-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72b36-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72b36-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72b36-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72b36-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72b36-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72b36-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72b36-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72b36-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72b36-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="72b36-134">Namespace</span></span><br/>                | <span data-ttu-id="72b36-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="72b36-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72b36-136">MOF</span><span class="sxs-lookup"><span data-stu-id="72b36-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72b36-137"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="72b36-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72b36-138">DLL</span><span class="sxs-lookup"><span data-stu-id="72b36-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b36-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72b36-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b36-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72b36-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b36-141">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="72b36-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="72b36-142">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="72b36-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

