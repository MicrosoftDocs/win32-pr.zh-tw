---
title: 'ICM_DRAW 訊息 (Vfw .h) '
description: ICM \_ 描繪訊息會通知轉譯驅動程式將資料框架解壓縮，並將其繪製到螢幕。
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685825"
---
# <a name="icm_draw-message"></a>ICM \_ 繪製訊息

**ICM \_ 描繪** 訊息會通知轉譯驅動程式將資料框架解壓縮，並將其繪製到螢幕。


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

[**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果 ICDRAW \_ 更新旗標是在 [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)的 **dwFlags** 成員中設定，則用於繪圖的畫面區域無效，需要更新。 更新的範圍取決於 **lpData** 成員的內容而定。

如果 **lpData** 為 **Null**，驅動程式應該使用目前的影像來更新整個目的地矩形。 如果驅動程式在非螢幕緩衝區中維護映射的複本，它可能會讓此訊息失敗。 如果 **lpData** 不是 **Null**，驅動程式應該繪製資料，並確定整個目的地都已更新。

如果 \_ 已在 **dwFlags** 中設定 ICDRAW HURRYUP 旗標，則呼叫的應用程式會希望驅動程式儘快進行，甚至可能不會更新螢幕。

如果在 \_ **dwFlags** 中設定 ICDRAW 預先設置旗標，此影片畫面會是初步資訊，而且不應該在可能的情況下顯示。 例如，如果播放是從畫面格10開始，而框架0是最接近的先前主要畫面格，則畫面格0到9將會設定 ICDRAW 的預先 \_ 設定。

如果您希望驅動程式將資料解壓縮到緩衝區中，請傳送 [**ICM \_ 解壓縮**](icm-decompress.md) 訊息。

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

 

 





