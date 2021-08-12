---
description: InkPicture. CursorButtonUp 事件-當 InkCollector 偵測到已啟動的資料指標按鈕時，就會發生此事件。
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: 'InkPicture. CursorButtonUp 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a84a5d8529ecf6387d3832608ae3821be9d317fef46211a6824bddc2ee9574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451077"
---
# <a name="inkpicturecursorbuttonup-event"></a>InkPicture. CursorButtonUp 事件

當 [**InkCollector**](inkcollector-class.md) 偵測到已啟動的資料指標按鈕時發生。

## <a name="syntax"></a>語法


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **CursorButtonUp** 事件的 [**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*按鈕* \[在\]
</dt> <dd>

已發行的按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當使用者完成筆觸並將畫筆從數位板中提起時，畫筆提示上的按鈕就會啟動。 當未按下按鈕時，會開啟張圓柱上的按鈕。

當您放開滑鼠右鍵時，您實際上會收到兩個 **CursorButtonUp** 事件：一個用於右按鈕，另一個用於左按鈕。

此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 的分配介面中定義，並具有 DISPID \_ ICECursorButtonUp 的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**CursorButtonDown 事件**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**CursorDown 事件**](inkpicture-cursordown.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




