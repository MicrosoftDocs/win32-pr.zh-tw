---
title: EmailAction 附件屬性
description: 針對腳本，取得或設定與電子郵件訊息一起傳送的附件陣列。
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- 附件屬性工作排程器
- 附件屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，附件屬性
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686008"
---
# <a name="emailactionattachments-property"></a>EmailAction 附件屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定與電子郵件訊息一起傳送的附件陣列。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>屬性值

與電子郵件訊息一起傳送的附件陣列。

## <a name="remarks"></a>備註

附件陣列中最多可以有八個附件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                    |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                       |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

