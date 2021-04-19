---
description: 圖形正在緩衝處理資料，或已停止緩衝資料。
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: 'EC_BUFFERING_DATA (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994306"
---
# <a name="ec_buffering_data"></a>EC \_ 緩衝 \_ 資料

圖形正在緩衝處理資料，或已停止緩衝資料。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

如果圖形正在開始緩衝區， (**BOOL**) **TRUE** ; 如果圖形已停止緩衝，則為 **FALSE** 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

如果篩選準則需要從外部來源緩衝資料，則可以傳送此事件。  (例如，可能是從網路載入資料。 ) 應用程式可以使用此事件來調整其使用者介面。

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

 

 




