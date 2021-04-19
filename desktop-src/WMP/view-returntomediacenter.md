---
title: ReturnToMediaCenter
description: ReturnToMediaCenter 方法會將使用者返回 Windows Media Player 的完整模式。
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- ReturnToMediaCenter Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977756"
---
# <a name="viewreturntomediacenter"></a>ReturnToMediaCenter

**ReturnToMediaCenter** 方法會將使用者返回 Windows Media Player 的完整模式。

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> </dl>

 

 





