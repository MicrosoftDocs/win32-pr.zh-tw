---
title: PLAYERAPPLICATION. hasDisplay 屬性
description: hasDisplay 屬性會抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項來顯示。
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571941"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

**hasDisplay** 屬性會抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項來顯示。

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。



| 值 | 描述               |
|-------|---------------------------|
| True  | 影片可以顯示。    |
| 否 | 影片無法顯示。 |



 

## <a name="remarks"></a>備註

只有在遠端 Windows Media Player 控制項時，才會使用這個屬性。

您可以同時在遠端執行數個 Windows Media Player 控制項，但影片在播放程式的完整模式或其中一個遠端控制項中，一次只能顯示在一個位置。 您可以使用這個屬性來判斷目前的控制項是否為可顯示影片的控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PLAYERAPPLICATION 元素**](playerapplication-element.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





