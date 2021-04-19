---
description: 指出機器檢查架構 (MCA) PCI 元件錯誤。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: MSMCAEvent_PCIComponentError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996906"
---
# <a name="msmcaevent_pcicomponenterror-class"></a>MSMCAEvent \_ PCIComponentError 類別

**MSMCAEvent \_ PCIComponentError** 類別指出電腦檢查架構 (MCA) PCI 元件錯誤。 此類別僅適用于64位的 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ PCIComponentError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ PCIComponentError** 類別具有這些屬性。

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

**PCI \_ 複合 \_ 錯誤 \_ 狀態**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

內部錯誤碼。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ BusNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的匯流排編號。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ ClassCodeBaseClass**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件之基類的類別代碼。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ ClassCodeInterface**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的類別程式碼介面。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ ClassCodeSubClass**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的類別程式碼子類別。

</dd> <dt>

**PCI \_ 複合 \_ 資訊 \_ DeviceId**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的裝置識別碼。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ DeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的裝置編號。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ FunctionNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的功能編號。

</dd> <dt>

**PCI \_ COMP \_ 資訊 \_ SegmentNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的區段編號。

</dd> <dt>

**PCI \_ COMP \_ INFO \_ VendorId**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PCI 元件的廠商識別碼。

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



| 值                                                                               | 意義                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1) </dt> </dl>   | PCI \_ 複合 \_ 錯誤 \_ 狀態為有效。<br/>    |
| <dl> <dt>2 (0x2) </dt> </dl>   | PCI \_ COMP \_ 資訊是有效的。<br/>             |
| <dl> <dt>4 (0x4) </dt> </dl>   | PCI \_ COMP \_ MEM \_ NUM 是有效的。<br/>         |
| <dl> <dt>8 (0x8) </dt> </dl>   | PCI \_ 複合 \_ IO \_ NUM 是有效的。<br/>          |
| <dl> <dt>16 (0x10) </dt> </dl> | PCI \_ COMP \_ REGS \_ 資料 \_ 配對有效。<br/> |



 

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ PCIComponentError** 類別衍生自 [**>register-wmievent**](wmievent.md)。

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

 

