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
# <a name="protocol"></a><span data-ttu-id="9d037-104">通訊協定</span><span class="sxs-lookup"><span data-stu-id="9d037-104">Protocol</span></span>

<span data-ttu-id="9d037-105">指出 OLE 1 容器中可插入這個 OLE 2 類別。</span><span class="sxs-lookup"><span data-stu-id="9d037-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9d037-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="9d037-106">Registry Entry</span></span>

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

## <a name="remarks"></a><span data-ttu-id="9d037-107">備註</span><span class="sxs-lookup"><span data-stu-id="9d037-107">Remarks</span></span>

<span data-ttu-id="9d037-108">**StdFileEditing** 專案會指定 OLE 1 相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="9d037-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="9d037-109">只有當此類別的物件可在 OLE 1 容器中插入時，才會出現此情況。</span><span class="sxs-lookup"><span data-stu-id="9d037-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="9d037-110">**伺服器** 會指定 OLE 2 伺服器應用程式的完整路徑，而 **動詞** 命令會指定動詞。</span><span class="sxs-lookup"><span data-stu-id="9d037-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="9d037-111">動詞0是主要動詞，而其他動詞必須連續編號。</span><span class="sxs-lookup"><span data-stu-id="9d037-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




