---
description: DeletePrintProcessor 函式會移除 AddPrintProcessor 函數所新增的列印處理器。
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: 'DeletePrintProcessor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: be88839ae51fc52d453e1171a8ed0489df7827dda9476bf5e27d9f3d6a16ee1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949988"
---
# <a name="deleteprintprocessor-function"></a>DeletePrintProcessor 函式

**DeletePrintProcessor** 函式會移除 [**AddPrintProcessor**](addprintprocessor.md)函數所新增的列印處理器。

## <a name="syntax"></a>語法


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要移除處理器的伺服器名稱。 如果此參數為 **Null**，則會在本機移除印表機處理器。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要移除處理器的環境 (例如 Windows NT x86、Windows IA64 或 Windows x64) 。 如果這個參數是 **Null**，就會從目前的呼叫應用程式和用戶端電腦的環境中移除處理器 (不是目的地應用程式和列印伺服器) 。 **Null** 是建議的值，因為它提供最大的可攜性。

</dd> <dt>

*pPrintProcessorName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要移除的處理器名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **DeletePrintProcessorW** (Unicode) 和 **DeletePrintProcessorA** (ANSI) <br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

