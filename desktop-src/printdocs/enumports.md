---
description: EnumPorts 函式會列舉可在指定的伺服器上列印的埠。
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: 'EnumPorts 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985244"
---
# <a name="enumports-function"></a>EnumPorts 函式

**EnumPorts** 函式會列舉可在指定的伺服器上列印的埠。

## <a name="syntax"></a>語法


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定您想要列舉其印表機埠的伺服器名稱。

如果 *pName* 為 **Null**，此函式會列舉本機電腦的印表機埠。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PPorts* 緩衝區中傳回的資訊類型。 如果 *層級* 為1， *PPorts* 會接收 [**埠 \_ 資訊 \_ 1**](port-info-1.md) 結構的陣列。 如果 *層級* 為2， *PPorts* 會接收 [**埠 \_ 資訊 \_ 2**](port-info-2.md) 結構的陣列。

</dd> <dt>

*pPorts* \[擴展\]
</dt> <dd>

接收 [**埠 \_ 資訊 \_ 1**](port-info-1.md) 或 [**埠 \_ 資訊 \_ 2**](port-info-2.md) 結構之陣列的緩衝區指標。 每個結構都包含描述可用印表機埠的資料。 緩衝區必須夠大，才能儲存結構成員所指向的字串。

若要判斷所需的緩衝區大小，請呼叫 **EnumPorts** ，並將 *cbBuf* 設定為零。 **EnumPorts** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PPorts* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收復制到 *pPorts* 緩衝區的位元組數目。 如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pPorts* 緩衝區中傳回的 [**埠 \_ 資訊 \_ 1**](port-info-1.md)或 [**埠 \_ 資訊 \_ 2**](port-info-2.md)結構的數目。 這是指定的伺服器上可用的印表機埠數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

即使 *pName* 指定的伺服器未定義印表機， **EnumPorts** 函式仍會成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPortsW** (Unicode) 和 **EnumPortsA** (ANSI) <br/>                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**埠 \_ 資訊 \_ 1**](port-info-1.md)
</dt> <dt>

[**埠 \_ 資訊 \_ 2**](port-info-2.md)
</dt> </dl>

 

