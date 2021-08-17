---
description: 代表 CPU 錯誤事件。 此類別僅適用于64位 Windows 系統。
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: MSMCAEvent_CPUError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 42542f9e32bee31e44df65c0d0ade3d337e3fe395315fe28d6fd8b1c66b3b8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926871"
---
# <a name="msmcaevent_cpuerror-class"></a>MSMCAEvent \_ CPUError 類別

**MSMCAEvent \_ CPUError** 類別代表 CPU 錯誤事件。 此類別僅適用于64位 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ CPUError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ CPUError** 類別具有這些屬性。

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

MCA 記錄中的其他錯誤數目。

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

這個類別實例的唯一識別碼。

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiMissingData** (-1) 
</dt> </dl>

發生錯誤之快取、轉譯緩衝區 (TLB) 或微架構結構的層級。 值為 0 (零) 表示第一個層級。

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果為零，則此事件不會記錄到系統事件記錄檔中。

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

原始錯誤記錄的大小（以位元組為單位）。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件記錄檔訊息的類型。 這些訊息會對應到事件記錄檔訊息程式碼，而這些訊息是用來在接收到其中一個事件時，由 Windows 事件記錄取用者提供者插入事件記錄檔訊息。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ CPUError** 類別衍生自 [**>register-wmievent**](wmievent.md)。

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

 

