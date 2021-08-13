---
description: 從筆墨屬性刪除 IInkStrokeDisp 物件之後發生。
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: 'InkPicture. StrokesDeleted 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b2d4f0be69adf6c9c44f3eadec250d8cba3ebb8935bde5c06cd026e478da3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717357"
---
# <a name="inkpicturestrokesdeleted-event"></a>InkPicture. StrokesDeleted 事件

從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之後發生。

## <a name="syntax"></a>語法


```C++
void StrokesDeleted();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

沒有任何事件資料。

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEStrokesDeleted 識別碼的) \_ 。

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
</dt> </dl>

 

 




