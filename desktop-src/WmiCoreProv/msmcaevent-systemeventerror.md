---
description: 指出已發生 (IPMI) 系統事件的智慧型平臺管理介面。 此錯誤會寫入 SMBIOS 系統事件記錄檔中， (SEL) 。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978312"
---
# <a name="msmcaevent_systemeventerror-class"></a>MSMCAEvent \_ SystemEventError 類別

**MSMCAEvent \_ SystemEventError** 類別指出已發生智慧型平臺管理介面 (IPMI) 系統事件。 此錯誤會寫入 SMBIOS 系統事件記錄檔中， (SEL) 。 此類別僅適用于64位的 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ SystemEventError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ SystemEventError** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

記錄中的其他錯誤數目。

</dd> <dt>

**Cpu**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

回報錯誤的 CPU。 這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

回報之錯誤的嚴重性層級。



| 值                                                                                                | 意義                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 可復原<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 嚴重<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 時發生<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

此類別實例的唯一識別碼。

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含原始錯誤記錄的位元組陣列。 陣列中 **Size** 屬性指定的元素數目。

</dd> <dt>

**記錄識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此錯誤之錯誤記錄的記錄識別碼。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**SEL \_ DATA1**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件資料欄位1。

</dd> <dt>

**SEL \_ DATA2**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件資料欄位2。

</dd> <dt>

**SEL \_ DATA3**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件資料欄位3。

</dd> <dt>

**SEL \_ 事件 \_ DIR \_ 類型**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件目錄類型。

</dd> <dt>

**SEL \_ EVM \_ REV**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤訊息的格式版本。

</dd> <dt>

**SEL 產生器 \_ \_ 識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

軟體識別碼（如果事件是軟體產生的話）。

</dd> <dt>

**選取 \_ 記錄 \_ 識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用於 SMBIOS 系統事件記錄檔的記錄識別碼， (SEL) 存取權。

</dd> <dt>

**選取 \_ 記錄 \_ 類型**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

記錄類型。

</dd> <dt>

**SEL \_ 感應器 \_ NUM**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

產生事件的感應器編號。

</dd> <dt>

**SEL \_ 感應器 \_ 類型**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

產生事件之感應器的感應器類型代碼。

</dd> <dt>

**選取 \_ 時間 \_ 戳**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件記錄檔的時間戳記。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**大小**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

原始錯誤記錄的大小。

</dd> <dt>

**型別**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件記錄檔訊息的類型。 這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。

</dd> <dt>

**驗證 \_ 位**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來指出後續欄位有效性的驗證位。



| 值                                                                                                                                            | 意義                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>             | **SEL \_記錄 \_ 識別碼** 有效。<br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0x2**</dt> </dl>             | **SEL \_記錄 \_ 類型** 有效。<br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>             | **SEL \_產生器 \_ 識別碼** 有效。<br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>             | **SEL \_EVM \_ REV** 有效。<br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>       | **SEL \_感應器 \_ 類型** 有效。<br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>       | **SEL \_感應器 \_ NUM** 是有效的。<br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>       | **SEL \_事件 \_ 目錄** 是有效的。<br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl>    | **SEL \_事件 \_ DATA1** 有效。<br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <dt>**256 0x100**</dt> </dl> | **SEL \_事件 \_ DATA2** 有效。<br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <dt>**512 0x200**</dt> </dl> | **SEL \_事件 \_ DATA3** 有效。<br/>  |



 

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ SystemEventError** 類別衍生自 [**>register-wmievent**](wmievent.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSMCA 類別](msmca-classes.md)
</dt> <dt>

[**>register-wmievent**](wmievent.md)
</dt> </dl>

 

