---
title: Visual Basic 方法附注 accName
description: 物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840132"
---
# <a name="visual-basic-method-notes-accname"></a>Visual Basic 方法附注： accName

物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。 Oleacc 檔案包含設定函數屬性之版本的下列定義：


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



雖然 *varChild* 參數在 ODL 檔和物件瀏覽器中列為選擇性，但在呼叫 [**accName**](https://www.bing.com/search?q=**accName**)的屬性設定版本時，您必須將它加入。

 

 




