---
title: 'ICM_DECOMPRESS_QUERY 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 查詢訊息會查詢影片解壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可將特定輸入格式解壓縮至特定的輸出格式。
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05edaa76f0d361741cb3ab5b274c63c2c2cc38ce5e388854f7056c3ea59d109f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987938"
---
# <a name="icm_decompress_query-message"></a>ICM \_解壓縮 \_ 查詢訊息

**ICM \_ 解壓縮 \_ 查詢** 訊息會查詢影片解壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可將特定輸入格式解壓縮至特定的輸出格式。 您可以使用 [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_QUERY 
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

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。 您可以為此參數指定零，以表示可接受任何輸出格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。

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

 

