---
description: Win32 \_ SystemConfigurationChangeEvent&\# 8194;WMI 類別指出系統上的裝置清單已重新整理， (已新增或移除裝置，或設定) 變更。
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751298"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Win32 \_ SystemConfigurationChangeEvent 類別

**Win32 \_ SystemConfigurationChangeEvent** [WMI 類別](../wmisdk/retrieving-a-class.md)指出系統上的裝置清單已重新整理， (已新增或移除裝置，或設定) 變更。 當傳送 "DevMgrRefreshOn<*ComputerName*>" 訊息時，就會引發事件，並建立此類別的實例。 裝置清單的確切變更不包含在訊息中，因此需要重新整理裝置才能取得目前的系統設定。 受影響的設定變更範例包括 IRQ 設定、COM 埠和 BIOS 版本。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>成員

**Win32 \_ SystemConfigurationChangeEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemConfigurationChangeEvent** 類別具有這些屬性。

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32APIDevice management messages \| wm \_ DEVICECHANGE \| WParam"，"Win32APIDevice management messages \| wm \_ SETTINGCHANGE" ) 
</dt> </dl>

已發生的事件變更通知類型。

這個屬性繼承自 [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

設定 **已變更** (1) 


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**裝置抵達** (2) 


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**移除裝置** (3) 


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**銜接** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](../wmisdk/wmi-security-constants.md)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。

這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SystemConfigurationChangeEvent** 類別衍生自 [**win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
