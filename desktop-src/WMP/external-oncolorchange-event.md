---
title: OnColorChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnColorChange 事件
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- External. OnColorChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae4ca15d4d7035fc342fa20263220560570d902e28b9245a6458ac59c40a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648748"
---
# <a name="externaloncolorchange-event"></a>OnColorChange 事件

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

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





