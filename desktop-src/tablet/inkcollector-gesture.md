---
description: 在識別應用程式特定的手勢時發生。
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: 'InkCollector 的軌跡事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb68add1a3fbba5781624f1df98c3a637745b95a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972206"
---
# <a name="inkcollectorgesture-event"></a>InkCollector 手勢事件

在識別應用程式特定的手勢時發生。

## <a name="syntax"></a>語法


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **手勢** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*筆觸* \[在\]
</dt> <dd>

辨識器傳回做為手勢的 [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。

</dd> <dt>

*手勢* \[在\]
</dt> <dd>

從辨識器 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) 物件的陣列，以信賴度為限。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

**變異 \_** 如果應該取消此手勢，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICEGesture 識別碼的) \_ 。

當 [ [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) ] 屬性設定為 [ [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)] 時，當使用者加入手勢以及 **手勢** 事件發生的時間，是您無法以程式設計方式改變的固定值。 在 **InkAndGesture** 模式中，手勢辨識的速度較快。

若要在 [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) 模式中防止筆墨收集：

-   將 [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) 設定為 [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)。
-   刪除 [**筆劃**](inkcollector-stroke.md) 事件中的筆劃。
-   處理 **手勢** 事件中的手勢。

若要在 gesturing 時防止筆墨流程，請將 [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) 屬性設定為 **FALSE**。

除了插入筆墨時，會在選取或清除模式時引發 **手勢** 事件。 您必須負責追蹤編輯模式，並且應該在解讀事件之前留意模式。

> [!Note]  
> 若要辨識筆勢，您必須使用可收集筆跡的物件或控制項。

 

應用程式手勢會定義為您的應用程式中支援的手勢。

若要進行此事件，物件或控制項必須對一組應用程式手勢感興趣。 若要設定一組手勢中感興趣的物件或控制項，請呼叫物件或控制項的 [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) 方法。

如需特定應用程式手勢的清單，請參閱 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉型別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkCollector 類別**](inkcollector-class.md)
</dt> <dt>

[**InkApplicationGesture 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[使用手勢](using-gestures.md)
</dt> </dl>

 

