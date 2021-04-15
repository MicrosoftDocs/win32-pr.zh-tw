---
title: 取得函式
description: 網路管理取得函式會取出網域的相關資訊。 您也可以呼叫這些函式來取得本機、全域、工作站和伺服器使用者帳戶的相關資訊。
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507292"
---
# <a name="get-functions"></a><span data-ttu-id="0d9d3-104">取得函式</span><span class="sxs-lookup"><span data-stu-id="0d9d3-104">Get Functions</span></span>

<span data-ttu-id="0d9d3-105">網路管理取得函式會取出網域的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="0d9d3-106">您也可以呼叫這些函式來取得本機、全域、工作站和伺服器使用者帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="0d9d3-107">網路管理取得功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="0d9d3-108">函式</span><span class="sxs-lookup"><span data-stu-id="0d9d3-108">Function</span></span>                                                               | <span data-ttu-id="0d9d3-109">描述</span><span class="sxs-lookup"><span data-stu-id="0d9d3-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d9d3-110">**NetGetAnyDCName**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="0d9d3-111">傳回指定伺服器直接信任之網域的任何網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="0d9d3-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="0d9d3-113">針對指定的網域，傳回網域主控站 (PDC) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="0d9d3-114">**NetGetDisplayInformationIndex**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="0d9d3-115">傳回第一個顯示資訊專案的索引，其名稱開頭為指定的字串或依字母順序排列在字串後面。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="0d9d3-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="0d9d3-117">傳回使用者、電腦或通用群組帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="0d9d3-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="0d9d3-118">[**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)函數所傳回的資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="0d9d3-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="0d9d3-119">**NET \_ 顯示 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="0d9d3-120">**淨 \_ 顯示器 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="0d9d3-121">**NET \_ DISPLAY \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




