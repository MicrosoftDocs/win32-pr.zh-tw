---
description: 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: subscriptionIdlFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851487"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>subscriptionIdlFunctionDeclarations 元素

針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。

## <a name="usage"></a>使用方式

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
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



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




