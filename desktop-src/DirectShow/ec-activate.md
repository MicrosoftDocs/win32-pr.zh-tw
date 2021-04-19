---
description: 正在啟用或停用影片視窗。
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: 'EC_ACTI加值稅E (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977735"
---
# <a name="ec_activate"></a>EC \_ 啟用

正在啟用或停用影片視窗。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

如果視窗已啟用，則 (**BOOL**) **TRUE** ; 如果停用視窗，則為 **FALSE** 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**IUnknown** \*) 轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選圖形管理員會透過 [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) 介面設定焦點。 它不會將事件通知傳送至應用程式。

## <a name="remarks"></a>備註

影片轉譯器會在每次啟動或停用其視窗時傳送此事件 (也就是在收到 WM \_ ACTI加值稅EAPP 訊息) 時。 視窗啟用或停用可能發生，因為視窗已取得或遺失焦點，或轉譯器在全螢幕模式與視窗模式之間切換。

此事件可讓篩選圖形管理員配置相依于視窗焦點的資源，例如音訊裝置。

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

 

 




