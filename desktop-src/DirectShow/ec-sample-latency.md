---
description: 指定元件排程處理範例的進度。
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: 'EC_SAMPLE_LATENCY (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686148"
---
# <a name="ec_sample_latency"></a>EC \_ 範例 \_ 延遲

指定元件排程處理範例的進度。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**CONST 參考 \_ 時間** \*) 元件背後的距離，以 100-毫微秒單位表示。 如果這個值是正數，則元件會落後排程。 如果這個值是負數，則元件會預先排程。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的自訂展示者 (EVR) 篩選器可以將此訊息傳送至 EVR，以通知 EVR 簡報者是在排程或預先排程的後方。

計算 *lParam1* 的最簡單方式是：立即 *QPC*   *QPC 目標*，其中 *QPC 現在* 是目前的時鐘時間，而 *QPC 目標* 是展示時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[如何撰寫 EVR 展示者](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

