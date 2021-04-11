---
description: NTEventLogEventConsumer 類別會在事件傳遞給它時，將特定訊息記錄到作業系統事件記錄檔中。
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848393"
---
# <a name="nteventlogeventconsumer-class"></a>NTEventLogEventConsumer 類別

**NTEventLogEventConsumer** 類別會在事件傳遞給它時，將特定訊息記錄到作業系統事件記錄檔中。 此類別是 WMI 提供的其中一個標準事件取用者。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>成員

**NTEventLogEventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**NTEventLogEventConsumer** 類別具有這些屬性。

<dl> <dt>

**類別**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件類別目錄。 這是來源特定的資訊，而且可以具有任何值。

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立篩選的使用者。 根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

訊息 DLL 中的事件訊息。 這個屬性不能是 **Null**。

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件的類型。 這個參數可以有下列清單中所列的其中一個值，這些值定義于 Winnt 中。

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG \_SUCCESS** (0 (0x0) ) 


</dt> <dd>

成功的事件

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG \_\_TPYE** (1 (0X1) ) 時發生錯誤


</dt> <dd>

錯誤事件

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG \_警告 \_ 類型** (2 (0x2) ) 


</dt> <dd>

警告事件

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG \_資訊 \_ 類型** (4 (0x4) ) 


</dt> <dd>

資訊事件

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG \_AUDIT \_ SUCCESS** (8 (0x8) ) 


</dt> <dd>

成功審核類型

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG \_AUDIT \_ 失敗** (16 (0x10) ) 


</dt> <dd>

失敗審核類型

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

標準字串範本的陣列，用來做為事件記錄檔記錄的插入字串。

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

特定取用者的佇列上限，以位元組為單位。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](key-qualifier.md)
</dt> </dl>

取用者的唯一名稱。

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件屬性的名稱，其中包含要傳遞給 [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) 函數 *lpRawData* 參數的資料。

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件屬性的名稱，其中包含要傳遞至 [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) 函式 *LPUSERSID* 參數 (SID) 的安全識別碼。 屬性必須是位元組陣列 (**uint8**) 或字串。 如果是位元組陣列，則會假設為 SID。 如果是字串，它就是轉換成 SID 的字串 SID。

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**InsertionStringTemplates** 陣列中的元素數目。

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

訊息所在的來源名稱。 假設客戶已使用必要的訊息註冊 DLL。

> [!Note]  
> 此參數的值不能包含冒號 (： ) 字元。

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要記錄事件的電腦名稱稱，如果事件是在本機伺服器上登入，則 **為 Null** 。

依預設，已驗證的使用者不能將事件記錄到遠端電腦上的應用程式記錄檔。 因此，使用此屬性指定遠端電腦將無法運作。 若要瞭解如何變更事件記錄檔安全性，請參閱這 [篇知識庫文章](https://support.microsoft.com/kb/323076)。

</dd> </dl>

## <a name="remarks"></a>備註

**NTEventLogEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。

## <a name="examples"></a>範例

如需使用 **NTEventLogEventConsumer** 來建立取用者的範例，請參閱 [根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ 訂用帳戶<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

