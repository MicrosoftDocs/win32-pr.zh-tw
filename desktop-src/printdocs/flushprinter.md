---
description: FlushPrinter 函式會將緩衝區傳送至印表機，以便從暫時性狀態中清除。
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: 'FlushPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949298"
---
# <a name="flushprinter-function"></a>FlushPrinter 函式

**FlushPrinter** 函式會將緩衝區傳送至印表機，以便從暫時性狀態中清除。

## <a name="syntax"></a>語法


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機物件的控制碼。 這應該是印表機驅動程式在先前的 [**WritePrinter**](writeprinter.md) 呼叫中所使用的相同控制碼。

</dd> <dt>

*pBuf* \[在\]
</dt> <dd>

位元組陣列的指標，其中包含要寫入至印表機的資料。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PBuf* 所指向的陣列大小（以位元組為單位）。

</dd> <dt>

*pcWritten* \[擴展\]
</dt> <dd>

值的指標，此值會接收寫入至印表機的資料位元組數目。

</dd> <dt>

*cSleep* \[在\]
</dt> <dd>

印表機埠的 i/o 線路應維持閒置的時間（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

只有在 [**WritePrinter**](writeprinter.md)失敗時才應該呼叫 **FlushPrinter** ，讓印表機處於暫時性狀態。 例如，當工作中止，且印表機驅動程式已部分傳送某些原始資料至印表機時，印表機可能會進入暫時性狀態。

**FlushPrinter** 也可以指定列印多工緩衝處理器不會將任何工作排程到對應印表機埠的閒置期間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




