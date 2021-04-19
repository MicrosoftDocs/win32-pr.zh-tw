---
description: 發生于控制項內的筆墨選取變更時（例如，透過對使用者介面的變化、剪下和貼上程式或選取屬性）。
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: 'SelectionChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980666"
---
# <a name="inkoverlayselectionchanged-event"></a>SelectionChanged 事件

發生于控制項內的筆墨選取變更時（例如，透過對使用者介面的變化、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。

## <a name="syntax"></a>語法


```C++
void SelectionChanged();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

沒有任何事件資料。

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionChanged 識別碼的) \_ 。

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

 

 




