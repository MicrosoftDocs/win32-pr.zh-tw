---
title: Description 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |Description 元素
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Description 元素 Windows Media Player
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78c3601abaf2a039b49318772eba1ed6e95d2aed06e2a91c72aabdadc3ffebd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579598"
---
# <a name="description-element"></a>Description 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Description** 元素會指定線上商店的行銷描述，該描述會在使用者第一次安裝 Windows Media Player 的體驗期間顯示。

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

描述的長度必須小於或等於255個字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





