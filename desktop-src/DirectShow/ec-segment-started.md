---
description: 已開始新的區段。
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: 'EC_SEGMENT_STARTED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015916"
---
# <a name="ec_segment_started"></a>\_ \_ 已開始 EC 區段

已開始新的區段。

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

此事件不會傳送至應用程式。 應用程式無法覆寫此事件的預設動作。

## <a name="remarks"></a>備註

如果篩選準則會在區段結尾傳送 [**EC \_ 結尾 \_ 的 \_ 區段**](ec-end-of-segment.md) ，則會在區段的開頭傳送此事件。 篩選圖形管理員會使用此事件通知來計算在 \_ \_ \_ 區段結束時應預期的 EC 區段通知數目。

根據預設，篩選不會在區段結尾傳送 $ [**\_ end \_ 的 \_ 區段**](ec-end-of-segment.md) 事件，因此不應該傳送此事件。 如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)。

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

 

 




