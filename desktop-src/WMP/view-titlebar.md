---
title: VIEW. 標題列
description: 標題列屬性會抓取值，指出是否顯示視窗標題列。
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. 標題列 Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb05550c22c342d14690f24f42c62a3af328eae65201b8138e82a7a33bf99fb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054066"
---
# <a name="viewtitlebar"></a>VIEW. 標題列

**標題** 欄屬性會抓取值，指出是否顯示視窗標題列。

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。



| 值 | 描述                             |
|-------|-----------------------------------------|
| true  | 預設值。 視窗標題列會顯示。 |
| false | 不會顯示視窗標題列。      |



 

## <a name="remarks"></a>備註

如果顯示標題列，則會顯示 [控制台]、[最小化] 和 [關閉] 按鈕。 視窗的標題將會是 **VIEW** 元素的標題。

如果 [ **標題** ] 設定為 [true]，而使用者嘗試變更 [ **視頻**] 的值，則不會進行變更，除非面板監視 **縮放比例** 並採取適當的動作來調整其本身的大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**VIEW. 標題**](view-title.md)
</dt> <dt>

[**影片。縮放**](video-zoom.md)
</dt> </dl>

 

 





