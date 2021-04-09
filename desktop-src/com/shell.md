---
title: 'Shell (COM) '
description: 提供 Windows 3.1 shell 列印和檔案開啟資訊。
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Shell 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685369"
---
# <a name="shell-com"></a><span data-ttu-id="ee9f7-104">Shell (COM) </span><span class="sxs-lookup"><span data-stu-id="ee9f7-104">Shell (COM)</span></span>

<span data-ttu-id="ee9f7-105">提供 Windows 3.1 shell 列印和檔案 **開啟** 資訊。</span><span class="sxs-lookup"><span data-stu-id="ee9f7-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ee9f7-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="ee9f7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="ee9f7-107">備註</span><span class="sxs-lookup"><span data-stu-id="ee9f7-107">Remarks</span></span>

<span data-ttu-id="ee9f7-108">這些專案應該提供應用程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="ee9f7-108">These entries should provide the path and file name of the application.</span></span>

 

 




