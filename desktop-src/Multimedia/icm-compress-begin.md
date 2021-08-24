---
title: 'ICM_COMPRESS_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 開始訊息會通知影片壓縮驅動程式，準備壓縮資料。 您可以使用 ICCompressBegin 宏明確地傳送此訊息。
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33a6ee9c080e2dfc7a779abd4ae2a788bbe136ddcab1ef529714639065553ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140946"
---
# <a name="icm_compress_begin-message"></a>ICM \_壓縮 \_ 開始訊息

**ICM \_ 壓縮 \_ 開始** 訊息會通知影片壓縮驅動程式，準備壓縮資料。 您可以使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏明確地傳送此訊息。


```C++
ICM_COMPRESS_BEGIN 
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

如果如果 \_ \_ 不支援輸入或輸出格式，驅動程式支援指定的壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK。

## <a name="remarks"></a>備註

驅動程式應該在收到 [**ICM \_ 壓縮**](icm-compress.md)訊息時，配置和初始化其壓縮資料格式所需的任何資料表或記憶體。

bc-vcm-lvm-hyperv 會儲存最近 **ICM \_ 壓縮 \_ 開始** 訊息的設定。 **ICM \_ 壓縮 \_ BEGIN** 和 [**ICM \_ 壓縮 \_ 結束**](icm-compress-end.md)訊息不會被嵌套。 如果您的驅動程式收到 ICM 壓縮在使用 **ICM \_ 壓縮 \_ 結束** 之前停止壓縮，則應該以新的參數重新開機壓縮。 **\_ \_**

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

 

