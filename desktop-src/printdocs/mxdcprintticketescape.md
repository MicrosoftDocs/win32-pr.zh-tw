---
description: MXDC \_ 的 printticket \_ escape \_ t 結構是 \_ \_ \_ 與 MXDC 的 \_ printticket \_ 資料 \_ t 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: 'MXDC_PRINTTICKET_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982721"
---
# <a name="mxdc_printticket_escape_t-structure"></a>MXDC \_ PRINTTICKET \_ ESCAPE \_ T 結構

**MXDC 的 \_ printticket \_ escape \_ t** 結構是與 [**MXDC 的 \_ printticket \_ 資料 \_ t**](mxdcprintticketpassthrough.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>成員

<dl> <dt>

**mxdcEscape**
</dt> <dd>

[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員設定為 MXDCOP \_ PRINTTICKET \_ 固定 \_ 頁面、MXDCOP \_ PRINTTICKET 固定檔 \_ \_ 或 MXDCOP \_ PRINTTICKET 固定檔 \_ \_ \_ SEQ。

</dd> <dt>

**printTicketData**
</dt> <dd>

包含列印票證的 [**MXDC \_ PRINTTICKET \_ 資料 \_ T**](mxdcprintticketpassthrough.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫該函式，而 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ printticket \_ fixed \_ PAGE**、 **MXDCOP \_ printticket \_ fixed \_ doc** 或 **MXDCOP \_ printticket \_ 固定檔 \_ \_ SEQ** 時，此結構會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數中傳遞。 結果是將列印票證寫入至 XPS 檔檔。

配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



如果作業 **碼** 設定為 **MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**，則對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須發生 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的呼叫。 如果 **opCode** 設定為 **MXDCOP \_ Printticket \_ 固定 \_** 檔或 **MXDCOP \_ printticket 固定檔 \_ \_ \_ SEQ**，則在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)與 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間必須進行 **ExtEscape** 的呼叫。

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

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

