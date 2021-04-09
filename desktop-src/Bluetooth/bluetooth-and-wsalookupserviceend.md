---
title: 藍牙和 WSALookupServiceEnd
description: 藍牙使用 WSALookupServiceEnd 函式來終止先前呼叫 WSALookupServiceBegin 時起始的查詢，而且可能會在後續的 WSALookupServiceNext 呼叫中延伸。
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- 藍牙和 WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933325"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>藍牙和 WSALookupServiceEnd

藍牙使用 [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) 函式來終止先前呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)時起始的查詢，而且可能會在後續的 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)呼叫中延伸。 呼叫 **WSALookupServiceEnd** 會終止查詢並清除內容。

在藍牙中進行裝置查詢和服務探索的步驟，與進行不同的處理方式有足夠的差異。 如需藍牙和裝置查詢的 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 函式的詳細資訊，請參閱 [藍牙和 WSALookupServiceBegin 中的裝置查詢](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)。 如需有關藍牙和服務探索之 **WSALookupServiceBegin** 功能的詳細資訊，請參閱 [適用于服務探索的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[適用于裝置查詢的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[適用于服務探索的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
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

 

 