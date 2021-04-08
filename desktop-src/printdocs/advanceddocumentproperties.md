---
description: AdvancedDocumentProperties 函式會顯示指定印表機的 [印表機設定] 對話方塊，讓使用者可以設定該印表機。
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: 'AdvancedDocumentProperties 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695015"
---
# <a name="advanceddocumentproperties-function"></a>AdvancedDocumentProperties 函式

**AdvancedDocumentProperties** 函式會顯示指定印表機的 [印表機設定] 對話方塊，讓使用者可以設定該印表機。

此函數是 [**DocumentProperties**](documentproperties.md) 函數的特殊案例。 如需詳細資訊，請參閱「備註」一節。

## <a name="syntax"></a>語法


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

印表機設定對話方塊的父視窗控制碼。

</dd> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機物件的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pDeviceName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應顯示印表機設定對話方塊的裝置名稱。

</dd> <dt>

*pDevModeOutput* \[擴展\]
</dt> <dd>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，此結構會包含使用者所指定的設定資料。

</dd> <dt>

*pDevModeInput* \[在\]
</dt> <dd>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，其中包含用來初始化 [印表機設定] 對話方塊之控制項的設定資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果具有這些參數的 [**DocumentProperties**](documentproperties.md) 函數成功，則 **AdvancedDocumentProperties** 的傳回值為1。 否則，傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

此功能只會顯示 [印表機設定] 對話方塊，讓使用者可以進行設定。 如需更多控制，請使用 [**DocumentProperties**](documentproperties.md)。 此函式的輸入參數會直接傳遞至 **DocumentProperties** ，而 *fMode* 值會在 \_ \_ \| \_ \_ 提示 \| dm \_ 輸出 \_ 緩衝區的緩衝區 DM 中設定為 DM。 與 **DocumentProperties** 不同，此函數只會傳回1或0。 因此，您無法藉由將 *pDevMode* 設定為零，判斷所需的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小。

應用程式可以透過呼叫 [**GetPrinter**](getprinter.md)函式，然後檢查 [**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的 **pPrinterName** 成員，來取得 *pDeviceName* 參數所指向的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AdvancedDocumentPropertiesW** (Unicode) 和 **AdvancedDocumentPropertiesA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




