---
title: SendEmail (actionGroup) 元素
description: 表示傳送電子郵件訊息的動作。
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- SendEmail 元素工作排程器
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934828"
---
# <a name="sendemail-actiongroup-element"></a>SendEmail (actionGroup) 元素

表示傳送電子郵件訊息的動作。

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

**SendEmail** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                         | 衍生自                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**行動**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | 包含工作所執行的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                        | 類型                                                                         | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**附件**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | 指定電子郵件訊息中的附件清單。<br/>                                 |
| [**密件副本**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | 指定電子郵件訊息的 [密件副本] 行上使用的電子郵件地址。<br/>               |
| [**主體**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | 指定電子郵件訊息主體中的文字。<br/>                                  |
| [**Cc**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | 指定電子郵件訊息之 Cc 行上使用的電子郵件地址。<br/>                |
| [**寄件者**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | 指定寄件者的電子郵件地址。<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | 指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | 指定電子郵件訊息中要回復的電子郵件地址。<br/>               |
| [**伺服器**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | 指定用來傳送電子郵件訊息的電子郵件伺服器。 <br/>                           |
| [**主體**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | 指定電子郵件訊息的主旨。<br/>                                           |
| [**自**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | 指定電子郵件將傳送至其中的電子郵件地址。<br/>                        |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) 介面。

如需腳本開發，請參閱 [**EmailAction**](emailaction.md) 物件。

**Windows 8 和 Windows Server 2012：** 已移除這個元素。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。

## <a name="examples"></a>範例

如需指定電子郵件動作之工作的 XML 完整範例，請參閱 [事件觸發程式範例 (xml) ](/previous-versions//aa446889(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows 7<br/>                                 |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                    |



 

