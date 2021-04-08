---
title: 註冊 RAS 安全性 DLL
description: RAS 安全性 DLL 的安裝程式必須向 Windows NT/Windows 2000 RAS 伺服器註冊 DLL。
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672772"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="60d81-103">註冊 RAS 安全性 DLL</span><span class="sxs-lookup"><span data-stu-id="60d81-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="60d81-104">RAS 安全性 DLL 的安裝程式必須向 Windows NT/Windows 2000 RAS 伺服器註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="60d81-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="60d81-105">只有一個 RAS 安全性 DLL 可註冊為未提供多個安全性 Dll 的支援。</span><span class="sxs-lookup"><span data-stu-id="60d81-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="60d81-106">若要註冊 RAS 安全性 DLL，請在登錄中的下列機碼底下設定 *DLLPath* 值：</span><span class="sxs-lookup"><span data-stu-id="60d81-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="60d81-107">值名稱</span><span class="sxs-lookup"><span data-stu-id="60d81-107">Value name</span></span> | <span data-ttu-id="60d81-108">值資料</span><span class="sxs-lookup"><span data-stu-id="60d81-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d81-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="60d81-109">*DLLPath*</span></span>  | <span data-ttu-id="60d81-110">**REG \_ SZ** 字串，其中包含 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="60d81-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="60d81-111">除非 DLL 位於系統路徑所列的目錄中，否則此字串應該指定完整路徑。</span><span class="sxs-lookup"><span data-stu-id="60d81-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="60d81-112">RAS 安全性 DLL 的安裝程式也必須提供移除/卸載功能。</span><span class="sxs-lookup"><span data-stu-id="60d81-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="60d81-113">如果使用者移除 DLL，安裝程式必須從登錄中刪除 *DLLPath* 值。</span><span class="sxs-lookup"><span data-stu-id="60d81-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="60d81-114">如果 *DLLPath* 值指定了找不到的 DLL，RAS 服務就不會啟動。</span><span class="sxs-lookup"><span data-stu-id="60d81-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="60d81-115">RAS 安全性 DLL 必須匯出 [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) 和 [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) 函數。</span><span class="sxs-lookup"><span data-stu-id="60d81-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




