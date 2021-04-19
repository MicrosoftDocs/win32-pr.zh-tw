---
title: HTMLView 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 HTMLView 元素會指定 HTMLView 網頁的基底 URL。
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- HTMLView 元素 Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989596"
---
# <a name="htmlview-element"></a>HTMLView 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**HTMLView** 元素會指定 HTMLView 網頁的基底 URL。

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (必要) 
</dt> <dd>

Windows Media Player 顯示之 HTMLView 網頁的基底 URL。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

您可以使用此元素，將 HTMLView 功能與您的線上商店整合。 如果目前線上商店所指定的 URL 網域與 HTMLView 網頁的網域相符，就會在沒有使用者介入的情況下， **立即播放** 的參數，並顯示 HTMLView 內容。 否則，Windows Media Player 會提示使用者顯示 HTMLView 內容的許可權。

例如，如果 HTMLView 網頁的 URL 為 https://www.proseware.com/html/HTMLView.htm ，而且 **BaseURL** 屬性的 url 指定為 https://www.proseware.com ，則會顯示 HTMLView 網頁，而不會提示使用者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**PARAM 元素**](param-element.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





