---
title: EmailAction. HeaderFields 屬性
description: 針對腳本，取得或設定您想要傳送的電子郵件中的標頭資訊。
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- HeaderFields 屬性工作排程器
- HeaderFields 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器、HeaderFields 屬性
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8131528c3fec93a6df78b58c4eda76f1f78e7b996b74df1068e3be30b468d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100298"
---
# <a name="emailactionheaderfields-property"></a>EmailAction. HeaderFields 屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定您想要傳送的電子郵件中的標頭資訊。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a>屬性值

您要傳送的電子郵件中的標頭資訊。

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

 

