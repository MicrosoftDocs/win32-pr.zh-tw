---
description: 發生于 InkEdit 控制項中目前的文字選取範圍已變更或插入點移動時。
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: 'InkEdit. SelChange 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712648"
---
# <a name="inkeditselchange-event"></a>InkEdit. SelChange 事件

發生于 [InkEdit](inkedit-control-reference.md) 控制項中目前的文字選取範圍已變更或插入點移動時。

## <a name="syntax"></a>語法


```C++
void SelChange();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

您可以使用 **SelChange** 事件來檢查提供目前選取專案相關資訊的各種屬性 (例如 [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) ，以便您可以在工具列中更新按鈕，例如。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>筆跡 (也需要筆跡 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




