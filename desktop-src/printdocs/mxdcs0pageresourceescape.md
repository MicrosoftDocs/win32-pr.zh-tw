---
description: MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ t 結構是 \_ \_ \_ 與 MXDC \_ XPS \_ S0PAGE \_ 資源 \_ t 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: 'MXDC_S0PAGE_RESOURCE_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192714"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T 結構

**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ t** 結構是與 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ t**](mxdcxpss0pageresource.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>成員

<dl> <dt>

**mxdcEscape**
</dt> <dd>

[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員會設定為 MXDCOP \_ set \_ S0PAGE \_ RESOURCE。

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

XPS 檔頁面上代表資源的 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](mxdcxpss0pageresource.md) 結構，例如字型或影像檔案。

</dd> </dl>

## <a name="remarks"></a>備註

當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫該函式時，會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數中傳遞這個結構，而 [**MXDC \_ ESCAPE \_ 標頭 \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ SET \_ S0PAGE \_ 資源**。 結果是要傳送至 MXDC 的頁面資源。

配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間;不過，對 **StartPage** 和 **EndPage** 的呼叫之間可以有一個以上的呼叫。

如果您針對頁面上的每個資源使用 **MXDCOP \_ set \_ S0PAGE \_ RESOURCE** **opCode** 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) ，然後再使用 **MXDCOP \_ set \_ S0PAGE****opCode** 呼叫 **ExtEscape** ，串流耗用量就會更有效率。  

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

 

