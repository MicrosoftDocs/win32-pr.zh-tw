---
description: Win32 \_ PnPDevice 關聯 WMI 類別會將已知的裝置 (設定管理員為 PNPEntity) 以及它所執行的函式。
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970120"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="48527-103">Win32 \_ PnPDevice 類別</span><span class="sxs-lookup"><span data-stu-id="48527-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="48527-104">**Win32 \_ PnPDevice** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將已知的裝置 (設定管理員為 PNPEntity) 以及它所執行的函式。</span><span class="sxs-lookup"><span data-stu-id="48527-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="48527-105">它的函式是以描述其使用方式的邏輯裝置子類別表示。</span><span class="sxs-lookup"><span data-stu-id="48527-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="48527-106">例如， [**win32 \_ 鍵盤**](win32-keyboard.md) 或 [**win32 \_ DiskDrive**](win32-diskdrive.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="48527-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="48527-107">這兩個參考的物件都代表相同的基礎系統裝置;PNPEntity 端資源配置的變更將會影響相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="48527-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="48527-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="48527-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="48527-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="48527-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48527-110">語法</span><span class="sxs-lookup"><span data-stu-id="48527-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="48527-111">成員</span><span class="sxs-lookup"><span data-stu-id="48527-111">Members</span></span>

<span data-ttu-id="48527-112">**Win32 \_ PnPDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="48527-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="48527-113">屬性</span><span class="sxs-lookup"><span data-stu-id="48527-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48527-114">屬性</span><span class="sxs-lookup"><span data-stu-id="48527-114">Properties</span></span>

<span data-ttu-id="48527-115">**Win32 \_ PnPDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="48527-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48527-116">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="48527-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48527-117">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="48527-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="48527-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48527-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48527-119">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ LogicalDevice" ) </span><span class="sxs-lookup"><span data-stu-id="48527-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="48527-120">參考 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例，表示與隨插即用裝置相關聯的邏輯裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="48527-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="48527-121">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="48527-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48527-122">資料類型： **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="48527-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="48527-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48527-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48527-124">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PnPEntity" ) </span><span class="sxs-lookup"><span data-stu-id="48527-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="48527-125">[**Win32 \_ PnPEntity**](win32-pnpentity.md)實例的參考，代表與邏輯裝置相關聯的隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="48527-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48527-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="48527-126">Requirements</span></span>



| <span data-ttu-id="48527-127">需求</span><span class="sxs-lookup"><span data-stu-id="48527-127">Requirement</span></span> | <span data-ttu-id="48527-128">值</span><span class="sxs-lookup"><span data-stu-id="48527-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48527-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48527-129">Minimum supported client</span></span><br/> | <span data-ttu-id="48527-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48527-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48527-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48527-131">Minimum supported server</span></span><br/> | <span data-ttu-id="48527-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48527-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48527-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="48527-133">Namespace</span></span><br/>                | <span data-ttu-id="48527-134">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="48527-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48527-135">MOF</span><span class="sxs-lookup"><span data-stu-id="48527-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48527-136"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="48527-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48527-137">DLL</span><span class="sxs-lookup"><span data-stu-id="48527-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48527-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48527-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48527-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48527-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48527-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="48527-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
