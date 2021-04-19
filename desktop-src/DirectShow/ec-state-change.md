---
description: 篩選圖形的狀態已變更。
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: 'EC_STATE_CHANGE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989789"
---
# <a name="ec_state_change"></a>EC \_ 狀態 \_ 變更

篩選圖形的狀態已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**DWORD**) [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，表示新的圖形狀態。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

沒有預設動作。 此事件不會傳送至應用程式。

> [!Note]  
> 當圖形關閉時，就會發生此事件。 如果您覆寫預設動作並接聽此事件，您必須特別小心，不要在釋出篩選圖形管理員之後處理事件。 否則，您的應用程式可能會參考不正確 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 指標和損毀。 如需詳細資訊，請參閱 [回應事件](responding-to-events.md)。

 

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

 

 




