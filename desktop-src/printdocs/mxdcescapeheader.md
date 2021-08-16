---
description: MXDC \_ escape \_ HEADER \_ T 結構會保存使用 MXDC \_ ESCAPE 作為 nEscape 參數之 ExtEscape 呼叫的作業程式碼。 它也會提供輸入和輸出緩衝區的大小。
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: 'MXDC_ESCAPE_HEADER_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 53dd83e362ab21938121a986ee2402076d72f870460bc9db608b9a048cee0f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099072"
---
# <a name="mxdc_escape_header_t-structure"></a>MXDC \_ ESCAPE \_ HEADER \_ T 結構

**MXDC \_ escape \_ HEADER \_ T** 結構會保存使用 [**MXDC \_ ESCAPE**](mxdc-escape.md)作為 *nEscape* 參數之 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)呼叫的作業程式碼。 它也會提供輸入和輸出緩衝區的大小。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>成員

<dl> <dt>

**cbInput**
</dt> <dd>

將傳遞給 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數之 *lpszOutData* 參數的輸入緩衝區大小。

</dd> <dt>

**cbOutput**
</dt> <dd>

輸出緩衝區的大小。 這與 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *cbOutput* 參數值相同。

</dd> <dt>

**opCode**
</dt> <dd>

告訴 MXDC 要做什麼的程式碼常數。



| 作業碼                      | 描述                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ 取得 \_ 檔案名                | 在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszOutData* 參數中，傳回輸出檔案的完整路徑（以零終止的字串或該字串的大小）。 請參閱＜備註＞。                   |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ | 將列印票證與 XPS 固定檔順序產生關聯。                                                                                                                                                         |
| MXDCOP \_ PRINTTICKET \_ 固定 \_ 檔      | 將列印票證與 XPS 檔產生關聯。                                                                                                                                                                        |
| MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面     | 將列印票證與 XPS 頁面產生關聯。                                                                                                                                                                            |
| MXDCOP \_ SET \_ S0PAGE                  | 將目前頁面的 XPS 標記傳送至輸出。                                                                                                                                                                |
| MXDCOP \_ 設定 \_ S0PAGE \_ 資源        | 將頁面上的資源（例如影像或字型）傳送至輸出。                                                                                                                                                 |
| MXDCOP \_ 設定 \_ XPSPASSTHRU \_ 模式       | 將 MXDC 置於傳遞狀態，讓應用程式可以直接將 XPS 寫入輸出檔，而不需要 MXDC 任何處理。 您可以用這種方式撰寫整份檔或甚至是檔順序。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

在呼叫 [**MXDC \_ escape**](mxdc-escape.md)之前， \_ 應用程式應該先使用 [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) ESCAPE 呼叫 [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)來確認驅動程式是否已 MXDC。 如果驅動程式是 MXDC，則函式會傳回以零結尾的字串 " http://schemas.microsoft.com/xps/2005/06 "。

此結構一律是在其 *lpszInData* 參數中傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的資料開頭。

當 **opCode** 為 MXDCOP 時， \_ 取得 \_ 檔案名：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數只包含 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構。
-   藉由呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 兩次來取得輸出檔案名。
    1.  第一次將4傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的 *cbOutput* 參數。 將 *lpszOutData* 參數設定為指向任何已配置的4位元組記憶體。 完整檔案路徑的大小會在 **ExtEscape** 的 *lpszOutData* 參數中傳回。
    2.  然後再呼叫一次函數。 這次將 *cbOutput* 和 *cbInput* 設定為 4 + *DataSize*。 完整檔案路徑會在 [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) 結構中傳回。

當 **opCode** 為 MXDCOP \_ printticket \_ 固定 \_ 檔 \_ SEQ 或 MXDCOP 的 \_ printticket \_ 固定 \_ 檔時：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)結構的 [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)結構所組成。
-   呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 和 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間進行。

當 **opCode** 為 MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)結構的 [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)結構所組成。
-   對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫。

當 **opCode** 為 MXDCOP \_ SET \_ S0PAGE 時：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md)結構的 [**MxdcS0PageData**](mxdcs0pagedata.md)結構所組成。
-   對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫。
-   呼叫應用程式負責驗證 XML。
-   如果您在使用 MXDCOP set S0PAGE 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 時，將 MXDCOP \_ 設定 \_ S0PAGE \_ 資源作為頁面上每個資源的 **opCode** ， \_ 則串流耗用量會更有效率 \_ 。

當 **opCode** 為 MXDCOP \_ SET \_ S0PAGE \_ RESOURCE：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)結構的 [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md)結構所組成。
-   對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫，但在 **startpage** 和 **EndPage** 呼叫之間可能會有多個這類呼叫。
-   如果您在使用 MXDCOP set S0PAGE 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 時，將 MXDCOP \_ 設定 \_ S0PAGE \_ 資源作為頁面上每個資源的 **opCode** ， \_ 則串流耗用量會更有效率 \_ 。

當 **opCode** 為 MXDCOP \_ SET \_ XPSPASSTHRU \_ 模式時：

-   [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數只包含 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構。
-   此呼叫必須在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)之前發生。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mxdc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

