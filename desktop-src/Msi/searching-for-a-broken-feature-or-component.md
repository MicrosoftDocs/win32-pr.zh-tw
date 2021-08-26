---
description: 安裝程式可以自動重新安裝損毀的元件，藉此提升應用程式的復原能力。
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: 搜尋中斷的功能或元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa17fc66fdf0bda0a04df9a5917d4e79671b32f453ead921d4f43f89bbd47dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041238"
---
# <a name="searching-for-a-broken-feature-or-component"></a>搜尋中斷的功能或元件

安裝程式可以自動重新安裝損毀的元件，藉此提升應用程式的 [復原能力](resiliency.md) 。 具體而言，安裝程式會在發現 [元件資料表](component-table.md) 的 KeyPath 資料行中指定的檔案或登錄機碼遺失時，重新安裝元件或功能。

如果來源中的功能元件 KeyPath 損毀，或在資料庫中撰寫 KeyPath 的方式發生錯誤，安裝程式可能會嘗試開啟安裝套件，並在每次啟用功能的快捷方式時重新安裝該功能。

若要判斷重複嘗試重新安裝功能或應用程式的原因，請檢查事件記錄檔中的兩個專案，如下所示。

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

第一個訊息指出正在安裝產品套件中的哪個元件。 這是 \_ [快捷方式資料表](shortcut-table.md)之 [元件] 資料行中所參考的元件。

第二個訊息指出哪個元件偵測失敗。 這是有遺失或損毀的 KeyPath 會觸發重新安裝的元件。

 

 



