---
description: 指定要產生程式碼的埠類型。
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: portType 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7fc502b2d899998a7f3e0f199c7804856317744ec8d127fb712a3f98c3bd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991648"
---
# <a name="porttype-element"></a>portType 元素

指定要產生程式碼的埠類型。

## <a name="usage"></a>使用方式

``` syntax
<portType/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                                 | 描述                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | 針對埠類型作業產生 proxy 函式的實作為宣告。<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | 針對埠類型作業產生 proxy 函式的 IDL 宣告。<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | 產生訊息類型的 C 結構定義。<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | 針對訊息類型產生 XML 架構資料表的 C 常數宣告。<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | 針對訊息類型產生 XML 架構資料表的 C 常數。<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | 產生埠類型的 C 常數宣告。<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | 產生埠類型的 C 常數。<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | 針對埠類型作業產生 proxy 函式的執行。<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | 針對埠類型作業產生存根函式的宣告。<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | 針對埠類型作業產生存根函式的實作為。<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。<br/> <br/>             |



## <a name="remarks"></a>備註

依預設，會針對 WSDL 輸入檔中的所有埠類型產生程式碼。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




