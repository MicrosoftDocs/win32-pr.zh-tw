---
title: 'ICM_DECOMPRESS_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 開始訊息會通知影片解壓縮驅動程式準備解壓縮資料。 您可以使用 ICDecompressBegin 宏明確地傳送此訊息。
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678348"
---
# <a name="icm_decompress_begin-message"></a>ICM \_解壓縮 \_ 開始訊息

**ICM \_ 解壓縮 \_ 開始** 訊息會通知影片解壓縮驅動程式準備解壓縮資料。 您可以使用 [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_BEGIN 
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

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。

## <a name="remarks"></a>備註

當驅動程式收到此訊息時，它應該配置緩衝區，並進行任何耗時的作業，讓它可以有效率地處理 [**ICM \_ 解壓縮**](icm-decompress.md)訊息。

如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md)訊息。

**ICM \_ 解壓縮 \_ 開始** 和 [**ICM \_ 解壓縮 \_ 結束**](icm-decompress-end.md)訊息不會被嵌套。 如果您的驅動程式收到 ICM 解壓縮在使用 **ICM \_ 解壓縮 \_ 結束** 之前停止解壓縮，則應該以新的參數重新開機解壓縮。 **\_ \_**

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

 

