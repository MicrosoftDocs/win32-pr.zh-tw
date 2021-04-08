---
description: EnumPrinterDrivers 函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: 'EnumPrinterDrivers 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692904"
---
# <a name="enumprinterdrivers-function"></a>EnumPrinterDrivers 函式

**EnumPrinterDrivers** 函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。

## <a name="syntax"></a>語法


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定用來列舉印表機驅動程式之伺服器的名稱。

如果 *pName* 為 **Null**，此函式會列舉本機印表機驅動程式。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64、Windows x64 或 Windows NT R4000) 。 如果這個參數為 **Null**，則函式會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。

如果 *pEnvironment* 字串指定 "all"， **EnumPrinterDrivers** 會列舉安裝在指定伺服器上之所有平臺的印表機驅動程式。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PDriverInfo* 緩衝區中傳回的資訊結構類型。 它可以是下列其中一項。



| 值                                                                                                | 意義                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[擴展\]
</dt> <dd>

接收驅動程式資訊結構陣列的緩衝區指標 \_ \_ \* ，如同 *層級* 所指定。 每個結構都包含描述可用印表機驅動程式的資料。 緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。

若要判斷所需的緩衝區大小，請呼叫 **EnumPrinterDrivers** ，並將 *cbBuf* 設定為零。 **EnumPrinterDrivers** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PDriverInfo* 所指向的緩衝區大小（以位元組為單位）

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收在函式成功時複製到 *pDriverInfo* 緩衝區的位元組數目。 如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pDriverInfo* 緩衝區中傳回的結構數目。 這是安裝在指定列印伺服器上的印表機驅動程式數目。

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
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrinterDriversW** (Unicode) 和 **EnumPrinterDriversA** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 1**](driver-info-1.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 5**](driver-info-5.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

