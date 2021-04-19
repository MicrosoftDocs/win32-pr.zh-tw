---
description: Windows 會載入並執行標準的 Microsoft GINA DLL (MSGina.dll) 。 若要載入不同的 GINA，您必須變更登錄機碼值。
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: 載入和執行 GINA DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971848"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="2c89e-104">載入和執行 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="2c89e-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="2c89e-105">Windows 會載入並執行標準的 Microsoft GINA DLL (MSGina.dll) 。</span><span class="sxs-lookup"><span data-stu-id="2c89e-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="2c89e-106">若要載入不同的 [*GINA*](../secgloss/g-gly.md)，您必須變更下列登錄機碼值：</span><span class="sxs-lookup"><span data-stu-id="2c89e-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="2c89e-107">如果有 GinaDLL 機碼值，它必須包含 [*Winlogon*](../secgloss/w-gly.md) 將載入和使用的 GINA DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="2c89e-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c89e-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c89e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c89e-109">建立和測試 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="2c89e-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="2c89e-110">GINA 匯出函數</span><span class="sxs-lookup"><span data-stu-id="2c89e-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="2c89e-111">GINA 結構</span><span class="sxs-lookup"><span data-stu-id="2c89e-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="2c89e-112">終端機服務 GINA 函式</span><span class="sxs-lookup"><span data-stu-id="2c89e-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
