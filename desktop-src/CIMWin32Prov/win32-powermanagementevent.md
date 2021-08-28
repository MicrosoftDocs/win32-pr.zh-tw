---
description: Win32 \_ PowerManagementEvent &\# 32;WMI 類別代表電源管理事件，由電源狀態變更所造成。
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 536963be51d665b03af77bb81c7592b44d2a6eb5ddc449bfa82896dd7f7da9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064418"
---
# <a name="win32_powermanagementevent-class"></a>Win32 \_ PowerManagementEvent 類別

**Win32 \_ PowerManagementEvent** [WMI 類別](../wmisdk/retrieving-a-class.md)代表電源管理事件，由電源狀態變更所造成。 這些狀態變更與 Advanced 電源管理 (APM) 或進階組態與電源介面 (ACPI) 系統管理通訊協定相關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a>成員

**Win32 \_ PowerManagementEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PowerManagementEvent** 類別具有這些屬性。

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 電源管理事件" ) 
</dt> </dl>

系統電源狀態的變更類型。

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**進入暫** 止 (4) 


</dt> <dd>

暫止時，電腦會顯示為關閉;不過，它可以「喚醒」以回應各種事件，包括使用者輸入 (例如移動滑鼠或按鍵盤上的按鍵) 。 當電腦暫停時，會根據系統的使用方式，將耗電量縮減為數個層級的其中一個。 功率耗用量越低，系統就會花更多時間回到工作狀態。 當電腦進入暫停狀態時，會鎖定桌面，您必須按 CTRL + ALT + DELETE，並提供有效的使用者名稱和密碼，才能繼續作業

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**從暫** 止 (7) 繼續


</dt> <dd>

表示已傳送暫停訊息的 Resume，讓電腦恢復正常的電源狀態。

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**電源狀態變更** (10) 


</dt> <dd>

指出電腦電源狀態的變更，例如從電池電力切換至 AC，或從 AC 切換至不斷電供應系統。 當剩餘電池的電力下滑至使用者所指定的臨界值之下，或是如果電池的電力由指定百分比來變更時，系統也會廣播這個事件。

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM 事件** (11) 


</dt> <dd>

指出 Advanced 電源管理 (APM) BIOS 已傳送 OEM 事件。 事件的值將會在 **OEMEventCode** 屬性中捕捉。 因為某些 APM BIOS 的執行不會提供 OEM 事件通知，所以在某些電腦上可能永遠不會廣播此事件。 APM 是舊版的電源管理配置。 雖然仍然受支援，但 (進階組態與電源介面) 中，大部分的 APM 都已由 ACPI 取代。

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**繼續** (18) 


</dt> <dd>

指出電腦已喚醒以回應事件。 如果系統偵測到使用者活動 (例如滑鼠按一下) ，ResumeSuspend 訊息將會廣播，讓應用程式知道他們可以繼續與使用者進行完全互動。

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 電源管理事件" ) 
</dt> </dl>

由原始設備製造商所定義的系統電源狀態 (OEM) 當此類別的 [ **事件** 類型] 屬性設為 [oem] (OEM 事件) ;否則，此屬性會設定為 **Null**。 當 APM BIOS 發出 APM OEM 事件的信號時，會產生 OEM 事件。 OEM 事件碼位於 0x0200h-0x02FFh 的範圍內。

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

**Win32 \_ PowerManagementEvent** 類別衍生自 [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)。

電源狀態的變更通常表示電腦或其他受管理裝置發生問題。 如果伺服器突然從 AC 電源切換至不斷電供應系統，這項變更可能表示發生某種情況的電子問題，可能是電腦本身或電腦保留的房間內的電力系統所發生。

系統管理員需要監視這些變更的電源狀態，並立即收到這類變更的通知。 這可讓他們在裝置完全斷電之前採取動作。 例如， (的不斷電供應系統供應系統可能只會在15分鐘內執行，然後才關閉。 ) 

**Win32 \_ PowerManagementEvent** 類別可以用來監視電腦電源狀態的變更。 這些變更可能包括從某個電源來源切換到另一個電源，以及電腦電源狀態的變更 (例如，進入或離開暫停模式) 。

**Win32 \_ PowerManagementEvent** 類別只有兩個屬性： [事件種類]，用來表示發生的電源變更事件種類，以及 OEMEventType，供某些原始設備製造商用來定義其他的電源變更事件。

如需有關回應 Windows 電源事件的詳細資訊，請參閱「嘿！」的[監視器和使用 PowerShell 來回應 Windows 電源事件](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx)一文 編寫專家的腳本！ 部落格。

## <a name="examples"></a>範例

下列 VBScript 會監視電腦電源狀態的變更。


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



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

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[監視電腦電源狀態的變更](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
