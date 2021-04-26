---
description: 指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autoStatic 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994925"
---
# <a name="autostatic-element"></a>autoStatic 元素

指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。 預設會啟用此行為。

## <a name="usage"></a>使用方式

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

**AutoStatic** 元素不是必要專案，而且可能會在 XML 設定檔中省略。 元素可用來停用產生的欄位標記為靜態，或明確地將某些產生的欄位標記為靜態。

可能的值為 1 (啟用、預設) 和 0 (停用) 。 根據程式碼產生器將程式碼產生器導向至輸出資料的方式而定，啟用 **autoStatic** 可能會造成編譯問題。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




