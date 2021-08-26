---
description: 顯示模式已變更。
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: 'EC_DISPLAY_CHANGED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee75517c1927d7f819565d796d9f15fb21050ef7b4ead86d98f582018cc66b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965918"
---
# <a name="ec_display_changed"></a>EC \_ 顯示 \_ 已變更

顯示模式已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**IUnknown** \*) 指標指向影片轉譯器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面陣列。 如果 *lParam2* 為零，則此參數可以是 **Null**。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

如果 *lParam2* 為零，則 *LParam1* 包含單一 **IPin** 指標或等於 **Null**。 如果 *lParam2* 大於零， *lParam1* 就會包含 **IPin** 指標的陣列，而陣列中的元素數目則由 *lParam2* 指定。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選圖形管理員會暫時停止圖形，然後中斷連接並重新連接影片轉譯器。 它不會將事件傳遞至應用程式。

## <a name="remarks"></a>備註

影片轉譯器可以傳送此事件以回應 [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息。 **WM \_ DISPLAYCHANGE** 訊息表示使用者已變更顯示器解析度。

在 pin 連接期間，大部分的影片轉譯器會根據目前的顯示模式來挑選格式。 如果顯示模式變更，影片轉譯器可能需要選擇另一種格式。 藉由傳送此訊息，轉譯器會向篩選圖形管理員發出需要重新連接的信號。 在重新連接期間，轉譯器可以選取新的格式。 如果重新連接失敗，則篩選圖形管理員會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至應用程式。

### <a name="enhanced-video-renderer"></a>增強的影片轉譯器

[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的自訂展示者 (EVR) 應該會將此事件傳送到 EVR，如果顯示者的 Direct3D 裝置有變更。 將 *lParam1* 和 *lParam2* 設定為零;EVR 會忽略事件參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

