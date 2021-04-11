---
description: Windows 通訊端中的 Multipoint 通訊端屬性 (Winsock) 。
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Multipoint 通訊端屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da67fd40c7c3bc7f1e9dbff22a3fef6cdaee4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191332"
---
# <a name="multipoint-socket-attributes"></a><span data-ttu-id="fd0ac-103">Multipoint 通訊端屬性</span><span class="sxs-lookup"><span data-stu-id="fd0ac-103">Multipoint Socket Attributes</span></span>

<span data-ttu-id="fd0ac-104">在聯結至 multipoint 會話的某些實例中，可能會有與點對點通訊端的一些行為差異。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-104">In some instances sockets joined to a multipoint session may have some behavioral differences from point-to-point sockets.</span></span> <span data-ttu-id="fd0ac-105">例如， \_ 根資料平面配置中的 d 分葉通訊端只能將資訊傳送給 d \_ 根參與者。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="fd0ac-106">這會讓用戶端需要能夠指出通訊端的預期使用方式與其建立方式一致。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-106">This creates a need for the client to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="fd0ac-107">這是透過可透過 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)中的 *dwFlags* 參數設定的四個 multipoint 屬性旗標來完成：</span><span class="sxs-lookup"><span data-stu-id="fd0ac-107">This is done through four multipoint attribute flags that can be set through the *dwFlags* parameter in [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):</span></span>

-   <span data-ttu-id="fd0ac-108">WSA \_ 旗標 \_ MULTIPOINT \_ C \_ root，用於建立作為 C 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根控制項平面時才允許。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="fd0ac-109">WSA \_ 旗 \_ \_ 標 MULTIPOINT C 分 \_ 葉，用於建立作為 C 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="fd0ac-110">WSA \_ 旗標 \_ MULTIPOINT \_ D \_ root，用於建立做為 D 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根資料平面時才允許。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="fd0ac-111">WSA \_ 旗標 \_ MULTIPOINT \_ D 分 \_ 葉，用於建立做為 D 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="fd0ac-112">建立 multipoint 通訊端時，必須在 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)的 *dwFlags* 參數中設定兩個控制平面旗標的其中一個，以及兩個數據平面旗標的其中一個。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-112">When creating a multipoint socket, exactly one of the two control plane flags, and one of the two data plane flags must be set in [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)'s *dwFlags* parameter.</span></span> <span data-ttu-id="fd0ac-113">因此，建立 multipoint 通訊端的四種可能性如下：「c \_ 根/d \_ 根目錄」、「c \_ 根/d 分 \_ 葉」、「c 分 \_ 葉/d \_ 根目錄」或「c 分 \_ 葉/d 分葉」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fd0ac-113">Thus, the four possibilities for creating multipoint sockets are: "c\_root/d\_root", "c\_root/d\_leaf", "c\_leaf/d\_root", or "c\_leaf /d\_leaf".</span></span>

 

 
