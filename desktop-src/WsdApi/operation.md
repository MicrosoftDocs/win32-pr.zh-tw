---
description: 指定要產生程式碼的作業。
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994314"
---
# <a name="operation-element"></a>operation 元素

指定要產生程式碼的作業。

## <a name="usage"></a>使用方式

``` syntax
<operation/>
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

您可以指定任意數目的作業。 如果未指定任何作業，則會針對所有相關埠類型中的所有作業產生程式碼。 使用 **operation** 元素會將產生的方法限制為包含在作業中的方法。

例如，印表機支援這些作業的其他作業：

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

不過，若要只包含與 **PrintJobByPost** 和 **GetJobElements** 作業相關的方法，程式碼產生腳本會使用 [**idlFunctionDeclarations**](idlfunctiondeclarations.md) 元素，如下所示：

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

這會針對與這兩個作業相關聯的所有方法產生 idl 函式宣告 (例如， **BeginPrintJobByPost**、 **EndPrintJobByPost**、 **BeginGetJobElements** 和 **EndGetJobElements**) 。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




