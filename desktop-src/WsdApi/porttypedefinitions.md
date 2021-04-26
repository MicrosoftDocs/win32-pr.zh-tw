---
description: 產生埠類型的 C 常數。
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: portTypeDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996545"
---
# <a name="porttypedefinitions-element"></a>portTypeDefinitions 元素

產生埠類型的 C 常數。

## <a name="usage"></a>使用方式

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                   | 描述                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**代號**](codename.md)<br/>                   | 指定要在產生的程式碼中用於埠類型的名稱。 根據預設，會從埠類型的限定名稱產生程式碼名稱。<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | 指定存根函數參考是否應該包含在通知作業的埠類型定義中的作業結構中。<br/> <br/>        |
| [**操作**](operation.md)<br/>                 | 指定要產生程式碼的作業。<br/> <br/>                                                                                                  |
| [**portType**](porttype.md)<br/>                   | 指定要產生程式碼的埠類型。<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | 指定存根函式參考是否應該包含在單向和雙向作業的埠類型定義中的作業結構中。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

此元素通常用於 C 來源檔案，以提供 [**portTypeDeclarations**](porttypedeclarations.md)所宣告的埠類型常數。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




