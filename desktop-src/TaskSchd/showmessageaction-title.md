---
title: ShowMessageAction Title 屬性
description: 針對腳本，取得或設定訊息方塊的標題。
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Title 屬性工作排程器
- Title 屬性工作排程器，ShowMessageAction 物件
- ShowMessageAction 物件工作排程器、Title 屬性
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685683"
---
# <a name="showmessageactiontitle-property"></a>ShowMessageAction Title 屬性

\[不再支援此物件。 您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80)) ，在使用者會話中顯示訊息。\]

針對腳本，取得或設定訊息方塊的標題。

## <a name="syntax"></a>Syntax


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a>屬性值

訊息方塊的標題。

## <a name="remarks"></a>備註

參數化字串可以在訊息方塊的標題文字中使用。 如需詳細資訊，請參閱 [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)中的範例一節。

設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。 特製化的字串會用來參考資源檔中的文字。 字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。 例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。

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

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

