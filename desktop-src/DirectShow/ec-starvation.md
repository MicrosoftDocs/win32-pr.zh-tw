---
description: 篩選未收到足夠的資料。
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: 'EC_STAR加值稅ION (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998697"
---
# <a name="ec_starvation"></a>EC \_ 耗盡

篩選未收到足夠的資料。

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

此事件不會傳送至應用程式。 如果篩選圖形正在執行，則篩選圖形管理員會暫停圖形，並等候暫停完成。 然後，它會再次執行圖形。 傳送事件的篩選不應完成其轉換為暫停，直到它有足夠的資料可繼續為止。 如果篩選圖形未執行，則篩選圖形管理員會忽略此事件。

## <a name="remarks"></a>備註

如果資料太少，剖析器或來源篩選器可以傳送此事件。

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

 

 




