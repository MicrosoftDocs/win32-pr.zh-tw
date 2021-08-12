---
title: 資訊中心元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |資訊中心元素
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- 資訊中心元素 Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1d89e7a35d0d9daacd87d3ac840f0ee87fa7c82b317afd54c9283344e204f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576257"
---
# <a name="infocenter-element"></a>資訊中心元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**資訊中心** 元素會指定網頁的 URL，Windows Media Player 在線上商店為使用中時，于 **現在播放** 的資訊中心視圖功能中顯示。

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) 
</dt> <dd>

Windows Media Player 顯示之網頁的 URL。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

使用者控制資訊中心視圖的作用中。

若要取得目前播放之媒體專案的相關資訊，您必須在網頁中內嵌 Windows Media Player 控制項的實例，並使用 Player 物件模型。

下表詳細說明以 URL 要求傳送的參數。 其他可能存在於舊版相容性的用途。



| 名稱         | 值                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *大地 水準面*      | Windows 的地理位置識別碼。 在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。 |
| *locale*     | Windows Media Player 地區設定識別碼。                                                                                                                                     |
| *userlocale* | Windows 地區設定識別碼。 地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。        |
| *version*    | 使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。                                                                         |



 

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

 

 





