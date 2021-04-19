---
description: MXDC \_ ESCAPE 印表機 escape 函式可讓應用程式透過 MICROSOFT XPS 檔轉換程式 (MXDC) ，以 XML 檔規格 (XPS) 格式將檔寫入檔案或印表機。
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: 'MXDC_ESCAPE 函式 (Mxdc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983621"
---
# <a name="mxdc_escape-function"></a>MXDC \_ ESCAPE 函式

**MXDC \_ ESCAPE** 印表機 escape 函式可讓應用程式透過 Microsoft XPS 檔轉換程式 (MXDC) ，以 XML 檔規格 (XPS) 格式將檔寫入檔案或印表機。

若要執行這項作業，請使用下列參數呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 函數。

## <a name="syntax"></a>語法


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* 
</dt> <dd>

印表機裝置內容的控制碼。

</dd> <dt>

*cbInput* 
</dt> <dd>

*LpszInData* 參數所指向之資料的大小（以位元組為單位）。

</dd> <dt>

*lpszInData* 
</dt> <dd>

包含輸入資料之緩衝區的指標，一律會儲存在下列其中一個結構中。

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

其中每個結構都有一個 opcode 成員，可指定 MXDC 的用途。 如需這些程式碼的詳細說明，請參閱 MxdcEscapeHeader。



| 作業程式碼 (opcode)                                                                                                                                                                                                   | 動作                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ 取得 \_ 檔案名**</dt> </dl>                                          | 將 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszOutData* 參數設定為，將輸出檔案的完整路徑設定為以零結尾的字串或該字串的大小。<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ**</dt> </dl> | 將列印票證與 XPS 固定檔順序產生關聯。<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ 固定 \_ 檔**</dt> </dl>              | 將列印票證與 XPS 檔產生關聯。<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**</dt> </dl>           | 將列印票證與 XPS 頁面產生關聯。<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE**</dt> </dl>                                                | 將目前頁面的 XPS 標記傳送至輸出。<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ 設定 \_ S0PAGE \_ 資源**</dt> </dl>                    | 將頁面上的資源（例如影像或字型）傳送至輸出。<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ 設定 \_ XPSPASSTHRU \_ 模式**</dt> </dl>                 | 將 MXDC 放入通過狀態，讓應用程式可以直接將 XPS 寫入輸出檔，而不需要 MXDC 任何處理。 您可以用這種方式撰寫整份檔或甚至是檔順序。<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

*LpszOutData* 參數所指向之資料的大小（以位元組為單位）。

</dd> <dt>

*lpszOutData* 
</dt> <dd>

包含輸出資料之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值大於零。 如果函數失敗或不受支援，則傳回值小於或等於零。

## <a name="remarks"></a>備註

MXDC 和 XPSDrv 支援此 escape，但 GDI 不支援。

若要判斷印表機驅動程式是否為 MXDC，請使用 [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 。 如果驅動程式是 MXDC，則 **ExtEscape** 會傳回以零結尾的字串 " http://schemas.microsoft.com/xps/2005/06 "。 請確定 *lpszOutData* 參數所參考的緩衝區夠大，足以容納這個字串。

若要判斷印表機驅動程式是否為 Windows 內建的 Microsoft XPS 檔寫入器驅動程式，請確認印表機驅動程式是否為 MXDC，然後判斷印表機驅動程式的名稱是否為 "Microsoft XPS Document Writer"。

若要取得印表機驅動程式名稱，請使用下列其中一種技術。 <dl> 將 *Level* 參數值設定為1時，呼叫 [**GetPrinterDriver**](getprinterdriver.md) 。 [**驅動程式 \_ 資訊 \_ 1**](driver-info-1.md)結構的 **pName** 成員會傳回印表機驅動程式名稱。  
或  
將 *Level* 參數值設定為2時，呼叫 [**GetPrinter**](getprinter.md) 。 印表機驅動程式名稱會傳回在 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **pDriverName** 成員中。  
</dl>

下表顯示在 XPS 檔案中尋找各種物件的位置，將會在其中寫入各種類型的物件。



| Object       | 輸出檔中的位置    |
|--------------|--------------------------------|
| 固定頁面   | /Documents/1/Pages/Esc%d.fpage |
| 縮圖    | /Documents/1/Metadata          |
| 列印票證 | /Documents/1/Metadata          |
| 字型         | /Documents/1/Resources/Fonts   |
| Image        | /Documents/1/Resources/Images  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mxdc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

