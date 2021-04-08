---
title: NONREDIST
description: 將名稱加入至封裝中的 COM + 應用程式在其他電腦上安裝時，不應該匯出的檔案清單。 請注意，這是子機碼，而不是值。
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- NONREDIST 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022139"
---
# <a name="nonredist"></a><span data-ttu-id="8a36f-105">NONREDIST</span><span class="sxs-lookup"><span data-stu-id="8a36f-105">NONREDIST</span></span>

<span data-ttu-id="8a36f-106">將名稱加入至封裝中的 COM + 應用程式在其他電腦上安裝時，不應該匯出的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="8a36f-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="8a36f-107">請注意，這是子機碼，而不是值。</span><span class="sxs-lookup"><span data-stu-id="8a36f-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8a36f-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="8a36f-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="8a36f-109">備註</span><span class="sxs-lookup"><span data-stu-id="8a36f-109">Remarks</span></span>

<span data-ttu-id="8a36f-110">您新增至清單的檔案會以儲存在此機碼下的名稱/值組來表示。</span><span class="sxs-lookup"><span data-stu-id="8a36f-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="8a36f-111">在每個名稱/值組中，名稱都是檔案名，而值則是保留名稱。</span><span class="sxs-lookup"><span data-stu-id="8a36f-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




