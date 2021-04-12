---
description: GetPrinterDriver2 函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式，GetPrinterDriver2 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: 'GetPrinterDriver2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194970"
---
# <a name="getprinterdriver2-function"></a>GetPrinterDriver2 函式

**GetPrinterDriver2** 函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式， **GetPrinterDriver2** 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。

## <a name="syntax"></a>語法


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在中，選擇性\]
</dt> <dd>

視窗的控制碼，將用作驅動程式在安裝期間顯示之任何使用者介面（例如對話方塊）的父視窗。 如果此參數的值為 **Null**，則在安裝期間仍會向使用者顯示驅動程式的使用者介面，但不會有父視窗。

</dd> <dt>

*hPrinter* \[在\]
</dt> <dd>

應抓取驅動程式資料之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pEnvironment* \[在中，選擇性\]
</dt> <dd>

以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。 如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PDriverInfo* 緩衝區中傳回的印表機驅動程式結構。 此參數可以是下列其中一個值。



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

緩衝區的指標，此緩衝區會接收包含驅動程式相關資訊的結構（依 *層級* 所指定）。 緩衝區必須夠大，才能儲存結構成員所指向的字串。

若要判斷所需的緩衝區大小，請呼叫 **GetPrinterDriver2** ，並將 *cbBuf* 設定為零。 **GetPrinterDriver2** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回 **錯誤 \_ 的 \_ 緩衝區**，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PDriverInfo* 點的陣列大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

值的指標，如果函式成功則為，如果 *cbBuf* 太小，則會收到所需的位元組數目，以接收復制的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。 若要取得傳回狀態，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)、[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)、[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)、[**驅動程式 \_ 資訊 \_ 5**](driver-info-5.md)、[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)和 [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md)結構包含 **pDriverPath** 成員中印表機驅動程式的檔案名或完整路徑和檔案名。 應用程式可以藉由呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式並提供路徑和檔案名作為單一引數，來使用路徑和檔案名來載入印表機驅動程式。

此函數的 ANSI 版本，不支援 **GetPrinterDriver2A** ，而且會傳回 **\_ 不 \_ 支援的錯誤**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetPrinterDriver2W** (Unicode) <br/>                                                               |



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

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

