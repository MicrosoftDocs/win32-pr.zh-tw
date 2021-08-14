---
description: EC \_ CODECAPI \_ 事件事件是由編碼器傳送以表示編碼事件。 用戶端會藉由呼叫 ICodecAPI：： RegisterForEvent 方法來註冊編碼器事件。
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: 'EC_CODECAPI_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965938"
---
# <a name="ec_codecapi_event"></a>EC \_ CODECAPI \_ 活動

EC \_ CODECAPI \_ 事件事件是由編碼器傳送以表示編碼事件。 用戶端會藉由呼叫 [**ICodecAPI：： RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) 方法來註冊編碼器事件。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

使用者資料。 此參數的值是呼叫端在 [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)方法的 *userData* 參數中指定的指標。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

事件資料的指標。 這項資料是由編碼器所配置，且必須由應用程式使用 **CoTaskMemFree** 函式來釋放。 資料區塊會以 [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) 結構開始;將 *lParam2* 參數轉換為此結構的指標。

</dd> </dl>

## <a name="default-action"></a>預設動作

沒有預設動作。

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

 

 




