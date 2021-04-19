---
description: 使用者可以使用 [服務] 控制台公用程式來啟動服務。 使用者可以在 [開始參數] 欄位中指定服務的引數。 服務控制程式可以啟動服務，並使用 StartService 函式指定其引數。
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: 依需求啟動服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001430"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="5d666-105">依需求啟動服務</span><span class="sxs-lookup"><span data-stu-id="5d666-105">Starting Services on Demand</span></span>

<span data-ttu-id="5d666-106">使用者可以使用 [服務] 控制台公用程式來啟動服務。</span><span class="sxs-lookup"><span data-stu-id="5d666-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="5d666-107">使用者可以在 [ **開始參數** ] 欄位中指定服務的引數。</span><span class="sxs-lookup"><span data-stu-id="5d666-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="5d666-108">服務控制程式可以啟動服務，並使用 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函式指定其引數。</span><span class="sxs-lookup"><span data-stu-id="5d666-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="5d666-109">當服務啟動時，SCM 會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5d666-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="5d666-110">取出儲存在資料庫中的帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="5d666-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="5d666-111">登入服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d666-111">Log on the service account.</span></span>
-   <span data-ttu-id="5d666-112">載入使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="5d666-112">Load the user profile.</span></span>
-   <span data-ttu-id="5d666-113">建立處於暫停狀態的服務。</span><span class="sxs-lookup"><span data-stu-id="5d666-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="5d666-114">將登入權杖指派給處理常式。</span><span class="sxs-lookup"><span data-stu-id="5d666-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="5d666-115">允許進程執行。</span><span class="sxs-lookup"><span data-stu-id="5d666-115">Allow the process to execute.</span></span>

 

 



