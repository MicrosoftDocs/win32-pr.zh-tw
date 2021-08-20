---
title: CurrentViewID
description: CurrentViewID 屬性會指定或抓取目前顯示的視圖。
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- CurrentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21bf3027b0249286689862e53fc2d616d1d33b19eca562c886e981bffb7f0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117809"
---
# <a name="themecurrentviewid"></a>CurrentViewID

**CurrentViewID** 屬性會指定或抓取目前顯示的 **視圖**。

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀取/寫入 **字串**，可指定目前 **視圖** 的 **識別碼**。 它沒有預設值。

## <a name="remarks"></a>備註

指定 **currentViewID** 會自動關閉 **view** global 屬性所指向的現有 **currentView** () 並開啟指定的 **視圖**。

## <a name="examples"></a>範例


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> </dl>

 

 





