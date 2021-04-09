---
title: 藍牙和 getaddrinfo
description: Getaddrinfo 函式會提供從主機名稱到位址的轉換，以供以 IP 為基礎的傳輸。 因為 getaddrinfo 函式是以 IP 為基礎的傳輸所特有，所以它會在 Bluetooth 通訊端上失敗。
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- 藍牙與 getaddrinfo 藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682995"
---
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="71bd9-105">藍牙和 getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="71bd9-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="71bd9-106">[**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)函式會提供從主機名稱到位址的轉換，以供以 IP 為基礎的傳輸。</span><span class="sxs-lookup"><span data-stu-id="71bd9-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="71bd9-107">因為 **getaddrinfo** 函式是以 IP 為基礎的傳輸所特有，所以它會在 Bluetooth 通訊端上失敗。</span><span class="sxs-lookup"><span data-stu-id="71bd9-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="71bd9-108">若要執行從主機名稱到 Bluetooth 通訊端位址的轉譯，請使用 [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) 函式搭配 **LUP \_ 容器** 來查詢遠端裝置，然後搜尋特定的相符遠端名稱和對應的位址。</span><span class="sxs-lookup"><span data-stu-id="71bd9-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71bd9-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="71bd9-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71bd9-110">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="71bd9-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="71bd9-111">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="71bd9-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="71bd9-112">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="71bd9-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 