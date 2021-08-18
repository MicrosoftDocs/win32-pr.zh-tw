---
description: WritePrinter 函數會通知列印多工緩衝處理器，資料應該寫入指定的印表機。
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: 'WritePrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4b8b413854f8634477f7fec9010f4306587a093bd5c791b1b7d0117b6c3ef91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971157"
---
# <a name="writeprinter-function"></a>WritePrinter 函式

**WritePrinter** 函數會通知列印多工緩衝處理器，資料應該寫入指定的印表機。

> [!Note]  
> **WritePrinter** 只支援 GDI 列印，且不能用於 XPS 列印。 如果您的列印工作使用 XPS 或 OpenXPS 列印路徑，請使用 [Xps 列印 API](/windows/desktop/printdocs/xps-printing)。 不支援使用 **WritePrinter** 將 XPS 或 OpenXPS 列印工作傳送至多工緩衝處理器，而且可能會導致無法確定的結果。

 

## <a name="syntax"></a>語法


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pBuf* \[在\]
</dt> <dd>

位元組陣列的指標，其中包含應寫入印表機的資料。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

陣列的大小（以位元組為單位）。

</dd> <dt>

*pcWritten* \[擴展\]
</dt> <dd>

值的指標，此值會接收寫入至印表機的資料位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

列印工作的順序如下所示：

1.  若要開始列印工作，請呼叫 [**StartDocPrinter**](startdocprinter.md)。
2.  若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。
3.  若要將資料寫入頁面，請呼叫 **WritePrinter**。
4.  若要結束每個頁面，請呼叫 [**EndPagePrinter**](endpageprinter.md)。
5.  視需要針對任意數量的頁面重複2、3和4。
6.  若要結束列印工作，請呼叫 [**EndDocPrinter**](enddocprinter.md)。

當高階檔 (（例如 Adobe PDF 或 Microsoft Word 檔案) 或其他印表機資料 (這類 PCL、PS 或 HPGL) 直接傳送到印表機時，檔中定義的列印設定會優先于 Windows 列印設定。 當在 [**StartDocPrinter**](startdocprinter.md)呼叫的 *pDocInfo* 參數中傳遞的 [**DOC \_ INFO \_ 1**](doc-info-1.md)結構之 *pDatatype* 成員的值為「未經處理」時，檔會輸出，必須完整地以硬體理解的語言描述 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)樣式的列印工作設定。

在 Windows XP 之前的 Windows 版本中，當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。 例如，列印大型 EMF 檔案時可能會發生這種情況。 Windows XP 之前的 Windows 版本中的頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。 在 Windows XP 和更新版本的 Windows 中，EMF 檔案的大小必須小於或等於2gb。 如果使用 **WritePrinter** 來寫入非 EMF 資料（例如印表機就緒的 PDL），檔案的大小只受限於可用磁碟空間。

## <a name="examples"></a>範例

如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

