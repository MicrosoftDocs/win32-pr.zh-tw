---
description: Win32 \_ NetworkAdapterSetting 關聯 WMI 類別會建立網路介面卡及其設定的關聯。
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972147"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="35a7d-103">Win32 \_ NetworkAdapterSetting 類別</span><span class="sxs-lookup"><span data-stu-id="35a7d-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="35a7d-104">**Win32 \_ NetworkAdapterSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立網路介面卡及其設定的關聯。</span><span class="sxs-lookup"><span data-stu-id="35a7d-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="35a7d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35a7d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="35a7d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="35a7d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="35a7d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="35a7d-108">成員</span><span class="sxs-lookup"><span data-stu-id="35a7d-108">Members</span></span>

<span data-ttu-id="35a7d-109">**Win32 \_ NetworkAdapterSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35a7d-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="35a7d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="35a7d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35a7d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35a7d-111">Properties</span></span>

<span data-ttu-id="35a7d-112">**Win32 \_ NetworkAdapterSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35a7d-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35a7d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="35a7d-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a7d-114">資料類型： **Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="35a7d-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="35a7d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a7d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a7d-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkAdapter" ) </span><span class="sxs-lookup"><span data-stu-id="35a7d-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="35a7d-117">[**Win32 \_ NetworkAdapter**](win32-networkadapter.md) ，描述使用特定網路介面卡設定的網路介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="35a7d-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="35a7d-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="35a7d-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a7d-119">資料類型： **Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="35a7d-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="35a7d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a7d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a7d-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >networkadapterconfiguration" ) </span><span class="sxs-lookup"><span data-stu-id="35a7d-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="35a7d-122">[**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md) ，描述網路介面卡上使用的設定。</span><span class="sxs-lookup"><span data-stu-id="35a7d-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35a7d-123">備註</span><span class="sxs-lookup"><span data-stu-id="35a7d-123">Remarks</span></span>

<span data-ttu-id="35a7d-124">**Win32 \_ NetworkAdapterSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。</span><span class="sxs-lookup"><span data-stu-id="35a7d-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="35a7d-125">如需如何使用關聯類別的詳細資訊，請參閱 [語句 associators of](../wmisdk/associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a7d-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35a7d-126">範例</span><span class="sxs-lookup"><span data-stu-id="35a7d-126">Examples</span></span>

<span data-ttu-id="35a7d-127">下列 VBScript 範例會使用 **Win32 \_ NetworkAdapterSetting** 來識別區域連接上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="35a7d-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="35a7d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="35a7d-128">Requirements</span></span>



| <span data-ttu-id="35a7d-129">需求</span><span class="sxs-lookup"><span data-stu-id="35a7d-129">Requirement</span></span> | <span data-ttu-id="35a7d-130">值</span><span class="sxs-lookup"><span data-stu-id="35a7d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a7d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35a7d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35a7d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35a7d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35a7d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35a7d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35a7d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a7d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35a7d-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="35a7d-135">Namespace</span></span><br/>                | <span data-ttu-id="35a7d-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="35a7d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35a7d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="35a7d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a7d-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a7d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35a7d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35a7d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a7d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a7d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a7d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35a7d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a7d-142">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="35a7d-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="35a7d-143">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="35a7d-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="35a7d-144">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="35a7d-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
