---
description: 表示元件花費在處理每個樣本的時間量。
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: 'EC_PROCESSING_LATENCY (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999074"
---
# <a name="ec_processing_latency"></a>EC \_ 處理 \_ 延遲

表示元件花費在處理每個樣本的時間量。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**CONST 參考 \_ 時間** \*) 處理每個樣本的時間量，以 100-毫微秒單位表示。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的簡報者 (EVR) 篩選器可以將此訊息傳送至 EVR，以通知 EVR 有關展示者的處理延遲。

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

 

 




