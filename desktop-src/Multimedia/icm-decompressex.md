---
title: 'ICM_DECOMPRESSEX 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX 訊息會通知影片壓縮驅動程式將資料框架直接解壓縮至螢幕、解壓縮至倒置的 DIB，或將來源和目的地矩形所描述的影像解壓縮。
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025365"
---
# <a name="icm_decompressex-message"></a>ICM \_ DECOMPRESSEX 訊息

**ICM \_ DECOMPRESSEX** 訊息會通知影片壓縮驅動程式將資料框架直接解壓縮至螢幕、解壓縮至倒置的 DIB，或將來源和目的地矩形所描述的影像解壓縮。


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

這則訊息與 [**ICM \_ 解壓縮**](icm-decompress.md) 類似，不同之處在于它會使用 [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) 結構來定義其解壓縮資訊。

如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。

如果在 [**ICM \_ DECOMPRESSEX \_ 開始**](icm-decompressex-begin.md) 訊息之前收到此訊息，驅動程式會傳回錯誤。

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

 

 





