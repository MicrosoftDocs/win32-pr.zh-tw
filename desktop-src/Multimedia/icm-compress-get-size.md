---
title: 'ICM_COMPRESS_GET_SIZE 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 取得 \_ 大小訊息要求當壓縮成指定的輸出格式時，影片壓縮驅動程式會提供一個資料框架的大小上限。 您可以使用 ICCompressGetSize 宏明確地傳送此訊息。
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934882"
---
# <a name="icm_compress_get_size-message"></a>ICM \_ 壓縮 \_ 取得 \_ 大小訊息

**ICM \_ 壓縮 \_ 取得 \_ 大小** 訊息要求當壓縮成指定的輸出格式時，影片壓縮驅動程式會提供一個資料框架的大小上限。 您可以使用 [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) 宏明確地傳送此訊息。


```C++
ICM_COMPRESS_GET_SIZE 
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

傳回單一壓縮框架可佔用的位元組數目上限。

## <a name="remarks"></a>備註

一般而言，應用程式會傳送此訊息，以判斷要為壓縮框架配置的緩衝區大小。

驅動程式應根據輸入和輸出格式來計算最大可能框架的大小。

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

 

