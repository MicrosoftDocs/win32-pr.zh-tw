---
title: RAS 管理 DLL 登錄設定
description: 協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL。
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507405"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="0b860-103">RAS 管理 DLL 登錄設定</span><span class="sxs-lookup"><span data-stu-id="0b860-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="0b860-104">協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="0b860-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0b860-105">若要註冊 DLL，請在此機碼下設定下列值。</span><span class="sxs-lookup"><span data-stu-id="0b860-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="0b860-106">值名稱</span><span class="sxs-lookup"><span data-stu-id="0b860-106">Value name</span></span>    | <span data-ttu-id="0b860-107">值資料</span><span class="sxs-lookup"><span data-stu-id="0b860-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0b860-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="0b860-108">*DisplayName*</span></span> | <span data-ttu-id="0b860-109">**REG \_ SZ** 字串，其中包含 DLL 的使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0b860-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="0b860-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="0b860-110">*DLLPath*</span></span>     | <span data-ttu-id="0b860-111">**REG \_ SZ** 字串，其中包含 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0b860-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="0b860-112">例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能是：</span><span class="sxs-lookup"><span data-stu-id="0b860-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0b860-113">*DisplayName* ： **REG \_ SZ** ： ProElectron RAS 管理 DLL</span><span class="sxs-lookup"><span data-stu-id="0b860-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="0b860-114">*DLLPath* ： **REG \_ SZ** ： C： \\ nt \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="0b860-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="0b860-115">RAS 系統管理 DLL 的安裝程式也應該提供移除/卸載功能。</span><span class="sxs-lookup"><span data-stu-id="0b860-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="0b860-116">如果使用者移除 DLL，安裝程式應該刪除 DLL 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="0b860-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




