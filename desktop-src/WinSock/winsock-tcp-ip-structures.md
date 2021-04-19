---
description: 下列清單提供每個 Winsock TCP/IP 結構的簡短描述。 如需任何結構的詳細資訊，請按一下結構名稱。
ms.assetid: 9c9a4639-4b51-4e00-b790-a0a5841c6ed3
title: Winsock TCP/IP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e350fc6fe12f6881d08d6757c739f9480d59afa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991837"
---
# <a name="winsock-tcpip-structures"></a><span data-ttu-id="57c7b-104">Winsock TCP/IP 結構</span><span class="sxs-lookup"><span data-stu-id="57c7b-104">Winsock TCP/IP Structures</span></span>

<span data-ttu-id="57c7b-105">下列清單提供每個 Winsock TCP/IP 結構的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="57c7b-105">The following list provides concise descriptions of each Winsock TCP/IP structure.</span></span> <span data-ttu-id="57c7b-106">如需任何結構的詳細資訊，請按一下結構名稱。</span><span class="sxs-lookup"><span data-stu-id="57c7b-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="57c7b-107">TCP/IP 結構</span><span class="sxs-lookup"><span data-stu-id="57c7b-107">TCP/IP Structure</span></span>                                 | <span data-ttu-id="57c7b-108">Description</span><span class="sxs-lookup"><span data-stu-id="57c7b-108">Description</span></span>                                                                                                                              |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57c7b-109">**介面 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="57c7b-109">**INTERFACE\_INFO**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)      | <span data-ttu-id="57c7b-110">與 ioctl 命令搭配使用，以取得介面 IP 位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57c7b-110">Used with the ioctl command to obtain information about an interface IP address.</span></span>                                                         |
| [<span data-ttu-id="57c7b-111">**介面 \_ 資訊 \_ EX**</span><span class="sxs-lookup"><span data-stu-id="57c7b-111">**INTERFACE\_INFO\_EX**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) | <span data-ttu-id="57c7b-112">搭配 **SIO \_ GET \_ interface \_ LIST IOCTL** 命令使用，以取得介面 IP 位址的相關資訊，包括 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="57c7b-112">Used with the **SIO\_GET\_INTERFACE\_LIST IOCTL** command to obtain information about an interface IP address, including IPv6 addresses.</span></span> |
| [<span data-ttu-id="57c7b-113">**sockaddr \_ gen**</span><span class="sxs-lookup"><span data-stu-id="57c7b-113">**sockaddr\_gen**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-sockaddr_gen)            | <span data-ttu-id="57c7b-114">提供一般通訊端位址資訊。</span><span class="sxs-lookup"><span data-stu-id="57c7b-114">Provides generic socket address information.</span></span> <span data-ttu-id="57c7b-115">搭配 [**介面 \_ 資訊**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) 結構使用。</span><span class="sxs-lookup"><span data-stu-id="57c7b-115">Used with the [**INTERFACE\_INFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) structure.</span></span>                        |



 

 

 



