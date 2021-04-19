---
description: 下列清單提供每個 Winsock ATM 結構的精確描述。 如需任何結構的詳細資訊，請按一下結構名稱。
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Winsock ATM 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974153"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="ff357-104">Winsock ATM 結構</span><span class="sxs-lookup"><span data-stu-id="ff357-104">Winsock ATM Structures</span></span>

<span data-ttu-id="ff357-105">下列清單提供每個 Winsock ATM 結構的精確描述。</span><span class="sxs-lookup"><span data-stu-id="ff357-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="ff357-106">如需任何結構的詳細資訊，請按一下結構名稱。</span><span class="sxs-lookup"><span data-stu-id="ff357-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="ff357-107">ATM 結構</span><span class="sxs-lookup"><span data-stu-id="ff357-107">ATM Structure</span></span>                           | <span data-ttu-id="ff357-108">Description</span><span class="sxs-lookup"><span data-stu-id="ff357-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="ff357-109">**ATM \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ff357-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="ff357-110">將 ATM 位址資料儲存在 ATM 型通訊端中。</span><span class="sxs-lookup"><span data-stu-id="ff357-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="ff357-111">**ATM \_ BHLI**</span><span class="sxs-lookup"><span data-stu-id="ff357-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="ff357-112">識別相關聯的 ATM 通訊端的 B-HLI 資訊。</span><span class="sxs-lookup"><span data-stu-id="ff357-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="ff357-113">**ATM \_ BLLI**</span><span class="sxs-lookup"><span data-stu-id="ff357-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="ff357-114">識別相關聯之 ATM 通訊端的 B LLI 資訊。</span><span class="sxs-lookup"><span data-stu-id="ff357-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="ff357-115">**sockaddr \_ atm**</span><span class="sxs-lookup"><span data-stu-id="ff357-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="ff357-116">儲存 ATM 通訊端的通訊端位址資訊。</span><span class="sxs-lookup"><span data-stu-id="ff357-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="ff357-117">若為原生 ATM 服務，請針對 \_ 位址家族使用 AF atm，並使用 [**sockaddr 的 \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) 通訊端位址結構。</span><span class="sxs-lookup"><span data-stu-id="ff357-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="ff357-118">若要開啟原生的 ATM 通訊端，請分別將 AF \_ 的 atm、SOCK \_ RAW 和 ATMPROTO \_ AAL5 或 ATMPROTO \_ AALUSER 傳遞至 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數。</span><span class="sxs-lookup"><span data-stu-id="ff357-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



