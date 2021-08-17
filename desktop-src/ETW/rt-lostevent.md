---
description: 此事件種類類別用來指出在即時會話中遺失事件。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328738"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent 類別

此事件種類類別用來指出在即時會話中遺失事件。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>成員

**RT \_ LostEvent** 類別未定義任何成員。

## <a name="remarks"></a>備註

RTLostEvent 事件種類指出有一或多個事件遺失。 RTLostBuffer 事件種類指出有一或多個緩衝區遺失。 RTLostEvent 和 RTLostBuffer 事件種類會在處理緩衝區中的事件之前傳遞。

RTLostFile 表示自動記錄器用來捕捉事件的支援檔案已遺失。

遺失事件取決於記錄事件的頻率，以及取用者花費多少時間來處理事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**遺失的 \_ 事件**](lost-event.md)
</dt> </dl>

 

 




