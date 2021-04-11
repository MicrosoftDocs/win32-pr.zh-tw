---
description: 當 \_ 您在 nonrooted 資料平面中使用 d 分葉通訊端時，會想要將傳送的流量送回相同的通訊端上。 適用于 \_ WSAIoctl 的 SIO MULTIPOINT \_ 回送命令程式碼可用來啟用或停用 MULTIPOINT 流量的回送。
ms.assetid: 5e267287-0ff5-4943-882f-5fe6687cca10
title: WSAIoctl 的 SIO_MULTIPOINT_LOOPBACK 命令程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61e58a9f1db6f246e9e76ec527e57353bb35cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943418"
---
# <a name="sio_multipoint_loopback-command-code-for-wsaioctl"></a><span data-ttu-id="1e19c-104">\_ \_ 適用于 WSAIOCTL 的 SIO MULTIPOINT 回送命令程式碼</span><span class="sxs-lookup"><span data-stu-id="1e19c-104">SIO\_MULTIPOINT\_LOOPBACK Command Code for WSAIoctl</span></span>

<span data-ttu-id="1e19c-105">當 \_ 您在 nonrooted 資料平面中使用 d 分葉通訊端時，會想要將傳送的流量送回相同的通訊端上。</span><span class="sxs-lookup"><span data-stu-id="1e19c-105">When d\_leaf sockets are used in a nonrooted data plane, it is desirable to have traffic that is sent out received back on the same socket.</span></span> <span data-ttu-id="1e19c-106">適用于 \_ WSAIoctl 的 SIO MULTIPOINT \_ 回[](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)送命令程式碼可用來啟用或停用 MULTIPOINT 流量的回送。</span><span class="sxs-lookup"><span data-stu-id="1e19c-106">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 



