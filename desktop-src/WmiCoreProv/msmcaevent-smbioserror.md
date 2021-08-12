---
description: 指出電腦檢查架構 (MCA) 系統 BIOS 錯誤。 此類別僅適用于64位 Windows 系統。
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: fccb38a73585db71c6418929a35458f26b9749159e537de47a298d920b318e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558393"
---
# <a name="msmcaevent_smbioserror-class"></a>MSMCAEvent \_ SMBIOSError 類別

**MSMCAEvent \_ SMBIOSError** 類別指出電腦檢查架構 (MCA) 系統 BIOS 錯誤。 此類別僅適用于64位 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ SMBIOSError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ SMBIOSError** 類別具有這些屬性。

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

**SMBIOS \_ 事件 \_ 類型**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件類型。



| 值                                                                                                  | 意義                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | 保留的。<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | 單一位 ECC 記憶體錯誤。<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | 多個位 ECC 記憶體錯誤。<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | 同位記憶體錯誤。<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | 匯流排超時時間。<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | I/o 通道檢查。<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | 軟體 NMI。<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | 張貼記憶體調整大小。<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | POST 錯誤。<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | PCI 同位錯誤。<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | PCI 系統錯誤。<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**rj-11**</dt> </dl> | CPU 失敗。<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**全年**</dt> </dl> | EISA 安全計時器超時時間。<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**.13**</dt> </dl> | 已停用可更正的記憶體記錄檔。<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**日**</dt> </dl> | 已停用特定事件種類的記錄。 在短時間內收到太多相同型別的錯誤。<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | 保留的。<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | 超過系統限制 (例如，超過電壓或溫度閾值) 。<br/>                                  |
| <span id="17"></span><dl> <dt>**至**</dt> </dl> | 非同步硬體計時器已過期，並已發出系統重設。<br/>                                                   |
| <span id="18"></span><dl> <dt>**達**</dt> </dl> | 系統組態資訊。<br/>                                                                                |
| <span id="19"></span><dl> <dt>**診斷**</dt> </dl> | 硬碟資訊。<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**名**</dt> </dl> | 系統重新設定。<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | 無法修復的 CPU-複雜錯誤。<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**日**</dt> </dl> | 記錄區域重設或已清除。<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**上午**</dt> </dl> | 系統開機。 如果已執行，則會保證此記錄專案是在任何系統開機時所寫入的第一個專案。<br/>        |



 

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件記錄檔訊息的類型。 這些訊息會對應到事件記錄檔訊息程式碼，而這些訊息是用來在接收到其中一個事件時，由 Windows 事件記錄取用者提供者插入事件記錄檔訊息。

</dd> <dt>

**驗證 \_ 位**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來指出後續欄位有效性的驗證位。 1 (0x1) 值表示 **SMBIOS \_ 事件** 有效。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ SMBIOSError** 類別衍生自 [**>register-wmievent**](wmievent.md)。

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

 

