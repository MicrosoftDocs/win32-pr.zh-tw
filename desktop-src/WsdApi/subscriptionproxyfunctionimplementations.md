---
description: 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995315"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>subscriptionProxyFunctionImplementations 元素

針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。

## <a name="usage"></a>使用方式

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a>屬性



| 屬性                 | 類型               | 必要      | 描述                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **擴展**<br/> | boolean<br/> | No<br/> | 將擴充功能新增至函式和介面的能力。 此值一律設定為 true。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                                                           | 描述                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | 指定與事件訂閱搭配使用之通知介面的名稱。<br/> <br/> |
| [**操作**](operation.md)<br/>                         | 指定要產生程式碼的作業。<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | 指定要產生程式碼的埠類型。<br/> <br/>                      |
| [**proxyClass**](proxyclass.md)<br/>                       | 指定用戶端 proxy 類別的名稱。<br/> <br/>                              |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




