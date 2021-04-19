---
description: 指定最新框架步驟的時間戳記。
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: 'EC_SCRUB_TIME (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985571"
---
# <a name="ec_scrub_time"></a>EC \_ 清理 \_ 時間

指定最新框架步驟的時間戳記。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

時間戳記的 (**DWORD**) 較低的32位。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

時間戳記的 (**DWORD**) 最高32位。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的簡報者 (EVR) 篩選器會在完成框架步驟時，將此訊息傳送至 EVR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> </dl>

 

 




