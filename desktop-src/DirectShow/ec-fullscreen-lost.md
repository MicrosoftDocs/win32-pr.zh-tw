---
description: 影片轉譯器正在切換至全螢幕模式。
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: 'EC_FULLSCREEN_LOST (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994724"
---
# <a name="ec_fullscreen_lost"></a>EC \_ 全螢幕 \_ 遺失

影片轉譯器正在切換至全螢幕模式。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

零個。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**IUnknown**) 指向影片轉譯器之 \* [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面的指標，或 **為 Null**。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

當 [全螢幕](full-screen-renderer-filter.md) 轉譯器失去啟用時，它會傳送此事件。 當另一個影片轉譯器切換至全螢幕模式時，篩選圖形管理員會傳送此事件，以回應轉譯器的 [**EC \_ 啟動**](ec-activate.md) 事件。

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

 

 




