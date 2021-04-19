---
description: InkPicture 控制項內的筆墨選取範圍變更時發生，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: 'InkPicture. SelectionChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975907"
---
# <a name="inkpictureselectionchanged-event"></a>InkPicture. SelectionChanged 事件

[InkPicture](inkpicture-control-reference.md)控制項內的筆墨選取範圍變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)屬性。

## <a name="syntax"></a>語法


```C++
void SelectionChanged();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

如需此事件的進一步詳細資料，請參閱 [**InkOverlay**](inkoverlay-class.md) 物件的 [**SelectionChanged**](inkoverlay-selectionchanged.md) 事件，該事件具有相同的功能。

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

[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

 




