---
description: DocumentEvent 函數是與列印檔案相關聯之事件的事件處理常式。
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: 'DocumentEvent 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0c38a95c4e0dc9820130e467c971c0adb5b9df0ede248506ed56f963c3246b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971597"
---
# <a name="documentevent-function"></a>DocumentEvent 函式

**DocumentEvent** 函數是與列印檔案相關聯之事件的事件處理常式。

## <a name="syntax"></a>語法


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機物件的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*hdc* \[在\]
</dt> <dd>

由呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)所產生的裝置內容控制碼。 如果 *iEsc* 設為 DOCUMENTEVENT CREATEDCPRE，則為零 \_ 。 如需在64位版 Windows 上從32位應用程式列印的限制，請參閱備註。

</dd> <dt>

*iEsc* 
</dt> <dd>

用來識別要處理之事件的轉義碼。 這個參數可以是下列其中一個整數常數。



| 常數                                                                                                                                                                                                                                                                                                                                               | 事件                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI 即將處理其 [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) 函式的呼叫。<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI 剛剛處理過其 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 或 [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica) 函數的呼叫。<br/> 除非先前已呼叫 **DocumentEvent** 並將 *IESC* 設為 DocumentEvent CREATEDCPRE，否則不應使用此 escape 程式碼 \_ 。<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI 即將處理其 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 或 [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica) 函數的呼叫。<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI 即將處理其 [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) 函式的呼叫。<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI 剛剛已處理其 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 函式的呼叫。<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE 或 DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI 即將處理其 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 函式的呼叫。<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI 即將處理其 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) 函式的呼叫。<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | GDI 即將處理其 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 函式的呼叫。<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | DOCUMENTEVENT \_ QUERYFILTER 事件代表一個機會，讓多工緩衝處理器查詢驅動程式，以取得 \_ 驅動程式將回應的 DOCUMENTEVENT *XXX* 事件清單。 此事件會在呼叫傳遞 DOCUMENTEVENT CREATEDCPRE 事件的 **DocumentEvent** 之前發出 \_ 。<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI 剛剛已處理其 [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) 函式的呼叫。<br/> 除非先前已呼叫 **DocumentEvent** 並將 *IESC* 設為 DocumentEvent RESETDCPRE，否則不應使用此 escape 程式碼 \_ 。<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI 即將處理其 [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) 函式的呼叫。<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI 剛剛已處理其 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函式的呼叫。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE 或 DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI 即將處理其 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函式的呼叫。<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI 即將處理其 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 函數的呼叫。<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

*PvIn* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pvIn* \[在\]
</dt> <dd>

緩衝區的指標。 緩衝區所包含的內容，取決於 *iEsc* 的值，如下表所示。



| 常數                                                                                                                                                                                                                                                                                                                                               | pvin 內容                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | 未使用。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* 包含對這個函式的前一個呼叫中， *pvOut* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構之指標的位址，其 *iEsc* 參數已設定為 DOCUMENTEVENT \_ CREATEDCPRE。<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* \_ 會指向 [Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)中記載的 DOCEVENT CREATEDCPRE 結構。<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | 未使用。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | 未使用。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE 或 DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | 未使用。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | 未使用。<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | *pvIn* \_ 會指向 [Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)中記載的 DOCEVENT ESCAPE 結構。<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | 與 DOCUMENTEVENT CREATEDCPRE 相同 \_ 。<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* 包含對這個函式的前一個呼叫中， *pvOut* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構之指標的位址，其 *iEsc* 參數已設定為 DOCUMENTEVENT \_ RESETDCPRE。<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* 包含 [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)呼叫端所提供的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構之指標的位址。<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* 會指向 LONG，以指定 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)所傳回的列印工作識別碼。<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE 或 DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* 包含 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)之呼叫者所提供之 [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)結構的指標位址。<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | 未使用。<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| 值                       | 意義                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | *PvOut* 之緩衝區指標的大小（以位元組為單位）。                             |
| DOCUMENTEVENT \_ ESCAPE       | 值，用來做為 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的 *cbOutput* 參數。 |
| 適用于所有其他值        | 未使用 *iEsc* 。                                                                  |



 

</dd> <dt>

*pvOut* \[擴展\]
</dt> <dd>

緩衝區的指標。 緩衝區的內容取決於提供給 *iEsc* 的值，如下表所示。



| 常數                                                                                                                                                                                          | pvOut 內容                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | 以驅動程式提供的 DEVMODE 結構指標，GDI 會使用此結構，而不是 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)呼叫端所提供的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構。  (如果是 **Null**，GDI 會使用呼叫端提供的結構。 ) <br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                | 用來當做 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)之 *lpszOutData* 參數的緩衝區指標。<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | 包含 DOCEVENT 篩選結構的緩衝區指標，該 \_ 結構記載于[Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)中。<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | 以驅動程式提供的 DEVMODE 結構指標，GDI 會使用此結構，而不是 [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)呼叫端所提供的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構。  (如果是 **Null**，GDI 會使用呼叫端提供的結構。 ) <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

函數的傳回值相依于為 *iEsc* 提供的 escape。 某些 escape 程式碼不會使用傳回值 (請參閱以下) 。 如果函式提供傳回值，則必須是下列其中一項。



