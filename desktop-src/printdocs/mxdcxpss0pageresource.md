---
description: MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T 結構會保存與 XPS 檔頁面相關聯的資源（例如影像或字型）相關資訊，並將其傳遞至 Microsoft XPS 檔轉換器 (MXDC) 輸出檔。
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: 'MXDC_XPS_S0PAGE_RESOURCE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971177"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T 結構

**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T** 結構會保存與 XPS 檔頁面相關聯的資源（例如影像或字型）相關資訊，並將其傳遞至 Microsoft xps 檔轉換器 (MXDC) 輸出檔。

## <a name="syntax"></a>語法


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

此結構和其指向的資源的總大小。

</dd> <dt>

**dwResourceType**
</dt> <dd>

[**MXDC \_ S0 \_ 頁面 \_**](mxdcs0pageenums.md)列舉類型的值，指出資源的類型，例如 TIFF 影像或 TrueType 字型。

</dd> <dt>

**szUri**
</dt> <dd>

資源的 URI。 這不能超過260個位元組。

</dd> <dt>

**dwDataSize**
</dt> <dd>

資源的大小（以位元組為單位）。

</dd> <dt>

**bData**
</dt> <dd>

資源的資料，大小為 1 + 資源大小的位元組陣列。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md) 結構 (，其作業 **碼** 設定為 **MXDCOP \_ set \_ S0PAGERESOURCE**) 以建立 [**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T**](mxdcs0pageresourceescape.md) 結構。 產生的 **MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T** 結構接著會傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數，並使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫它。 效果是將資源傳送至 MXDC 進行轉換，並寫入輸出檔。

呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間;不過，對 **StartPage** 和 **EndPage** 的呼叫之間可以有一個以上的呼叫。

如果您針對頁面上的每個資源使用 **MXDCOP \_ set \_ S0PAGE \_ RESOURCE** **opCode** 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) ，然後再使用 **MXDCOP \_ set \_ S0PAGE** **opCode** 呼叫 **ExtEscape** ，串流耗用量就會更有效率。

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

 

