---
description: 篩選圖形正在進行終結之前，正在關閉。
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: 'EC_SHUTTING_DOWN (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917a8f79b1a5201e50d0fcf2761a99b2801f75601f95ef866902492fb36065f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079108"
---
# <a name="ec_shutting_down"></a>EC \_ 關機 \_

篩選圖形正在進行終結之前，正在關閉。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

零個。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

此事件不會傳送至應用程式。 篩選圖形管理員會將它傳送至外掛程式散發者，以通知圖形正在關閉。 應用程式無法覆寫此事件的預設動作。

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

 

 




