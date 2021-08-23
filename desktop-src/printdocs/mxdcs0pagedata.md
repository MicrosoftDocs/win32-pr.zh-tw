---
description: MXDC \_ S0PAGE \_ DATA \_ T 結構會保存 XPS 檔頁面，以傳遞至 Microsoft xps 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: 'MXDC_S0PAGE_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776548"
---
# <a name="mxdc_s0page_data_t-structure"></a>MXDC \_ S0PAGE \_ 資料 \_ T 結構

**MXDC \_ S0PAGE \_ DATA \_ T** 結構會保存 XPS 檔頁面，以傳遞至 MICROSOFT xps 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

輸出緩衝區的大小（ **bData**）。

</dd> <dt>

**bData**
</dt> <dd>

XPS 檔頁面。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md) 結構， (其 **opCode** 設定為 MXDCOP \_ set \_ S0PAGE) ，以建立 [**MXDC \_ S0PAGE \_ 通過 \_ ESCAPE \_ T**](mxdcs0pagepassthroughescape.md) 結構。 該結構接著會傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數，並以 [**MXDC \_ escape**](mxdc-escape.md)作為 ESCAPE 來呼叫它。 結果是 MXDC 會將頁面傳遞至輸出，而不進行處理。

呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間。

呼叫應用程式負責驗證 XPS 檔頁面的 XML。

如果您在使用 **MXDCOP \_ set \_ S0PAGE** 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，將 **MXDCOP \_ 設定 \_ S0PAGE \_ 資源** 作為頁面上每個資源的 **opCode** ，則串流耗用量會更有效率。

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

 

