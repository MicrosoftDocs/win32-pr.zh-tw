---
description: EnumPrintProcessorDatatypes 函式會列舉指定列印處理器支援的資料類型。
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: 'EnumPrintProcessorDatatypes 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513328"
---
# <a name="enumprintprocessordatatypes-function"></a>EnumPrintProcessorDatatypes 函式

**EnumPrintProcessorDatatypes** 函式會列舉指定列印處理器支援的資料類型。

## <a name="syntax"></a>語法


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定列印處理器所在之伺服器的名稱。 如果這個參數為 **Null**，則會列舉本機列印處理器的資料類型。

</dd> <dt>

*pPrintProcessorName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定列舉其資料類型的列印處理器名稱。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PDatatypes* 緩衝區中傳回的資訊類型。 此參數必須是1。

</dd> <dt>

*pDatatypes* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**資料類型 \_ 資訊 \_ 1**](datatypes-info-1.md) 結構的陣列。 每個結構都描述可用的資料類型。 緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。

若要判斷所需的緩衝區大小，請呼叫 **EnumPrintProcessorDatatypes** ，並將 *cbBuf* 設定為零。 **EnumPrintProcessorDatatypes** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PDatatypes* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收在函式成功時複製到 *pDatatypes* 緩衝區的位元組數目。 如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pDatatypes* 緩衝區中傳回的結構數目。 這是支援的資料類型數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

v

從 Windows Vista 開始，來自遠端列印伺服器的資料類型資訊，會從本機快取中取出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrintProcessorDatatypesW** (Unicode) 和 **EnumPrintProcessorDatatypesA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**資料類型 \_ 資訊 \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

