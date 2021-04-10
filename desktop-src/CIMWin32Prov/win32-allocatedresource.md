---
description: Win32 \_ AllocatedResource 關聯 WMI 類別會將邏輯裝置與系統資源產生關聯。 此類別是用來探索特定裝置正在使用的資源，例如 Irq 或 DMA 通道。
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Win32_AllocatedResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936455"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="4e346-104">Win32 \_ AllocatedResource 類別</span><span class="sxs-lookup"><span data-stu-id="4e346-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="4e346-105">**Win32 \_ AllocatedResource** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將邏輯裝置與系統資源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4e346-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="4e346-106">此類別是用來探索特定裝置正在使用的資源，例如 Irq 或 DMA 通道。</span><span class="sxs-lookup"><span data-stu-id="4e346-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="4e346-107">這個類別已經過時。</span><span class="sxs-lookup"><span data-stu-id="4e346-107">This class is obsolete.</span></span> <span data-ttu-id="4e346-108">若要取代這個類別，您應該使用 [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md) 類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e346-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="4e346-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e346-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4e346-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4e346-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e346-111">語法</span><span class="sxs-lookup"><span data-stu-id="4e346-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4e346-112">成員</span><span class="sxs-lookup"><span data-stu-id="4e346-112">Members</span></span>

<span data-ttu-id="4e346-113">**Win32 \_ AllocatedResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4e346-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="4e346-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4e346-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e346-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4e346-115">Properties</span></span>

<span data-ttu-id="4e346-116">**Win32 \_ AllocatedResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4e346-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e346-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="4e346-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e346-118">資料類型： **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="4e346-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="4e346-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e346-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e346-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \| CIM \_ SystemResource" ) </span><span class="sxs-lookup"><span data-stu-id="4e346-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="4e346-121">[**CIM \_ SystemResource**](cim-systemresource.md) ，描述可供邏輯裝置使用之系統資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e346-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4e346-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4e346-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e346-123">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4e346-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4e346-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e346-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e346-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="4e346-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4e346-126">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，表示使用指派給它的系統資源之邏輯裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e346-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e346-127">備註</span><span class="sxs-lookup"><span data-stu-id="4e346-127">Remarks</span></span>

<span data-ttu-id="4e346-128">**Win32 \_ AllocatedResource** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="4e346-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e346-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e346-129">Requirements</span></span>



| <span data-ttu-id="4e346-130">需求</span><span class="sxs-lookup"><span data-stu-id="4e346-130">Requirement</span></span> | <span data-ttu-id="4e346-131">值</span><span class="sxs-lookup"><span data-stu-id="4e346-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e346-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e346-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e346-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e346-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e346-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e346-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e346-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e346-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e346-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e346-136">Namespace</span></span><br/>                | <span data-ttu-id="4e346-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e346-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e346-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4e346-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e346-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e346-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e346-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4e346-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e346-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e346-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e346-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e346-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e346-143">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="4e346-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="4e346-144">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4e346-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

