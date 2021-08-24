---
title: 通訊協定
description: 指出 OLE 1 容器中可插入這個 OLE 2 類別。
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- 通訊協定登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130020"
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

 

 




