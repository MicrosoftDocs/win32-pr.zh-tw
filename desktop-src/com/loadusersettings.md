---
title: LoadUserSettings
description: 判斷 COM 是否會載入執行的 COM 伺服器的使用者設定檔，做為啟動使用者應用程式識別。
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- LoadUserSettings 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932410"
---
# <a name="loadusersettings"></a><span data-ttu-id="66313-104">LoadUserSettings</span><span class="sxs-lookup"><span data-stu-id="66313-104">LoadUserSettings</span></span>

<span data-ttu-id="66313-105">判斷 COM 是否會載入執行的 COM 伺服器的使用者設定檔，做為啟動使用者應用程式識別。</span><span class="sxs-lookup"><span data-stu-id="66313-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="66313-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="66313-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="66313-107">備註</span><span class="sxs-lookup"><span data-stu-id="66313-107">Remarks</span></span>

<span data-ttu-id="66313-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="66313-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="66313-109">如果 *值* 為非零值，則 com 會載入用來啟動 COM 伺服器之使用者帳戶的設定檔。</span><span class="sxs-lookup"><span data-stu-id="66313-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="66313-110">如果 *值* 為零或不存在，com 將不會載入用來啟動 COM 伺服器之使用者帳戶的設定檔。</span><span class="sxs-lookup"><span data-stu-id="66313-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="66313-111">如果有 [**RunAs**](runas.md) 專案存在，就會忽略此設定。</span><span class="sxs-lookup"><span data-stu-id="66313-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




