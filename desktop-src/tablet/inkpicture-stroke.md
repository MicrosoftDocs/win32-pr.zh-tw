---
description: InkPicture。當使用者在任何平板電腦上繪製新的筆劃時，就會發生筆觸事件。
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: 'InkPicture： Stroke 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b181c8dc46348c76bd9c2d015d4a97c1f6911ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113696"
---
# <a name="inkpicturestroke-event"></a>InkPicture。筆觸事件

當使用者在任何平板電腦上繪製新筆劃時發生。

## <a name="syntax"></a>語法


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **筆劃** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*筆觸* \[在\]
</dt> <dd>

收集的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

**變異 \_TRUE** 表示取消筆劃的集合;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICEStroke 識別碼的) \_ 。

在選取或清除模式中（而不只是在插入筆墨時），就會發生 **筆劃** 事件。 這需要您監視您負責設定) 的編輯模式 (，並在解讀事件之前感知模式。 這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。

> [!Note]  
> 當使用者完成繪製筆劃時，不會在將筆劃加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合時，就會發生 **筆劃** 事件。 當使用者第一次開始繪製筆劃時，會立即將其新增至 InkStrokes 集合;不過，在筆劃完成之前，不會發生 **筆劃** 事件。 因此，筆劃可以存在於 **筆劃** 事件處理常式未看到的 InkStrokes 集合中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**StrokesAdded 事件 \[ InkPicture 控制項\]**](inkpicture-strokesadded.md)
</dt> <dt>

[**StrokesDeleted 事件 \[ InkPicture 控制項\]**](inkpicture-strokesdeleted.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

