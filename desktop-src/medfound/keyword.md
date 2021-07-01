---
description: 指定 MFTrace 提供者的關鍵字字。
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: 關鍵字元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119373"
---
# <a name="keyword-element"></a>關鍵字元素

指定 [MFTrace](mftrace.md) 提供者的關鍵字字。

## <a name="usage"></a>使用方式

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>屬性



| 屬性         | 類型             | 必要       | 描述                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **識別碼**<br/> | CDATA<br/> | 是<br/> | 關鍵字組的名稱或遮罩<br/> <br/> |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素

| 元素                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**供應商**](provider.md)<br/>   |



## <a name="remarks"></a>備註

針對 [**mfdetours**](mfdetours.md) 元素，有效的關鍵字會列在主題 [MFTrace 關鍵字](mftrace-keywords.md)中。

針對 [**提供者**](provider.md) 專案，關鍵字組相依于事件提供者。 您可以使用 Wevtutil.exe 公用程式來列出指定提供者的關鍵字。

## <a name="element-information"></a>項目資訊

:::row:::
    :::column:::
        可以是空的
    :::column-end:::
    :::column span="2":::
        是
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MFTrace 設定檔](mftrace-configuration-file.md)
</dt> <dt>

[MFTrace 關鍵字](mftrace-keywords.md)
</dt> </dl>

 

 




