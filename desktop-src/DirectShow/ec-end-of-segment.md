---
description: 到達區段的結尾。
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: 'EC_END_OF_SEGMENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bbc55ab316a56264c9c0b66196a53181d0abd72bfdddf3315523b8c387a1d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639748"
---
# <a name="ec_end_of_segment"></a>EC \_ 結尾 \_ 的 \_ 區段

到達區段的結尾。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**常數****參考 \_ 時間** \*) **參考 \_ 時間** 值的指標，此值會指定自區段開始以來累積的資料流程時間，以 100-毫微秒單位表示。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**DWORD**) 區段號碼 (以零為基礎的) 。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選圖形管理員會根據 [**ec \_ 區段 \_ 開始**](ec-segment-started.md)事件的數目，來檢查 **\_ \_ \_ 區段事件的 EC 結束** 次數。 如果兩者相符，就會將 [ **EC] \_ \_ \_ 區段** 事件轉送到應用程式。 應用程式無法覆寫此事件的預設動作。

## <a name="remarks"></a>備註

此事件程式碼支援無縫迴圈。 當呼叫 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法包含 AM \_ 搜尋區段旗標時 \_ ，來源篩選會傳送此事件程式碼，而不是呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)。

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

 

 




