---
title: 適用于裝置查詢的藍牙和 WSAQUERYSET
description: 用來協助探索藍牙命名空間（NS BTH）中的裝置和服務 \_ 。
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- 適用于裝置的藍牙與 WSAQUERYSET 查詢藍牙
- WSAQUERYSET 藍牙，適用于裝置查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de7adf8c15907fe539ddac5133df08d68ee7c4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682443"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>適用于裝置查詢的藍牙和 WSAQUERYSET

在 Bluetooth 中， [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構是用來協助探索藍牙命名空間 NS BTH 中的裝置和服務 \_ 。

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)和 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數會使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構來取得裝置查詢程式的相關資訊。 下表列出並描述 **WSAQUERYSET** 結構中的成員值。

| 成員                      | 使用指定的 LUP 容器輸入至 WSALookupServiceBegin \_                                                                                                                                              | 從 WSALookupServiceNext 傳回的值                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | 必須設定為 **sizeof** ([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) 。                                                                                                                                       | **sizeof** (系統傳回的 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) 。                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | 未使用。                                                                                                                                                                                                  | 可能有一或多個旗標設定： **BTHNS \_ 結果 \_ 裝置 \_ 已連線** 指定裝置已連線。<br/> **BTHNS \_\_ \_ 記住的結果裝置** 會指定裝置是已記住的裝置。 並非所有記住的裝置都會經過驗證。<br/> **BTHNS \_\_ \_ 經過驗證的結果裝置** 會指定裝置已通過驗證、配對或進行。 系統會記住所有已驗證的裝置。<br/> |
| **lpszServiceInstanceName** | 未使用。                                                                                                                                                                                                  | 裝置的顯示名稱，原先從藍牙遠端名稱要求操作傳回，而且可能由本機使用者更新。 如果指定了 **LUP 傳回 \_ \_ 名稱** ，則會傳回。                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | 未使用。                                                                                                                                                                                                  | 裝置的32位藍牙類別 (出貨) 欄位，對應至 GUID 的 **Data1** 成員。 如果指定了 **LUP 傳回 \_ \_ 類型** ，則傳回。                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | 必須是 NS \_ BTH。                                                                                                                                                                                           | 傳回 **NS \_ BTH**。                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszCoNtext**             | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | 未使用。                                                                                                                                                                                                  | 未使用。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | 未使用。                                                                                                                                                                                                  | 指出 [**CSADDR \_ 資訊**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) 結構陣列中的元素數目。                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | 未使用。                                                                                                                                                                                                  | [**CSADDR \_ 資訊**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)結構的指標，其 **LocalAddr. lpSockaddr** 成員指向具有遠端裝置位址的 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構。 如果指定了 **LUP 傳回 \_ \_ ADDR** ，則會傳回。                                                                                                                                                                  |
| **lpBlob**                  | 選擇性。 可能指向指向 [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)結構的 [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構，此結構可能會限制非快取裝置查詢作業的長度。 | 指向 [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)結構之 [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構的指標。 如果指定 **LUP \_ RETURN \_ BLOB** ，則會傳回 **lpBlob** 。 指定 **LUP \_ 傳回 \_ 名稱** ，以取得 **BTH \_ 裝置 \_ 資訊** 的名稱欄位。                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于設定服務的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[用於服務查詢的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[藍牙和 BLOB](bluetooth-and-blob.md)
</dt> <dt>

[藍牙和 WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[藍牙和 WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**CSADDR \_ 資訊**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

