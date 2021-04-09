---
description: Win32 \_ PnPAllocatedResource 關聯 WMI 類別代表邏輯裝置與系統資源之間的關聯。
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847587"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="4af90-103">Win32 \_ PnPAllocatedResource 類別</span><span class="sxs-lookup"><span data-stu-id="4af90-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="4af90-104">**Win32 \_ PnPAllocatedResource** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)代表邏輯裝置與系統資源之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4af90-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="4af90-105">此類別是用來探索特定裝置使用中的資源，例如插斷要求 (IRQ) 或直接記憶體存取 (DMA) 通道。</span><span class="sxs-lookup"><span data-stu-id="4af90-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="4af90-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4af90-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4af90-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4af90-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af90-108">語法</span><span class="sxs-lookup"><span data-stu-id="4af90-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4af90-109">成員</span><span class="sxs-lookup"><span data-stu-id="4af90-109">Members</span></span>

<span data-ttu-id="4af90-110">**Win32 \_ PnPAllocatedResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4af90-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="4af90-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4af90-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4af90-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4af90-112">Properties</span></span>

<span data-ttu-id="4af90-113">**Win32 \_ PnPAllocatedResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4af90-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4af90-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="4af90-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4af90-115">資料類型： **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="4af90-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="4af90-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4af90-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4af90-117">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ SystemResource" ) </span><span class="sxs-lookup"><span data-stu-id="4af90-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="4af90-118">[**CIM \_ SystemResource**](cim-systemresource.md)實例的參考，代表可供邏輯裝置使用之系統資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="4af90-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="4af90-119">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="4af90-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="4af90-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4af90-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4af90-121">資料類型： **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="4af90-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="4af90-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4af90-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4af90-123">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="4af90-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4af90-124">[**Win32 \_ PnPEntity**](win32-pnpentity.md)實例的參考，該實例會使用指派給它的系統資源來表示邏輯裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="4af90-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="4af90-125">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="4af90-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4af90-126">備註</span><span class="sxs-lookup"><span data-stu-id="4af90-126">Remarks</span></span>

<span data-ttu-id="4af90-127">**Win32 \_ PnPAllocatedResource** 類別衍生自 [**CIM \_ AllocatedResource**](cim-allocatedresource.md)。</span><span class="sxs-lookup"><span data-stu-id="4af90-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4af90-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4af90-128">Requirements</span></span>



| <span data-ttu-id="4af90-129">需求</span><span class="sxs-lookup"><span data-stu-id="4af90-129">Requirement</span></span> | <span data-ttu-id="4af90-130">值</span><span class="sxs-lookup"><span data-stu-id="4af90-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4af90-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4af90-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4af90-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4af90-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4af90-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4af90-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4af90-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4af90-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4af90-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="4af90-135">Namespace</span></span><br/>                | <span data-ttu-id="4af90-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4af90-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4af90-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4af90-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4af90-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4af90-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4af90-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4af90-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4af90-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4af90-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4af90-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4af90-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af90-142">**CIM \_ AllocatedResource**</span><span class="sxs-lookup"><span data-stu-id="4af90-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="4af90-143">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4af90-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
