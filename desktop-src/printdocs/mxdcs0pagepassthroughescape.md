---
description: MXDC \_ S0PAGE \_ 傳遞 \_ escape \_ t 結構是 \_ \_ \_ 與 MXDC \_ S0PAGE \_ 資料 \_ T 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: 'MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319571"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>MXDC \_ S0PAGE \_ 傳遞 \_ ESCAPE \_ T 結構

**MXDC \_ S0PAGE \_ 傳遞 \_ escape \_ t** 結構是與 [**MXDC \_ S0PAGE \_ 資料 \_ T**](mxdcs0pagedata.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>成員

<dl> <dt>

**mxdcEscape**
</dt> <dd>

[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員會設定為 **MXDCOP \_ set \_ S0PAGE**。

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

代表 XPS 檔頁面的 [**MxdcS0PageData**](mxdcs0pagedata.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫時，這個結構會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *LpszInData* 參數中傳遞，而 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ SET \_ S0PAGE**。 結果是 Microsoft XML 檔轉換器 (MXDC) 會將頁面傳送至印表機，而不需要處理。

配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間。

呼叫應用程式負責驗證 XPS 檔頁面的 XML。

如果您在使用 **MXDCOP \_ set \_ S0PAGE** 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，將 **MXDCOP \_ 設定 \_ S0PAGE \_ 資源** 作為頁面上每個資源的 **opCode** ，則串流耗用量會更有效率。

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

 

