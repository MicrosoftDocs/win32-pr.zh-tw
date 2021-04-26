---
description: 定義服務主機的 ServiceID 和 Types 元素。
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: host 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993795"
---
# <a name="host-element"></a>host 元素

定義服務主機的 [**ServiceID**](serviceid.md) 和 [**Types**](types.md) 元素。

## <a name="usage"></a>使用方式

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | 定義服務主機的服務識別碼。<br/> <br/> |
| [**類型**](types.md)<br/>         | 定義 XSD 限定名稱的清單。<br/> <br/>               |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>父元素



| 元素                                         | 描述                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | 要執行之裝置的裝載中繼資料。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




