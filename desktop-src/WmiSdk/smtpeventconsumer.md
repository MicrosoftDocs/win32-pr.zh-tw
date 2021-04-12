---
description: SMTPEventConsumer 類別會在每次傳遞事件給它時，使用 Simple Mail Transfer Protocol (SMTP) 傳送電子郵件訊息。
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: SMTPEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195050"
---
# <a name="smtpeventconsumer-class"></a>SMTPEventConsumer 類別

**SMTPEventConsumer** 類別會在每次傳遞事件給它時，使用 Simple Mail Transfer PROTOCOL (SMTP) 傳送電子郵件訊息。 SMTP 伺服器必須存在於網路上。 SMTPEventConsumer 類別不支援附件。 電子郵件訊息的編碼必須是美國-ASCII。

此類別是 WMI 提供的其中一個標準事件取用者。 如需使用 **SMTPEventConsumer** 來建立取用者的範例，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>成員

**SMTPEventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SMTPEventConsumer** 類別具有這些屬性。

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

地址清單（以逗號或分號分隔），格式為要將訊息當作密件副本傳送的標準字串範本格式。 如需詳細資訊，請參閱本主題的「備註」一節。

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

地址清單（以逗號或分號分隔），採用標準字串範本的格式，訊息會以副本的形式傳送。 如需詳細資訊，請參閱本主題的「備註」一節。

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

**FromLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從電子郵件訊息的行，以標準字串範本的格式。 如果是 **Null**，就會以 "WinMgmt@*MachineName*" 的形式來構成 From 行。

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

插入電子郵件訊息的標頭欄位陣列，不含解讀。

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

**訊息**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含電子郵件訊息主體的標準字串範本。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](key-qualifier.md)
</dt> </dl>

事件取用者的唯一識別碼。

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電子郵件訊息的回復行，格式為標準字串範本。 如果是 **Null**，則不會使用回復行。

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳送電子郵件的 SMTP 伺服器名稱。 允許的名稱為 IP 位址或 DNS 或 NetBIOS 名稱。 這個屬性不能是 **Null**。

</dd> <dt>

**主旨**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

標準字串範本，包含電子郵件訊息的主旨。

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

地址清單（以逗號或分號分隔），格式為識別要傳送訊息之位置的標準字串範本格式。 如需詳細資訊，請參閱本主題的「備註」一節。

</dd> </dl>

## <a name="remarks"></a>備註

SMTPEventConsumer 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。

某些 **ToLine**、 **CcLine** 或 **BccLine** 屬性可以是 **Null**，但不能全部為 **null**。

從 SMTP 服務收到錯誤傳回碼會視為失敗。

## <a name="examples"></a>範例

如需使用 **SMTPEventConsumer** 來建立取用者的範例，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ 訂用帳戶<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> </dl>

 

 




