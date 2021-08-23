---
title: EmailAction 物件
description: 代表傳送電子郵件訊息之動作的腳本物件。
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- EmailAction 物件工作排程器
- EmailAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918065515322696a33114d2d9b09b7b72d12eb6b74e120a7963835a23321fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002476"
---
# <a name="emailaction-object"></a>EmailAction 物件

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

代表傳送電子郵件訊息之動作的腳本物件。

## <a name="members"></a>成員

**EmailAction** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**EmailAction** 物件具有這些屬性。



| 屬性                                                    | 存取類型           | 描述                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**附件**](emailaction-attachments.md)<br/>   | 讀取/寫入<br/> | 取得或設定與電子郵件訊息一起傳送的附件陣列。<br/>                      |
| [**密件副本**](emailaction-bcc.md)<br/>                   | 讀取/寫入<br/> | 取得或設定要在電子郵件訊息中密件副本的電子郵件地址。<br/>         |
| [**主體**](emailaction-body.md)<br/>                 | 讀取/寫入<br/> | 取得或設定包含電子郵件訊息的電子郵件內文。<br/>                            |
| [**Cc**](emailaction-cc.md)<br/>                     | 讀取/寫入<br/> | 取得或設定要在電子郵件訊息中抄送的電子郵件地址。<br/>          |
| [**從**](emailaction-from.md)<br/>                 | 讀取/寫入<br/> | 取得或設定要傳送電子郵件的電子郵件地址。<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | 讀取/寫入<br/> | 取得或設定要傳送的電子郵件中的標頭資訊。<br/>                        |
| [**Id**](action-id.md)<br/>                          | 讀取/寫入<br/> | 繼承自 [**動作**](action.md) 物件。 取得或設定動作的識別碼。<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | 讀取/寫入<br/> | 取得或設定要回復的電子郵件地址。<br/>                                      |
| [**伺服器**](emailaction-server.md)<br/>             | 讀取/寫入<br/> | 取得或設定用來傳送電子郵件的伺服器名稱。<br/>                           |
| [**主體**](emailaction-subject.md)<br/>           | 讀取/寫入<br/> | 取得或設定電子郵件訊息的主旨。<br/>                                                 |
| [**自**](emailaction-to.md)<br/>                     | 讀取/寫入<br/> | 取得或設定要傳送電子郵件的電子郵件地址。<br/>                |
| [**類型**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | 唯讀<br/>  | 繼承自 [**動作**](action.md) 物件。 取得動作的類型。<br/>                   |



 

## <a name="remarks"></a>備註

電子郵件動作必須具有 [[**伺服器**](emailaction-server.md)]、[[**寄件者**](emailaction-from.md)]、[收件者] 或 [副本 [**] 屬性的**](emailaction-cc.md)有效值 [**，才能讓**](emailaction-to.md)工作正確註冊並執行。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) 元素來指定電子郵件動作。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [事件觸發程式範例 (腳本) ](/previous-versions//aa446887(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                    |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                       |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

