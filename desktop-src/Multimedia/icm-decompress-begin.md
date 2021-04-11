---
title: 'ICM_DECOMPRESS_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 開始訊息會通知影片解壓縮驅動程式準備將資料解壓縮。 您可以使用 ICDecompressBegin 宏明確地傳送此訊息。
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN message Windows 多媒體
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
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105437"
---
# <a name="icm_decompress_begin-message"></a>ICM \_ 解壓縮 \_ 開始訊息

**ICM \_ 解壓縮 \_ 開始** 訊息會通知影片解壓縮驅動程式準備將資料解壓縮。 您可以使用 [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) 宏明確地傳送此訊息。


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

當驅動程式收到此訊息時，它應該配置緩衝區，並進行任何耗時的作業，以便能夠有效率地處理 [**ICM 的 \_ 解壓縮**](icm-decompress.md) 訊息。

如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。

**Icm \_ 解壓縮 \_ 開始** 和 [**icm \_ 解壓縮 \_ 結束**](icm-decompress-end.md)訊息不會被嵌套。 如果您的驅動程式在使用 **icm \_ 解壓縮 \_ 結束** 解壓縮之前收到 **icm \_ 解壓縮 \_** ，則應該以新的參數重新開機解壓縮。

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

 

