---
description: 下列函式是由網路提供者 DLL 所執行，以與多個提供者路由器 (MPR) 進行通訊。
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: 網路提供者所執行的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945044"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="42daa-103">網路提供者所執行的函式</span><span class="sxs-lookup"><span data-stu-id="42daa-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="42daa-104">下列函式是由網路提供者 DLL 所執行，以與 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) (MPR) 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="42daa-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="42daa-105">請注意，只有 [功能函數](capabilities-functions.md) 必須由網路提供者來執行。</span><span class="sxs-lookup"><span data-stu-id="42daa-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="42daa-106">其他類型的函式的執行是選擇性的，且取決於網路提供者的需求。</span><span class="sxs-lookup"><span data-stu-id="42daa-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="42daa-107">函數集</span><span class="sxs-lookup"><span data-stu-id="42daa-107">Function set</span></span>                                                                                    | <span data-ttu-id="42daa-108">Description</span><span class="sxs-lookup"><span data-stu-id="42daa-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42daa-109">功能功能</span><span class="sxs-lookup"><span data-stu-id="42daa-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="42daa-110">允許呼叫者判斷網路提供者的功能。</span><span class="sxs-lookup"><span data-stu-id="42daa-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="42daa-111">使用者名稱函式</span><span class="sxs-lookup"><span data-stu-id="42daa-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="42daa-112">提示網路提供者提供與連接相關聯的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="42daa-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="42daa-113">裝置重新導向功能</span><span class="sxs-lookup"><span data-stu-id="42daa-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="42daa-114">允許網路提供者重新導向 Microsoft MS-DOS 作業系統上標準的裝置、磁碟機號和 LPT 埠。</span><span class="sxs-lookup"><span data-stu-id="42daa-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="42daa-115">提供者特定的對話方塊函式</span><span class="sxs-lookup"><span data-stu-id="42daa-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="42daa-116">允許網路提供者顯示或處理網路特定資訊。</span><span class="sxs-lookup"><span data-stu-id="42daa-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="42daa-117">系統管理功能</span><span class="sxs-lookup"><span data-stu-id="42daa-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="42daa-118">允許網路提供者顯示特殊的網路目錄或採取行動。</span><span class="sxs-lookup"><span data-stu-id="42daa-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="42daa-119">列舉函數</span><span class="sxs-lookup"><span data-stu-id="42daa-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="42daa-120">允許使用者流覽網路資源。</span><span class="sxs-lookup"><span data-stu-id="42daa-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="42daa-121">如需有關如何建立和註冊網路提供者的詳細資訊，請參閱 [執行網路提供](implementing-a-network-provider.md) 者和註冊網路提供者 [和認證管理員](registering-network-providers-and-credential-managers.md)。</span><span class="sxs-lookup"><span data-stu-id="42daa-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

