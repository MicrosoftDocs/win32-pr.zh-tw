---
description: 指示程式碼產生器產生檔案並指定輸出檔名稱。
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc20f7d6853ccd52b231e19c99d60fe4b71d15b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969305"
---
# <a name="file-element"></a>file 項目

指示程式碼產生器產生檔案並指定輸出檔名稱。

## <a name="usage"></a>使用方式

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>屬性



| 屬性           | 類型                       | 必要       | 描述                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | pathname 字串<br/> | Yes<br/> | 產生之內容的輸出檔案名。 檔案名字串應該包含完整的路徑資訊。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                 | 描述                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cdata**<br/>                                                                                    | 在不修改的情況下，會將 Text 和 CDATA 區段複製到檔案。 您可以使用 text 和 CDATA 區段，將不是合約輸入資料功能的原始程式碼新增至輸出檔案。<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | 針對所有列舉類型的值產生 C 宣告。<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | 針對建立事件來源類別的函式產生宣告。<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | 產生建立事件來源類別的函式。<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | 針對埠類型作業產生 proxy 函式的實作為宣告。<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | 產生函式的宣告，這個函式會建立具類型的主控制項。<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | 產生可建立具型別主機的函式。<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | 針對埠類型作業產生 proxy 函式的 IDL 宣告。<br/> <br/>                                                                                                                       |
| [**包括**](include.md)<br/>                                                                   | 在產生的輸出中包含宏或檔案的內容。<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | 產生 QueryInterface、AddRef 和 Release 的宣告。<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | 產生 QueryInterface、AddRef 和 Release 的實作為。<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | 將 C 或 IDL include 語句放在產生的程式碼中。 <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | 產生訊息類型的 C 結構定義。<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | 針對訊息類型產生 XML 架構資料表的 C 常數宣告。<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | 針對訊息類型產生 XML 架構資料表的 C 常數。<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | 為命名空間資料表產生 C 宣告。<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | 產生命名空間資料表的 C 定義。<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | 產生埠類型的 C 常數宣告。<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | 產生埠類型的 C 常數。<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | 產生函數的宣告，以建立具類型的 proxy。<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | 產生函數以建立具類型的 proxy。<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | 針對埠類型作業產生 proxy 函式的執行。<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | 針對 [**hostMetadata**](hostmetadata.md) 元素中指定的裝載中繼資料產生向前宣告。 <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | 針對 [**hostMetadata**](hostmetadata.md) 元素中指定的裝載中繼資料產生 C 常數定義。 <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | 產生已知類型的 C 結構宣告。<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | 產生已知類型的 C 結構定義。<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | 針對埠類型作業產生存根函式的宣告。<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | 針對埠類型作業產生存根函式的實作為。<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | 在不修改的情況下，會將 Text 和 CDATA 區段複製到檔案。 您可以使用 text 和 CDATA 區段，將不是合約輸入資料功能的原始程式碼新增至輸出檔案。<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | 針對 [**thisModelMetadata**](thismodelmetadata.md) 元素中指定的製造商中繼資料，產生 C 常數的向前宣告。<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | 針對 [**thisModelMetadata**](thismodelmetadata.md) 元素中指定的製造商中繼資料產生 C 常數。<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | 針對已知類型產生 XML 架構資料表的 C 常數宣告。<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | 針對已知類型產生 XML 架構資料表的 C 常數。<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

檔案的名稱是由 name 屬性的值或子項目所決定。 檔案的內容是由 **file** 元素中的其他子項目、TEXT 和 CDATA 所決定。 Text 和 CDATA 會複製到未修改的檔案。 已產生的程式碼會取代子項目。 Text、CDATA 和子項目可能會以任何順序發生，而且可能會無限期地重複。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




