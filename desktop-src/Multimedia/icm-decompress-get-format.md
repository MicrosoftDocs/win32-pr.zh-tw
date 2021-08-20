---
title: 'ICM_DECOMPRESS_GET_FORMAT 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 取得格式訊息會向 \_ 影片解壓縮驅動程式要求解壓縮資料的輸出格式。 您可以使用 ICDecompressGetFormat 宏明確地傳送此訊息。
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d6c6ca03cc442db4a84c6cd9595b50888e6953efc8badac83f3917f16c152b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988107"
---
# <a name="icm_decompress_get_format-message"></a>ICM \_解壓縮 \_ 取得 \_ 格式訊息

**ICM \_ 解壓縮 \_ 取得 \_ 格式** 訊息會向影片解壓縮驅動程式要求解壓縮資料的輸出格式。 您可以使用 [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_GET_FORMAT 
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

要包含輸出格式之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構的指標。 您可以指定零來要求輸出格式的大小，如同在 [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) 宏中一樣。

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

 

