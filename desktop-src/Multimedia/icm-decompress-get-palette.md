---
title: 'ICM_DECOMPRESS_GET_PALETTE 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 取得 \_ 調色板訊息要求影片解壓縮驅動程式提供輸出 BITMAPINFOHEADER 結構的色彩表。 您可以使用 ICDecompressGetPalette 宏明確地傳送此訊息。
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998024"
---
# <a name="icm_decompress_get_palette-message"></a>ICM \_ 解壓縮 \_ 取得 \_ 選用區訊息

**ICM \_ 解壓縮 \_ 取得 \_ 調色板** 訊息要求影片解壓縮驅動程式提供輸出 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的色彩表。 您可以使用 [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的指標，其中包含輸入格式。

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

要包含色彩表之 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) 結構的指標。 為色彩表保留的空間一律為至少256的色彩。 您可以為此參數指定零，只傳回色彩表的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果 *lpbiOutput* 為非零值，驅動程式會將 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))的 **biClrUsed** 成員設定為 color 資料表中的色彩數目。 驅動程式會以實際的色彩填滿 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)的 **bmiColors** 成員。

驅動程式只有在使用輸入格式所指定的調色板時，才應該支援此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

