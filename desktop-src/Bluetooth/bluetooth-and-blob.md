---
title: 藍牙和 BLOB
description: 藍牙在呼叫 WSASetService 或 WSALookupService \ 函式期間，使用 BLOB 結構來傳遞或接收傳輸特定資料到 WSAQUERYSET 結構。
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- 藍牙
- 藍牙
- 藍牙和 BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081132"
---
# <a name="bluetooth-and-blob"></a>藍牙和 BLOB

藍牙在呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md)或 **WSALookupService** 函式期間，使用 [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構來傳遞或接收傳輸特定資料到 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構 \* 。

若要搭配藍牙和 [**WSASetService**](bluetooth-and-wsasetservice.md)函式使用， [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構成員必須具有下列設定：

-   **Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 集 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構大小（以位元組為單位）。
-   **PBlobData** 成員必須是 [**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構的指標。

若要搭配使用藍牙和[WSALookupServiceBegin 進行裝置查詢](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)，請使用下列設定：

-   **Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)結構大小（以位元組為單位）。
-   **PBlobData** 成員必須是 [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)結構的指標。

若要搭配使用藍牙和[WSALookupServiceBegin 進行服務探索](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)，請使用下列設定：

-   **Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構大小（以位元組為單位）。
-   **PBlobData** 成員必須是 [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構的指標。

如需詳細資訊，請參閱 [**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) 結構參考頁面中的「備註」一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置查詢的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[藍牙和 WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 