---
title: 藍牙和 getaddrinfo
description: Getaddrinfo 函式會提供從主機名稱到位址的轉換，以供以 IP 為基礎的傳輸。 因為 getaddrinfo 函式是以 IP 為基礎的傳輸所特有，所以它會在藍牙通訊端上失敗。
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- 藍牙和 getaddrinfo 藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9faea4cebf9eee183942da04f39dfae123feea4900483d27ae2d70d8cb5b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004528"
---
# <a name="bluetooth-and-getaddrinfo"></a>藍牙和 getaddrinfo

[**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)函式會提供從主機名稱到位址的轉換，以供以 IP 為基礎的傳輸。 因為 **getaddrinfo** 函式是以 IP 為基礎的傳輸所特有，所以它會在藍牙通訊端上失敗。

若要從主機名稱對藍牙通訊端的位址執行轉譯，請使用 [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)函式搭配 **LUP \_ 容器** 來查詢遠端裝置，然後搜尋特定的相符遠端名稱和對應的位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 