---
description: InkCollector. CursorOutOfRange 事件-當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時，就會發生此事件。
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: 'InkCollector. CursorOutOfRange 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42963c06f7b2700056b06b20c1e38815714e384a67a6dae95e75d4bf553ae953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883968"
---
# <a name="inkcollectorcursoroutofrange-event"></a>InkCollector. CursorOutOfRange 事件

當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。

## <a name="syntax"></a>語法


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **CursorOutOfRange** 事件的 [**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICECursorOutOfRange 識別碼的) \_ 。

即使在 [選取] 或 [清除] 模式中，也不只是在 [筆墨] 模式中，也會引發 **CursorOutOfRange** 事件。 這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。 這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkCollector 類別**](inkcollector-class.md)
</dt> <dt>

[**CursorInRange 事件**](inkcollector-cursorinrange.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




