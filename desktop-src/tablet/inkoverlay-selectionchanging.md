---
description: 發生于控制項內的筆墨選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或選取屬性）。
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: 'SelectionChanging 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975442"
---
# <a name="inkoverlayselectionchanging-event"></a>SelectionChanging 事件

發生于控制項內的筆墨選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。

## <a name="syntax"></a>語法


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewSelection* \[在\]
</dt> <dd>

要選取的新 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionChanging 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> <dt>

[**Selection 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

