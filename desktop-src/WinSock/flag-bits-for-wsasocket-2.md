---
description: 在聯結至 multipoint 會話的某些實例中，從點對點通訊端的行為可能有所差異。
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: WSASocket 的旗標位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971398"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="8d4fc-103">WSASocket 的旗標位</span><span class="sxs-lookup"><span data-stu-id="8d4fc-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="8d4fc-104">在聯結至 multipoint 會話的某些實例中，從點對點通訊端的行為可能有所差異。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="8d4fc-105">例如， \_ 根資料平面配置中的 d 分葉通訊端只能將資訊傳送給 d \_ 根參與者。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="8d4fc-106">這會讓應用程式必須能夠指出通訊端的預期使用方式與其建立方式一致。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="8d4fc-107">這是透過可在 *dwFlags* 參數中設定為 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的四個旗標位來完成：</span><span class="sxs-lookup"><span data-stu-id="8d4fc-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="8d4fc-108">WSA \_ 旗標 \_ MULTIPOINT \_ C \_ root，用於建立作為 C 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根控制項平面時才允許。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d4fc-109">WSA \_ 旗 \_ \_ 標 MULTIPOINT C 分 \_ 葉，用於建立作為 C 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d4fc-110">WSA \_ 旗標 \_ MULTIPOINT \_ D \_ root，用於建立做為 D 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根資料平面時才允許。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d4fc-111">WSA \_ 旗標 \_ MULTIPOINT \_ D 分 \_ 葉，用於建立做為 D 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="8d4fc-112">請注意，建立 multipoint 通訊端時，正好是兩個控制平面旗標的其中一個，而且必須在 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的 *dwFlags* 參數中設定兩個數據平面旗標的其中一個。</span><span class="sxs-lookup"><span data-stu-id="8d4fc-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="8d4fc-113">因此，建立 multipoint 通訊端的四種可能性如下：</span><span class="sxs-lookup"><span data-stu-id="8d4fc-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="8d4fc-114">"c \_ root/d \_ root"</span><span class="sxs-lookup"><span data-stu-id="8d4fc-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="8d4fc-115">"c \_ 根/d 分 \_ 葉"</span><span class="sxs-lookup"><span data-stu-id="8d4fc-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="8d4fc-116">"c 分 \_ 葉/d \_ 根"</span><span class="sxs-lookup"><span data-stu-id="8d4fc-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="8d4fc-117">"c 分 \_ 葉/d 分 \_ 葉"</span><span class="sxs-lookup"><span data-stu-id="8d4fc-117">"c\_leaf /d\_leaf"</span></span>

 

 
