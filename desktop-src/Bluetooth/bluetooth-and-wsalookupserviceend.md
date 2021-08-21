---
title: 藍牙和 WSALookupServiceEnd
description: 藍牙使用 WSALookupServiceEnd 函式來終止先前呼叫 WSALookupServiceBegin 時起始的查詢，而且可能會在後續的 WSALookupServiceNext 呼叫中延伸。
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- 藍牙
- WSALookupServiceEnd
- 藍牙和 WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd6c893a06fbf586d07e3a2581d1d25626e161508e505dc089d7660267bae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081092"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>藍牙和 WSALookupServiceEnd

藍牙使用 [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)函式來終止先前呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)時起始的查詢，而且可能會在後續的 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)呼叫中延伸。 呼叫 **WSALookupServiceEnd** 會終止查詢並清除內容。

在藍牙中進行裝置查詢和服務探索的步驟，會有足夠的差異，可進行個別的處理。 如需有關藍牙的詳細資訊，以及裝置查詢的 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式，請參閱 [藍牙和針對裝置查詢的 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)。 如需有關藍牙的詳細資訊以及服務探索的 **WSALookupServiceBegin** 函式，請參閱 [服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[裝置查詢的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[藍牙和 WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**連線**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 