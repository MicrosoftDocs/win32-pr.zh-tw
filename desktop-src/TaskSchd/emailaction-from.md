---
title: EmailAction 屬性
description: 針對腳本，取得或設定要傳送電子郵件的電子郵件地址。
ms.assetid: befe6900-6fbe-4ba2-aeda-271b770e971a
keywords:
- 從屬性工作排程器
- From 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，從屬性
topic_type:
- apiref
api_name:
- EmailAction.From
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3331b658f21907467ed32f3369357530f30df3facbe630238a704674f23909c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100308"
---
# <a name="emailactionfrom-property"></a>EmailAction 屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定要傳送電子郵件的電子郵件地址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.From As String
```



## <a name="property-value"></a>屬性值

您要傳送電子郵件的電子郵件地址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
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

 

