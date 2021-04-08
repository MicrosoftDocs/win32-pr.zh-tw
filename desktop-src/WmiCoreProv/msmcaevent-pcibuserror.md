---
description: 代表 (MCA) PCI 匯流排錯誤的機器檢查架構。 此類別僅適用于在64位 Windows 作業系統上執行的電腦。
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690368"
---
# <a name="msmcaevent_pcibuserror-class"></a>MSMCAEvent \_ PCIBusError 類別

**MSMCAEvent \_ PCIBusError** 類別代表 (MCA) PCI 匯流排錯誤的機器檢查架構。 此類別僅適用于在64位 Windows 作業系統上執行的電腦。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ PCIBusError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ PCIBusError** 類別具有這些屬性。

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

如果 0 (零) ，則此事件不會記錄到系統事件記錄檔中。

</dd> <dt>

**PCI \_ 匯流排 \_ 位址**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在發生事件時 PCI 匯流排上的記憶體或 i/o 位址。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ 匯流排 \_ CMD**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生事件時的匯流排命令或作業。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ 匯流排 \_ 資料**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生事件時 PCI 匯流排上的資料。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ 匯流排 \_ 錯誤 \_ 狀態**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生錯誤時的匯流排狀態。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ 匯流排 \_ 錯誤 \_ 類型**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 匯流排錯誤的類型。



| 值                                                                                                | 意義                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 未知或 OEM 系統的特定錯誤。<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 資料同位錯誤。<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 系統錯誤。<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Master Abort。<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 沒有任何 DEVSEL)  (的匯流排超時或裝置不存在 \# 。<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | 主要資料同位錯誤。<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | 位址同位錯誤。<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | 命令同位錯誤。<br/>                            |



 

</dd> <dt>

**PCI \_ 匯流排 \_ 識別碼 \_ BusNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生錯誤之 PCI 匯流排指定的識別碼。

</dd> <dt>

**PCI \_ 匯流排 \_ 識別碼 \_ SegmentNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生錯誤之 PCI 匯流排的指定區段識別碼。

</dd> <dt>

**PCI \_ 匯流排要求者 \_ \_ 識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件時的 PCI 匯流排要求者識別碼。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ 匯流排 \_ 回應程式 \_ 識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件當時的 PCI 匯流排回應程式識別碼。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

位元組陣列，其中包含系統抽象層 (SAL) 呈現給 Windows 的原始錯誤記錄。 陣列中的元素數目是由 **Size** 屬性指定。

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



| 值                                                                                  | 意義                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1) </dt> </dl>      | PCI \_ 匯流排 \_ 錯誤 \_ 狀態為有效。<br/>     |
| <dl> <dt>2 (0x2) </dt> </dl>      | PCI \_ 匯流排 \_ 錯誤 \_ 類型有效。<br/>       |
| <dl> <dt>4 (0x4) </dt> </dl>      | PCI \_ 匯流排 \_ 識別碼有效。<br/>                |
| <dl> <dt>8 (0x8) </dt> </dl>      | PCI \_ 匯流排 \_ 位址有效。<br/>           |
| <dl> <dt>16 (0x10) </dt> </dl>    | PCI \_ 匯流排 \_ 資料有效。<br/>              |
| <dl> <dt>32 (0x20) </dt> </dl>    | PCI \_ 匯流排 \_ CMD 有效。<br/>               |
| <dl> <dt>64 (0x40) </dt> </dl>    | PCI \_ 匯流排要求者 \_ \_ 識別碼有效。<br/>     |
| <dl> <dt>128 (0x80) </dt> </dl>   | PCI \_ 匯流排 \_ 回應 \_ 程式識別碼有效。<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | PCI \_ 匯流排 \_ 目標 \_ 識別碼有效。<br/>        |
| <dl> <dt>512 (0x200) </dt> </dl>  | PCI \_ 匯流排 \_ OEM \_ 識別碼有效。<br/>           |
| <dl> <dt>1024 (0x400) </dt> </dl> | PCI \_ 匯流排 \_ OEM \_ 資料 \_ 結構有效。<br/> |



 

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ PCIBusError** 類別衍生自 [**>register-wmievent**](wmievent.md)。

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

 

