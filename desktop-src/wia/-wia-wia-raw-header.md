---
description: WIA \_ 原始 \_ 標頭結構會以裝置的原始資料格式來定義影像，並可讓應用程式在 Windows 映像取得 (WIA) 傳輸中使用原始格式。
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: 'WIA_RAW_HEADER 結構 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 2b4e89f47737788fa9ebf238f06f6420eafbc31d7b27ab7933372d0716fb6588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812948"
---
# <a name="wia_raw_header-structure"></a>WIA \_ 原始 \_ 標頭結構

**WIA \_ 原始 \_ 標頭** 結構會以裝置的原始資料格式來定義影像，並可讓應用程式在 Windows 映像取得 (WIA) 傳輸中使用原始格式。

## <a name="syntax"></a>語法


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**Tag**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

格式的名稱。 這必須是常值 ' WRAW ' (四個單一位元組 ASCII 字元) 。

</dd> <dt>

**版本**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

原始格式的版本。 一律使用0x00010000。

</dd> <dt>

**HeaderSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

標頭中的有效位元組總數。

</dd> <dt>

**XRes**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

水平解析度 (單位為 DPI)。

</dd> <dt>

**YRes**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

垂直解析度 (單位為 DPI)。

</dd> <dt>

**範圍**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

影像的寬度（以圖元為單位）。

</dd> <dt>

**YExtent**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

影像的高度（以圖元為單位）。

</dd> <dt>

**BytesPerLine**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

未壓縮影像行中的位元組數目。 當資料壓縮時使用0，表示每行的位元組數目未知。

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

所有圖元通道的每個圖元的位元組總數。

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

圖元中的色彩聲道數目。

</dd> <dt>

**DataType**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

影像的 WIA \_ IPA \_ 資料類型。 由於 WIA \_ IPA \_ 格式設定為 [WiaImgFmt \_ RAW]，這是應用程式所挑選的允許值清單。

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

類型： **位元組**

</dd> <dd>

通道中的位數，最大值為8。

</dd> <dt>

**壓縮**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

WIA \_ IPA \_ 壓縮值，指定所使用的壓縮類型（如果有的話）。

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

WIA \_ IPA \_ PHOTOMETRIC \_ INTERP 值，指定影像的 PHOTOMETRIC 轉譯。

</dd> <dt>

**LineOrder**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

代表影像行順序的值。 這一律是從 \_ \_ 上到下的 wia 行順序，或是從 \_ \_ \_ \_ \_ \_ 下 \_ 到 \_ 上的 wia 行順序。

</dd> <dt>

**RawDataOffset**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

原始影像資料的位置（以位元組為單位），從標頭結尾的位置或調色板結束的位置開始。

</dd> <dt>

**RawDataSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

原始影像資料的大小（以位元組為單位）。

</dd> <dt>

**PaletteOffset**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

元件的位置，以位元組為單位，從標頭結尾的位置或資料結束的位置開始。  (如果沒有任何調色板，則此值為0。 ) 

</dd> <dt>

**PaletteSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

調色板資料表的大小（以位元組為單位）。  (如果沒有任何調色板，則為0。 ) 

</dd> </dl>

## <a name="remarks"></a>備註

因為這不是檔案格式，所以請針對 WIA \_ IPA \_ 副檔名屬性使用空字串 \_ 。

選擇區和資料可能會以任何順序出現。

**RawDataSize** 不包含標頭或調色板。 使用此欄位來確認是否已成功傳送映射。

**PaletteSize** 是位元組，而不是調色板中的專案數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