| 傳回值               | 意義                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ 失敗     | 驅動程式支援 *iEsc* 所識別的 escape 程式碼，但發生失敗。 |
| DOCUMENTEVENT \_ 成功     | 驅動程式已成功處理 *iEsc* 所識別的 escape 程式碼。             |
| \_不支援 DOCUMENTEVENT | 驅動程式不支援 *iEsc* 所識別的 escape 程式碼。                 |



 

下列清單指出哪些 escape 程式碼需要傳回值，哪些不是，並說明 DOCUMENTEVENT \_ SUCCESS、DOCUMENTEVENT \_ 失敗和 DOCUMENTEVENT 不支援的傳回碼的意義 \_ 。



| 傳回值                                          | 意義                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | DOCUMENTEVENT \_ 失敗-GDI 不會建立裝置內容或資訊內容，而且會針對 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 或 [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica)提供0的傳回值。 |
| DOCUMENTEVENT \_ DELETEDC                               | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE 或 DOCUMENTEVENT \_ ENDDOC     | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ ESCAPE                                 | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | 請參閱＜備註＞。                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | 不會使用傳回值，也不應讀取。                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | DOCUMENTEVENT \_ 失敗-GDI 不會重設裝置內容，並為 [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)提供傳回值0。                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | DOCUMENTEVENT \_ 失敗-GDI 會呼叫 [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) 來停止檔，然後 \_ 針對 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)提供 SP ERROR 的傳回值。                      |
| DOCUMENTEVENT \_ STARTDOCPRE 或 DOCUMENTEVENT \_ STARTDOC | DOCUMENTEVENT \_ 失敗-GDI 不會開機檔案，並且針對 StartDoc 提供 SP ERROR 的傳回值 \_ 。 [](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | DOCUMENTEVENT \_ 失敗-GDI 不會啟動頁面，而且會針對 StartPage 提供傳回值的 SP \_ ERROR [****](/windows/desktop/api/Wingdi/nf-wingdi-startpage)。                                                         |



 

## <a name="remarks"></a>備註

針對 DOCUMENTEVENT QUERYFILTER 的 *iEsc* 值 \_ ，多工緩衝處理器可以 \_ 用兩種方式來解讀 **DOCUMENTEVENT** 所傳回的 DOCUMENTEVENT SUCCESS 值，這取決於驅動程式是否修改了 DOCEVENT 篩選結構的特定成員 \_ (，其記載于 [Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)) 。  (*pvOut* 參數指向此結構。當多工緩衝處理器為此類型的結構配置記憶體時，) 它會將此結構的兩個成員（ **cElementsReturned** 和 **cElementsNeeded**）初始化為已知的值。 **DocumentEvent** 傳回之後，多工緩衝處理器會判斷這些成員的值是否已變更，並使用該資訊來解讀 **DocumentEvent** 傳回值。 下表摘要說明這種情況。



| 傳回值                          | CElementsReturned 和 cElementsNeeded 的狀態    | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ 成功<br/>     | 驅動程式對任一成員都沒有任何變更。<br/> | 多工緩衝處理器會將此傳回值解釋為相當於 \_ 不支援的 DOCUMENTEVENT。 多工緩衝處理器無法從驅動程式抓取事件篩選器，因此它會持續呼叫所有事件的 **DocumentEvent** 。<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ 成功<br/>     | 驅動程式已寫入一個或兩個成員。<br/>    | 多工緩衝處理器會接受此傳回值而不需要解讀。 如果驅動程式只寫入其中一個 **cElementsNeeded** 和 **cElementsReturned**，則多工緩衝處理器會將未變更的成員視為值為零。<br/> 多工緩衝處理器會篩選出 DOCEVENT 篩選 (的 **aDocEventCall** 成員中列出的所有事件， \_ 這些事件記載于 [Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)) 。<br/> |
| \_不支援 DOCUMENTEVENT<br/> | 不適用<br/>                          | 驅動程式不支援 DOCUMENTEVENT \_ QUERYFILTER。<br/> 多工緩衝處理器無法從驅動程式抓取事件篩選器，因此它會持續呼叫所有事件的 **DocumentEvent** 。<br/>                                                                                                                                                                                                                                            |
| DOCUMENTEVENT \_ 失敗<br/>     | 不適用<br/>                          | 驅動程式支援 DOCUMENTEVENT \_ QUERYFILTER，但遇到內部錯誤。<br/> 多工緩衝處理器無法從驅動程式抓取事件篩選器，因此它會持續呼叫所有事件的 **DocumentEvent** 。<br/>                                                                                                                                                                                                                 |



 

如果 *iEsc* 參數中提供的 escape 程式碼為 DOCUMENTEVENT \_ CREATEDCPRE，則適用下列規則：

-   如果作業是直接傳送到印表機而不需要進行幕後處理，>pvIn 會指向印表機名稱。  (需詳細資訊，請參閱 \_ [Windows 驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)中的 DOCEVENT CREATEDCPRE 結構檔。 ) 
-   如果作業正在進行多工緩衝處理，pvIn >pszDevice 會指向印表機埠名稱。

> [!Note]  
> 在64位版本的 Windows 上執行32位應用程式時，適用下列限制。 **DocumentEvent** 應該呼叫的唯一 GDI 函數是 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)，而且只應使用私用的轉義。 **DocumentEvent** 對其他 GDI 函數的呼叫可能會產生未定義的行為。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DocumentEventW** (Unicode) 和 **DocumentEventA** (ANSI) <br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows驅動程式開發工具組](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

