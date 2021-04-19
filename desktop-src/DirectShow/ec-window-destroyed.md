---
description: 影片轉譯器已從圖形終結或移除。
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: 'EC_WINDOW_DESTROYED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992557"
---
# <a name="ec_window_destroyed"></a>EC \_ 視窗已 \_ 損毀

影片轉譯器已從圖形終結或移除。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**IUnknown** \*) 指標指向影片轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選圖形管理員會透過 [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) 介面，將此視窗以焦點的形式釋放。 它不會將事件通知傳送至應用程式。

## <a name="remarks"></a>備註

影片轉譯器會在其 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法中離開篩選圖形時傳送此事件。 當篩選損毀時 (傳送事件可能太晚，因為篩選圖形管理員可能也會終結。 ) 

此事件可讓其他篩選器取得相依于視窗焦點的資源，例如音訊裝置。

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

 

 




