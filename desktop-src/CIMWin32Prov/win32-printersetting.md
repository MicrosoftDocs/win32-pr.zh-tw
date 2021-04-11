---
description: Win32 \_ PrinterSetting 關聯 WMI 類別會建立印表機與其設定的關聯性。
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187729"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="bc121-103">Win32 \_ PrinterSetting 類別</span><span class="sxs-lookup"><span data-stu-id="bc121-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="bc121-104">**Win32 \_ PrinterSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立印表機與其設定的關聯性。</span><span class="sxs-lookup"><span data-stu-id="bc121-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="bc121-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc121-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bc121-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bc121-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc121-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc121-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="bc121-108">成員</span><span class="sxs-lookup"><span data-stu-id="bc121-108">Members</span></span>

<span data-ttu-id="bc121-109">**Win32 \_ PrinterSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc121-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bc121-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bc121-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc121-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bc121-111">Properties</span></span>

<span data-ttu-id="bc121-112">**Win32 \_ PrinterSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bc121-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc121-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc121-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc121-114">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="bc121-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bc121-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc121-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc121-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ LogicalDevice" ) </span><span class="sxs-lookup"><span data-stu-id="bc121-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="bc121-117">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，代表可套用設定的邏輯裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="bc121-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="bc121-118">這個屬性繼承自 [**Win32 \_ DeviceSettings**](win32-devicesettings.md)。</span><span class="sxs-lookup"><span data-stu-id="bc121-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc121-119">**設定**</span><span class="sxs-lookup"><span data-stu-id="bc121-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc121-120">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="bc121-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="bc121-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc121-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc121-122">限定詞： [**key**](../wmisdk/key-qualifier.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ 設定" ) </span><span class="sxs-lookup"><span data-stu-id="bc121-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="bc121-123">[**CIM \_ 設定**](cim-setting.md)，代表可以套用至邏輯裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="bc121-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="bc121-124">這個屬性繼承自 [**Win32 \_ DeviceSettings**](win32-devicesettings.md)。</span><span class="sxs-lookup"><span data-stu-id="bc121-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc121-125">備註</span><span class="sxs-lookup"><span data-stu-id="bc121-125">Remarks</span></span>

<span data-ttu-id="bc121-126">**Win32 \_ PrinterSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。</span><span class="sxs-lookup"><span data-stu-id="bc121-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc121-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc121-127">Requirements</span></span>



| <span data-ttu-id="bc121-128">需求</span><span class="sxs-lookup"><span data-stu-id="bc121-128">Requirement</span></span> | <span data-ttu-id="bc121-129">值</span><span class="sxs-lookup"><span data-stu-id="bc121-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc121-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc121-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bc121-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc121-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bc121-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc121-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bc121-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc121-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bc121-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc121-134">Namespace</span></span><br/>                | <span data-ttu-id="bc121-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc121-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="bc121-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bc121-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc121-137"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc121-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc121-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bc121-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc121-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc121-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bc121-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc121-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc121-141">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="bc121-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="bc121-142">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="bc121-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
