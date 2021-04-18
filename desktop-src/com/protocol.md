---
title: 通訊協定
description: 指出 OLE 1 容器中可插入這個 OLE 2 類別。
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- 通訊協定登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968652"
---
# <a name="protocol"></a>通訊協定

指出 OLE 1 容器中可插入這個 OLE 2 類別。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>備註

**StdFileEditing** 專案會指定 OLE 1 相容性資訊。 只有當此類別的物件可在 OLE 1 容器中插入時，才會出現此情況。

**伺服器** 會指定 OLE 2 伺服器應用程式的完整路徑，而 **動詞** 命令會指定動詞。 動詞0是主要動詞，而其他動詞必須連續編號。

 

 




