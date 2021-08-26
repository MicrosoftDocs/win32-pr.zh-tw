---
description: ConfigurePort 函式會顯示指定伺服器上端口的 [埠-設定] 對話方塊。
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: 'ConfigurePort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dbc31de341c137e8baf729a468e8576684ccef8b0a860be898c9cb5a6af34217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950438"
---
# <a name="configureport-function"></a>ConfigurePort 函式

**ConfigurePort** 函式會顯示指定伺服器上端口的 [埠-設定] 對話方塊。

## <a name="syntax"></a>語法


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

指標，指向以 null 終止的字串，這個字串會指定指定的埠所在之伺服器的名稱。 如果此參數為 **Null**，則埠為本機。

</dd> <dt>

*hWnd* \[在\]
</dt> <dd>

埠設定對話方塊的父視窗的控制碼。

</dd> <dt>

*pPortName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要設定的埠名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

在呼叫 **ConfigurePort** 函式之前，應用程式應該呼叫 [**EnumPorts**](enumports.md) 函數來判斷有效的埠名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **ConfigurePortW** (Unicode) 和 **ConfigurePortA** (ANSI) <br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




