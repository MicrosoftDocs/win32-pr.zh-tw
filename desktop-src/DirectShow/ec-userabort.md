---
description: 使用者已結束播放。
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: 'EC_USERABORT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995310"
---
# <a name="ec_userabort"></a>EC \_ USERABORT

使用者已結束播放。

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

無。 應用程式必須決定是否要停止圖形。

## <a name="remarks"></a>備註

此事件程式碼表示使用者已結束正常的圖形播放。 例如，如果使用者關閉影片視窗，影片轉譯器就會傳送此事件。

傳送此事件之後，篩選準則應該會拒絕所有範例，而不會傳送任何 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件，直到篩選停止並重設為止。

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

 

 




