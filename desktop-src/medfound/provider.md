---
description: 針對 MFTrace 指定追蹤提供者 (ETW 或 WPP) 。
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider 項目
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118443"
---
# <a name="provider-element"></a>provider 項目

針對 [MFTrace](mftrace.md)指定追蹤提供者 (ETW 或 WPP) 。

## <a name="usage"></a>使用方式

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>屬性



| 屬性            | 類型             | 必要       | 描述                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **識別碼**<br/>    | CDATA<br/> | 是<br/> | 提供者的名稱或 GUID。<br/> <br/> |
| **level**<br/> | CDATA<br/> | 是<br/> | 追蹤層級。<br/> <br/>                  |



## <a name="child-elements"></a>子元素



| 元素                               |
|---------------------------------------|
| [**關鍵 字**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
keyword+
```

## <a name="parent-elements"></a>父元素



| 元素                                   |
|-------------------------------------------|
| [**供應商**](providers.md)<br/> |



## <a name="element-information"></a>項目資訊

:::row:::
    :::column:::
        可以是空的
    :::column-end:::
    :::column span="2":::
        否
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MFTrace 設定檔](mftrace-configuration-file.md)
</dt> </dl>

 

 




