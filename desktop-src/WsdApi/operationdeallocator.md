---
description: 指定作業存根函式所要使用的類型釋放器。
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994285"
---
# <a name="operationdeallocator-element"></a>operationDeallocator 元素

指定作業的存根函數所要使用的類型釋放器。

## <a name="usage"></a>使用方式

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>屬性



| 屬性                  | 類型                         | 必要       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **釋放器**<br/> | 字元 \_ 字串<br/> | Yes<br/> | 要用於作業的釋放器。<br/> <br/> 下列字串是有效的值。<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>* * * * 無 *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * *<dt>* * * * WSDFreeLinkedMemory *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * *<dt>* * * * CoTaskMemFree *</dt> <span id="free"></span> <span id="FREE"></span> * * *<dt>* * * * 免費 *</dt> <span id="delete"></span> <span id="DELETE"></span> * * *<dt>* * * * 刪除 * *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> * *<dt>* * * * deleteArray *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> * * *<dt>* * * * 發行 *</dt> * * </dl> |
| **operation**<br/>   | 字元 \_ 字串<br/> | Yes<br/> | 作業的名稱。<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                               | 描述                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | 針對埠類型作業產生存根函式的實作為。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




