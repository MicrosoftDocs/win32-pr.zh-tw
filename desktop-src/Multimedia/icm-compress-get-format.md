---
title: 'ICM_COMPRESS_GET_FORMAT 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 取得格式訊息會向 \_ 視訊壓縮驅動程式要求壓縮資料的輸出格式。 您可以使用 ICCompressGetFormat 宏明確地傳送此訊息。
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466476"
---
# <a name="icm_compress_get_format-message"></a>ICM \_ 壓縮 \_ 取得 \_ 格式訊息

**ICM \_ 壓縮 \_ 取得 \_ 格式** 訊息會向視訊壓縮驅動程式要求壓縮資料的輸出格式。 您可以使用 [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) 宏明確地傳送此訊息。


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

要包含輸出格式之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構的指標。 您可以為此參數指定零，以要求輸出格式的大小，如同在 [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) 宏中一樣。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *lpbiOutput* 為零，則會傳回結構的大小。

如果 *lpbiOutput* 為非零值，則會 \_ 在成功時傳回 ICERR OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果 *lpbiOutput* 為非零值，則驅動程式應該以對應至針對 *lpbiInput* 指定之輸入格式的預設輸出格式來填滿 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構。 如果壓縮程式可能會產生數種格式，預設格式應該是保留最大量資訊的格式。

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

 

