---
description: MXDC \_ S0 \_ 頁面 \_ 列舉列舉是用來指定可與 XPS 檔中的頁面相關聯的資源類型，以及可由 Microsoft XPS 檔轉換器 (MXDC) 到其輸出的處理或傳遞的資源類型。
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: 'MXDC_S0_PAGE_ENUMS 列舉 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471312"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>MXDC \_ S0 \_ 頁面 \_ 列舉列舉

**MXDC \_ S0 \_ 頁面 \_** 列舉列舉是用來指定可與 XPS 檔中的頁面相關聯的資源類型，以及可由 MICROSOFT XPS 檔轉換器 (MXDC) 到其輸出的處理或傳遞的資源類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC \_ 資源 \_ TTF**
</dt> <dd>

TrueType 或 OpenType 字型。

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ 資源 \_ JPEG**
</dt> <dd>

JPEG 影像

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ 資源 \_ PNG**
</dt> <dd>

PNG 影像。

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ 資源 \_ TIFF**
</dt> <dd>

TIFF 影像。

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ 資源 \_ WDP**
</dt> <dd>

WindowsMedia 相片影像。

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC \_ 資源 \_ 字典**
</dt> <dd>

應傳遞給 MXDC 未處理之輸出的遠端資源字典。

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC \_ 資源 \_ ICC \_ 設定檔**
</dt> <dd>

應傳遞給 MXDC 未處理之輸出的 ICC 設定檔。

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC \_ 資源 \_ JPEG \_ 縮圖**
</dt> <dd>

應傳遞給 MXDC 未處理之輸出的 JPEG 縮圖。

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC \_ 資源 \_ PNG \_ 縮圖**
</dt> <dd>

應該傳遞給 MXDC 未處理之輸出的 PNG 縮圖。

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ 資源 \_ 上限**
</dt> <dd>

驗證的最大資源計數。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉主要是用來做為 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](mxdcxpss0pageresource.md)結構的 **dwResourceType** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



 

 




