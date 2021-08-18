---
title: ShowMessageAction. MessageBody 屬性
description: 針對腳本，取得或設定顯示在訊息方塊主體中的郵件內文。
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- MessageBody 屬性工作排程器
- MessageBody 屬性工作排程器，ShowMessageAction 物件
- ShowMessageAction 物件工作排程器、MessageBody 屬性
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5b408ad8642cc17b85d783a8f26d7de3322a26309897e4d9b3c128401449d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139341"
---
# <a name="showmessageactionmessagebody-property"></a>ShowMessageAction. MessageBody 屬性

\[不再支援此物件。 您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80))，在使用者會話中顯示訊息。\]

針對腳本，取得或設定顯示在訊息方塊主體中的郵件內文。

## <a name="syntax"></a>Syntax


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>屬性值

顯示在訊息方塊內文中的郵件內文。

## <a name="remarks"></a>備註

參數化字串可以在訊息方塊的郵件內文中使用。 如需詳細資訊，請參閱 [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)中的範例一節。

設定這個屬性值時，值可以是從資源 .dll 檔抓取的文字。 特製化的字串會用來參考資源檔中的文字。 字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ Dll \] 是包含資源的 .dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。 例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。

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

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

