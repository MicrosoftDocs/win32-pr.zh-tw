---
description: 篩選器要求重新開機圖形。
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: 'EC_NEED_RESTART (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae3426048229c19b1d35a061d67d3d1d0a3149a8f820e891987c88405b76f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820140"
---
# <a name="ec_need_restart"></a>EC \_ 需要 \_ 重新開機

篩選器要求重新開機圖形。

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

篩選圖形管理員會暫停並重新啟動圖形。 它不會將事件傳遞至應用程式。

## <a name="remarks"></a>備註

如果篩選準則拒絕了串流中間的範例，上游釘選將會停止傳遞範例。 篩選可以藉由傳送此事件來重新開機資料流程。 例如，音訊轉譯器可能會遺失聲音裝置的存取權，因為影片視窗已遺失焦點。 屆時，音訊轉譯器會開始拒絕範例。 當它重新取得音效裝置的存取權時，會傳送此事件以重新開機音訊串流。

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

 

 




