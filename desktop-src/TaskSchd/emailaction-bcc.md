---
title: EmailAction 密件副本屬性
description: 針對腳本，取得或設定要在電子郵件訊息中密件副本的電子郵件地址。
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- 密件副本屬性工作排程器
- 密件副本屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器、密件副本屬性
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268aece8d6433d07b06d856c266d1e26c096104f0456856ac383253faaf4e976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100388"
---
# <a name="emailactionbcc-property"></a>EmailAction 密件副本屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定要在電子郵件訊息中密件副本的電子郵件地址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a>屬性值

您要在電子郵件訊息中密件副本的電子郵件地址。

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

 

