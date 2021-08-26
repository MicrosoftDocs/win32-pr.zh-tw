---
description: MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T 結構會保存 Microsoft XPS 檔轉換器的完整路徑和檔案名， (MXDC) 輸出檔。
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: 'MXDC_GET_FILENAME_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ef0b29590b4a9080e943fae5c3e78fb18a99232a2a531a80b63b303b28c2bea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948338"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T 結構

**MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T** 結構會保存 Microsoft XPS 檔轉換器的完整路徑和檔案名， (MXDC) 輸出檔。

## <a name="syntax"></a>語法


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>成員

<dl> <dt>

**cbOutput**
</dt> <dd>

輸出緩衝區的大小（ **wszData**）。

</dd> <dt>

**wszData**
</dt> <dd>

輸出檔的完整路徑和檔案名。

</dd> </dl>

## <a name="remarks"></a>備註

當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，會傳回這個結構，而且在 *lpszInData* 參數中傳遞的 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構會將其 **opCode** 設定為 **MXDCOP \_ 取得 \_ 檔案名**。

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

 

