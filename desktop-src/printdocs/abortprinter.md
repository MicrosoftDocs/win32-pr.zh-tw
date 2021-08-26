---
description: 如果印表機設定為可進行幕後處理，AbortPrinter 函式會刪除印表機多工緩衝處理檔案。
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: 'AbortPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c4d3bd7af58c0c927d01fad734ad58f59941815b1680e730f2569efcc6c00b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951028"
---
# <a name="abortprinter-function"></a>AbortPrinter 函式

如果印表機設定為可進行幕後處理， **AbortPrinter** 函式會刪除印表機的多工緩衝處理檔案。

## <a name="syntax"></a>語法


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

從刪除多工緩衝處理檔案之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

如果印表機未設定為進行幕後處理， **AbortPrinter** 函式不會有任何作用。

列印工作的順序如下所示：

1.  若要開始列印工作，請呼叫 [**StartDocPrinter**](startdocprinter.md)。
2.  若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。
3.  若要將資料寫入頁面，請呼叫 [**WritePrinter**](writeprinter.md)。
4.  若要結束每個頁面，請呼叫 [**EndPagePrinter**](endpageprinter.md)。
5.  視需要針對任意數量的頁面重複2、3和4。
6.  若要結束列印工作，請呼叫 [**EndDocPrinter**](enddocprinter.md)。

當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。 例如，列印大型 EMF 檔案時可能會發生這種情況。 頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。

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

 

 




