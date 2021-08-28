---
description: EnumMonitors 函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: 'EnumMonitors 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 67a623e98b72ee26e6a9325120d26b26f92d03384318e90f28983a3a1978edf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949628"
---
# <a name="enummonitors-function"></a>EnumMonitors 函式

**EnumMonitors** 函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定監視器所在伺服器的名稱。 如果此參數為 **Null**，則會列舉本機監視器。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PMonitors* 所指向的結構版本。

這個值可以是1或2。

</dd> <dt>

*pMonitors* \[擴展\]
</dt> <dd>

接收結構陣列的緩衝區指標。 緩衝區必須夠大，才能儲存結構成員所參考的字串。

若要判斷所需的緩衝區大小，請呼叫 **EnumMonitors** ，並將 *cbBuf* 設定為零。 **EnumMonitors** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

如果 *層級* 為1，緩衝區會接收 [**監視 \_ 資訊 \_ 1**](monitor-info-1.md)結構的陣列，如果 *層級* 為2，則會接收 [**監視器 \_ 資訊 \_ 2**](monitor-info-2.md)結構。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PMonitors* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收函式成功時所複製的位元組數目，或 *cbBuf* 太小時所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pMonitors* 所指向之緩衝區中傳回的結構數目。

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
| Unicode 與 ANSI 名稱<br/>   | **EnumMonitorsW** (Unicode) 和 **EnumMonitorsA** (ANSI) <br/>                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**監視 \_ 資訊 \_ 1**](monitor-info-1.md)
</dt> <dt>

[**監視 \_ 資訊 \_ 2**](monitor-info-2.md)
</dt> </dl>

 

