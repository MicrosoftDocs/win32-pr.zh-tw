---
title: 'OnColorChange 事件 (類型 1) '
description: '請注意，本主題將說明針對線上商店使用而設計的功能。 |OnColorChange 事件 (類型 1) '
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- OnColorChange 事件 (類型 1) Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b50f23763827965c80c3c2774f6139ba2345e4e50633966d5debc1f2d4b782e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648778"
---
# <a name="externaloncolorchange-event-type-1"></a>OnColorChange 事件 (類型 1) 

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當 Windows Media Player 使用者介面的色彩變更時，就會發生 **OnColorChange** 事件。

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此事件的函式不會使用任何參數。

## <a name="remarks"></a>備註

使用者可以變更 Windows Media Player 使用者介面的色彩。 您可以使用此事件來自訂您的託管網頁外觀，以符合播放程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





