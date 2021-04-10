---
title: " (網路管理) 的會話函數"
description: 網路管理會話功能會控制在工作站和伺服器之間建立的網路會話。 函數需要在伺服器上啟動伺服器服務。
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842992"
---
# <a name="session-functions-network-management"></a><span data-ttu-id="b660e-104"> (網路管理) 的會話函數</span><span class="sxs-lookup"><span data-stu-id="b660e-104">Session Functions (Network Management)</span></span>

<span data-ttu-id="b660e-105">網路管理會話功能會控制在工作站和伺服器之間建立的網路會話。</span><span class="sxs-lookup"><span data-stu-id="b660e-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="b660e-106">函數需要在伺服器上啟動伺服器服務。</span><span class="sxs-lookup"><span data-stu-id="b660e-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="b660e-107">以下列出會話函數。</span><span class="sxs-lookup"><span data-stu-id="b660e-107">The session functions are listed following.</span></span>



| <span data-ttu-id="b660e-108">函式</span><span class="sxs-lookup"><span data-stu-id="b660e-108">Function</span></span>                                      | <span data-ttu-id="b660e-109">描述</span><span class="sxs-lookup"><span data-stu-id="b660e-109">Description</span></span>                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b660e-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="b660e-110">**NetSessionDel**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="b660e-111">刪除工作站與伺服器之間的目前連接;終止網路會話。</span><span class="sxs-lookup"><span data-stu-id="b660e-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="b660e-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="b660e-112">**NetSessionEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="b660e-113">傳回針對伺服器建立之所有目前會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b660e-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="b660e-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b660e-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="b660e-115">傳回特定會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b660e-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="b660e-116">*會話* 是工作站和伺服器之間的連結。</span><span class="sxs-lookup"><span data-stu-id="b660e-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="b660e-117">當工作站第一次建立與伺服器上共用資源的連接時，就會建立會話。</span><span class="sxs-lookup"><span data-stu-id="b660e-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="b660e-118">在會話結束之前，工作站和伺服器之間的所有進一步連線都是相同會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="b660e-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="b660e-119">若要結束會話，連接的伺服器端上的應用程式會呼叫 [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) 函數。</span><span class="sxs-lookup"><span data-stu-id="b660e-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="b660e-120">網路管理會話函式會使用 *username* 參數來管理每個使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="b660e-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="b660e-121">因為每個會話可以有多個使用者，所以需要此參數才能存取會話的使用者特定資訊。</span><span class="sxs-lookup"><span data-stu-id="b660e-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="b660e-122">會話函數可在下列資訊層級取得：</span><span class="sxs-lookup"><span data-stu-id="b660e-122">Session functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="b660e-123">**會話 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="b660e-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [<span data-ttu-id="b660e-124">**會話 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b660e-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [<span data-ttu-id="b660e-125">**會話 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b660e-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [<span data-ttu-id="b660e-126">**會話 \_ 資訊 \_ 10**</span><span class="sxs-lookup"><span data-stu-id="b660e-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [<span data-ttu-id="b660e-127">**會話 \_ 資訊 \_ 502**</span><span class="sxs-lookup"><span data-stu-id="b660e-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

<span data-ttu-id="b660e-128">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理會話功能達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="b660e-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="b660e-129">如需詳細資訊，請參閱 [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) 和 [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)。</span><span class="sxs-lookup"><span data-stu-id="b660e-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
