---
title: TranslateDispatch 回呼函式
description: DoReaderMode 函式的用戶端使用它來攔截並明確處理以讀取器強制回應視窗的捲動區域為目標的任何 windows 訊息。 這是應用程式定義的回呼函數。
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch 回呼函式 Windows 控制項
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060528"
---
# <a name="translatedispatch-callback-function"></a>TranslateDispatch 回呼函式

\[*TranslateDispatch* 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

[**DoReaderMode**](doreadermode.md)函式的用戶端使用它來攔截並明確處理以讀取器強制回應視窗的捲動區域為目標的任何 windows 訊息。 這是應用程式定義的回呼函數。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpmsg* \[在\]
</dt> <dd>

Type： **Const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標，其中包含攔截的訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果此函式已處理訊息，則為 **TRUE** ;否則 **為 FALSE**。 如果 **為 FALSE**，則表示訊息是由預設讀取器模式執行所處理。 該執行會處理滑鼠移動和按鈕，以及按鍵。

## <a name="examples"></a>範例

下列範例概述此函式的實作為。


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista，僅 Windows vista \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>          |



 

