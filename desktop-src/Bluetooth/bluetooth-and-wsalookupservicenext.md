---
title: 藍牙和 WSALookupServiceNext
description: 藍牙使用 WSALookupServiceNext 函式來比對 WSALookupServiceBegin 先前呼叫中所指定的查詢。
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- 藍牙
- WSALookupServiceNext
- 藍牙和 WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010390"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>藍牙和 WSALookupServiceNext

藍牙使用 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式來比對 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)先前呼叫中所指定的查詢。 **WSALookupServiceNext** 函式的結果取決於在初始 **WSALookupServiceBegin** 函式呼叫中傳遞的 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構中所設定的設定。

在藍牙中進行裝置查詢和服務探索的步驟，會有足夠的差異，可進行個別的處理。 如需有關藍牙的詳細資訊，以及裝置查詢的 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式，請參閱 [藍牙和針對裝置查詢的 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)。 如需有關藍牙的詳細資訊以及服務探索的 **WSALookupServiceBegin** 函式，請參閱 [服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[裝置查詢的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[藍牙和 WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect)
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
</dt> </dl>

 

 