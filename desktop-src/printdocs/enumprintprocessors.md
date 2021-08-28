---
description: EnumPrintProcessors 函式會列舉安裝在指定伺服器上的列印處理器。
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: 'EnumPrintProcessors 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 800ed5afcf332a0c34dc272158f98fed64e47e86cb3c16cb24d6013951ffd3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846038"
---
# <a name="enumprintprocessors-function"></a>EnumPrintProcessors 函式

**EnumPrintProcessors** 函式會列舉安裝在指定伺服器上的列印處理器。

## <a name="syntax"></a>語法


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定列印處理器所在之伺服器的名稱。 如果此參數為 **Null**，則會列舉本機列印處理器。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定環境 (例如 Windows x86、Windows IA64 或 Windows x64) 。 如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PPrintProcessorInfo* 緩衝區中傳回的資訊類型。 此參數必須是1。

</dd> <dt>

*pPrintProcessorInfo* \[擴展\]
</dt> <dd>

接收 [**PRINTPROCESSOR \_ INFO \_ 1**](printprocessor-info-1.md) 結構陣列的緩衝區指標。 每個結構都描述可用的列印處理器。 緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串。

若要判斷所需的緩衝區大小，請呼叫 **EnumPrintProcessors** ，並將 *cbBuf* 設定為零。 **EnumPrintProcessors** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PPrintProcessorInfo* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收在函式成功時複製到 *pPrintProcessorInfo* 緩衝區的位元組數目。 如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pPrintProcessorInfo* 緩衝區中傳回的結構數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrintProcessorsW** (Unicode) 和 **EnumPrintProcessorsA** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**PRINTPROCESSOR \_ 資訊 \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

