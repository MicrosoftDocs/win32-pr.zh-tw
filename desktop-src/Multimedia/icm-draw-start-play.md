---
title: 'ICM_DRAW_START_PLAY 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 開始 \_ 播放訊息提供轉譯驅動程式播放作業的開始和結束時間。 您可以使用 ICDrawStartPlay 宏明確地傳送此訊息。
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094399"
---
# <a name="icm_draw_start_play-message"></a>ICM \_ DRAW \_ 開始 \_ 播放訊息

**ICM \_ DRAW \_ 開始 \_ 播放** 訊息提供轉譯驅動程式播放作業的開始和結束時間。 您可以使用 [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) 宏明確地傳送此訊息。


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

開始時間。

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*
</dt> <dd>

結束時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

這則訊息會在傳送至轉譯驅動程式的任何框架資料之前。

*LFrom* 和 *lTo* 的單位是以 [**ICM \_ 繪製 \_ 開始**](icm-draw-begin.md)訊息來指定。 對於影片資料，這通常是畫面格編號。 如需播放速率的詳細資訊，請參閱 [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)結構的 **dwRate** 和 **dwScale** 成員。

如果結束時間小於開始時間，則會反轉播放方向。

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

 

 





