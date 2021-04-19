---
description: SCM 支援控制碼類型，以允許存取下列物件。
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975921"
---
# <a name="scm-handles"></a><span data-ttu-id="13170-103">SCM 控制碼</span><span class="sxs-lookup"><span data-stu-id="13170-103">SCM Handles</span></span>

<span data-ttu-id="13170-104">SCM 支援控制碼類型，以允許存取下列物件。</span><span class="sxs-lookup"><span data-stu-id="13170-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="13170-105">已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="13170-105">The database of installed services.</span></span>
-   <span data-ttu-id="13170-106">服務。</span><span class="sxs-lookup"><span data-stu-id="13170-106">A service.</span></span>
-   <span data-ttu-id="13170-107">資料庫鎖定。</span><span class="sxs-lookup"><span data-stu-id="13170-107">The database lock.</span></span>

<span data-ttu-id="13170-108">SCManager 物件代表已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="13170-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="13170-109">它是保存服務物件的容器物件。</span><span class="sxs-lookup"><span data-stu-id="13170-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="13170-110">[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)函式會將控制碼傳回至指定電腦上的 SCManager 物件。</span><span class="sxs-lookup"><span data-stu-id="13170-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="13170-111">當您安裝、刪除、開啟和列舉服務，以及鎖定服務資料庫時，會使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="13170-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="13170-112">服務物件代表已安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="13170-112">A service object represents an installed service.</span></span> <span data-ttu-id="13170-113">[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)和 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)函數會傳回已安裝服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13170-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="13170-114">[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)、 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)和 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)函數可以要求不同類型的 SCManager 和服務物件存取權。</span><span class="sxs-lookup"><span data-stu-id="13170-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="13170-115">根據呼叫進程的存取權杖以及與 SCManager 或服務物件相關聯的安全描述項，授與或拒絕所要求的存取權。</span><span class="sxs-lookup"><span data-stu-id="13170-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="13170-116">[**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)函式會關閉 SCManager 和服務物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13170-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="13170-117">當您不再需要這些控制碼時，請務必將它們關閉。</span><span class="sxs-lookup"><span data-stu-id="13170-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



