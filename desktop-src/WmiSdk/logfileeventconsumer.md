---
description: 當事件傳遞至文字記錄檔時，LogFileEventConsumer 類別會將自訂字串寫入至文字記錄檔。
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: LogFileEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dbcf0f90a8bca0cf1f648f74d1b58d7037b79fa8bc9d2d13c4fe2c6dc8306eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996518"
---
# <a name="logfileeventconsumer-class"></a>LogFileEventConsumer 類別

當事件傳遞至文字記錄檔時， **LogFileEventConsumer** 類別會將自訂字串寫入至文字記錄檔。 這些字串會以行尾序列分隔。 此類別是 WMI 提供的其中一個標準事件取用者。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>成員

**LogFileEventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**LogFileEventConsumer** 類別具有這些屬性。

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立篩選的使用者。 根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**檔案名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

檔案的名稱，其中包含附加記錄專案的路徑。 如果檔案不存在， **LogFileEventConsumer** 會嘗試建立它。 當路徑不存在，或建立取用者的使用者沒有檔案或路徑的寫入權限時，取用者會失敗。

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示記錄檔是 Unicode 文字檔。 如果 **為 FALSE**，則表示記錄檔是多位元組程式碼文字檔。 如果檔案存在，則會忽略此屬性，並使用目前的檔案設定。 例如，如果 **IsUnicode** 為 **FALSE**，但現有的檔案是 unicode 檔案，則會使用 unicode。 如果 **IsUnicode** 為 **TRUE**，但檔案是多位元組程式碼，則會使用多位元組程式碼。

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

**MaximumFileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

記錄檔的大小上限（以位元組為單位）。 如果主要檔案超過其大小上限，則會將內容移至不同的檔案，並清空主要檔案。 值為 0 (零) 表示沒有大小限制。 預設值為65535個位元組。 在寫入作業之前，會檢查檔案的大小。 因此，您可以有稍微大於指定大小限制的檔案。 下一次寫入作業會攔截它，並啟動新的檔案。

下列清單會識別備份檔案的命名結構：

-   如果原始檔案名為8.3，則會使用 "001"、"002" 格式的字串來取代此延伸模組，依此類推，其最小數位會大於所有先前使用和選擇的數位。 如果使用 "999"，則選擇的數位是最小未使用的數位。
-   如果原始檔案名不是8.3，則會在檔案名後面附加 "001"、"002" 等格式的字串。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

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

此取用者的唯一名稱。

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

記錄專案文字的標準字串 [範本](using-standard-string-templates.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> **LogFileEventConsumer** 不會保護記錄檔。 因此，當您設定 **LogFileEventConsumer** 時，請務必指定受限於所需層級的目錄。

 

**LogFileEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。

## <a name="examples"></a>範例

如需使用 **LogFileEventConsumer** 來建立取用者的範例，請參閱 [根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔。

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

[根據事件寫入記錄檔](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

