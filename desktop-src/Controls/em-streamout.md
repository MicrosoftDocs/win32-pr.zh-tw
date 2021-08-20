---
title: 'EM_STREAMOUT 訊息 (Richedit .h) '
description: 讓 rich edit 控制項將其內容傳遞至應用程式 \ 8211; 定義的 EditStreamCallback 回呼函式。 回呼函數接著可以將資料串流寫入檔案或它所選擇的任何其他位置。
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63236083c1964d29cb915e4bfc51303b30b730e01f76f2b186cc200d1dcfce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019466"
---
# <a name="em_streamout-message"></a>EM \_ STREAMOUT 訊息

讓 rich edit 控制項將其內容傳遞至應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函數。 回呼函數接著可以將資料串流寫入檔案或它所選擇的任何其他位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定資料格式和取代選項。

此值必須是下列其中一個值。



| 值                                                                                                                                                      | 意義                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | RTF。<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTFNOOBJS**</dt> </dl> | 以空格取代 COM 物件的 RTF。<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ 文字**</dt> </dl>                | 具有空格的文字，用來取代 COM 物件。<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ TEXTIZED**</dt> </dl>    | 具有 COM 物件文字表示的文字。<br/> |



 

如果應用程式儲存 COM 物件本身， **SF \_ RTFNOOBJS** 選項會很有用，因為 RTF 表示 com 物件並不太精簡。 \\Objattph，後面接著一個空格的控制字代表物件位置。

此外，您可以指定下列旗標。



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | 如果有指定，rich edit 控制項會只串流所有語言通用的關鍵字，並忽略語言特定關鍵字。 如果未指定，rich edit 控制項會串流所有關鍵詞。 您可以結合此旗標與 **sf \_ RTF** 或 **sf \_ RTFNOOBJS** 旗標。<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SFF \_ 選取專案**</dt> </dl>    | 如果有指定，rich edit 控制項會只串流目前選取範圍的內容。 如果未指定，控制項會串流處理整個內容。 您可以結合此旗標與任何資料格式值。<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>             | **Microsoft Rich Edit 2.0 和更新版本：** 指出 Unicode 文字。 您可以結合此旗標與 **SF \_ 文字** 旗標。<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ USECODEPAGE**</dt> </dl> | **Rich Edit 3.0 和更新版本：** 使用其他字碼頁產生 UTF-8 RTF 以及文字。 字碼頁是在 *wParam* 的最高字組中設定。 例如，若是 UTF-8 RTF，請將 *wParam* 設定為 (CP \_ UTF8 << 16) \| sf \_ USECODEPAGE \| sf \_ RTF。<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的指標。 在輸入時，此結構的 **pfnCallback** 成員必須指向應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 函數。 在輸出中，如果發生錯誤， **dwError** 成員可以包含非零的錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回寫入至資料流程的字元數。

## <a name="remarks"></a>備註

當您傳送 **EM \_ STREAMOUT** 訊息時，rich Edit 控制項會對 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **pfnCallback** 成員所指定的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)函數進行重複呼叫。 每次呼叫回呼函式時，控制項都會傳遞包含控制項內容部分的緩衝區。 此程式會繼續進行，直到控制項將其所有內容都傳遞給回呼函式，或直到發生錯誤為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





