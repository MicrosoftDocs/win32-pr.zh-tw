---
title: ButtonTip 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |ButtonTip 元素
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- ButtonTip 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764298"
---
# <a name="buttontip-element"></a>ButtonTip 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ButtonTip** 元素會指定當使用者指向工作窗格按鈕時所顯示的文字字串。

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                              |
|-----------------|------------------------------------------------------|
| 父元素 | **ServiceTask1**、 **ServiceTask2**、 **ServiceTask3** |
| 子元素  | 無                                                 |



 

## <a name="remarks"></a>備註

針對 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 的每個實例，這個元素是選擇性的。 如果未提供此元素，Windows Media Player 會使用按鈕文字作為預設值。

> [!Note]  
> Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。 線上商店可以選擇使用一個、兩個或三個工作窗格。 Windows Media Player 11 只有一個工作窗格，使用者可以按一下 [**線上商店**] 索引標籤來查看。 Windows Media Player 11 會忽略 **ServiceTask2** 和 **ServiceTask3** 元素。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





