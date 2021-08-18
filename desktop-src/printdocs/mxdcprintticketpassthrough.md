---
description: MXDC 的 \_ PRINTTICKET \_ 資料 \_ T 結構會保存 XPS 檔列印票證，其中包含的印表機和列印工作設定，可傳遞給 Microsoft XPS 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: 'MXDC_PRINTTICKET_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471637"
---
# <a name="mxdc_printticket_data_t-structure"></a>MXDC \_ PRINTTICKET \_ 資料 \_ T 結構

**MXDC 的 \_ PRINTTICKET \_ 資料 \_ T** 結構會保存 XPS 檔列印票證，其中包含的印表機和列印工作設定，可傳遞給 MICROSOFT XPS 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>成員

<dl> <dt>

**dwDataSize**
</dt> <dd>

列印票證的大小（以位元組為單位）。

</dd> <dt>

**bData**
</dt> <dd>

XPS 檔列印票證。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md) 結構，此結構的 **opCode** 成員設定為 **MXDCOP \_ Printticket \_ fixed \_ PAGE**、 **MXDCOP \_ PRINTTICKET \_ fixed \_ doc** 或 **MXDCOP \_ PRINTTICKET 固定檔 \_ \_ \_ SEQ** ，以建立 MXDC 的 [**\_ printticket \_ ESCAPE \_ T**](mxdcprintticketescape.md) 結構。 **MXDC 的 \_ PRINTTICKET \_ escape \_ T** 結構接著會在使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫時，傳遞給 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數。 效果是將列印票證寫入至 XPS 檔檔。

如果作業 **碼** 設定為 **MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**，則對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須發生 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的呼叫。 如果 **opCode** 設定為 **MXDCOP \_ Printticket \_ 固定 \_** 檔或 **MXDCOP \_ printticket 固定檔 \_ \_ \_ SEQ**，則在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)與 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間必須進行 **ExtEscape** 的呼叫。

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

 

