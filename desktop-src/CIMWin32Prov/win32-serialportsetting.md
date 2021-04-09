---
description: Win32 \_ SerialPortSetting 關聯 WMI 類別會建立序列埠及其設定的關聯。
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936107"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="a8b6b-103">Win32 \_ SerialPortSetting 類別</span><span class="sxs-lookup"><span data-stu-id="a8b6b-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="a8b6b-104">**Win32 \_ SerialPortSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立序列埠及其設定的關聯。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="a8b6b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a8b6b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b6b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a8b6b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="a8b6b-108">成員</span><span class="sxs-lookup"><span data-stu-id="a8b6b-108">Members</span></span>

<span data-ttu-id="a8b6b-109">**Win32 \_ SerialPortSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8b6b-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="a8b6b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a8b6b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8b6b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a8b6b-111">Properties</span></span>

<span data-ttu-id="a8b6b-112">**Win32 \_ SerialPortSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8b6b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b6b-114">資料類型： **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="a8b6b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8b6b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b6b-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ SerialPort" ) </span><span class="sxs-lookup"><span data-stu-id="a8b6b-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="a8b6b-117">[**Win32 \_ SerialPort**](win32-serialport.md) ，包含電腦系統上序列埠的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a8b6b-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b6b-119">資料類型： **Win32 \_ SerialPortConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="a8b6b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8b6b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b6b-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ SerialPortConfiguration" ) </span><span class="sxs-lookup"><span data-stu-id="a8b6b-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="a8b6b-122">包含序列埠設定的 [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8b6b-123">備註</span><span class="sxs-lookup"><span data-stu-id="a8b6b-123">Remarks</span></span>

<span data-ttu-id="a8b6b-124">**Win32 \_ SerialPortSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。</span><span class="sxs-lookup"><span data-stu-id="a8b6b-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b6b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8b6b-125">Requirements</span></span>



| <span data-ttu-id="a8b6b-126">需求</span><span class="sxs-lookup"><span data-stu-id="a8b6b-126">Requirement</span></span> | <span data-ttu-id="a8b6b-127">值</span><span class="sxs-lookup"><span data-stu-id="a8b6b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b6b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8b6b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b6b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b6b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8b6b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8b6b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b6b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b6b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8b6b-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8b6b-132">Namespace</span></span><br/>                | <span data-ttu-id="a8b6b-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8b6b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8b6b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a8b6b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8b6b-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8b6b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8b6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b6b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b6b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b6b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8b6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b6b-139">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="a8b6b-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="a8b6b-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
