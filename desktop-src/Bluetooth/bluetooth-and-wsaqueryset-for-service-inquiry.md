---
title: 服務查詢的藍牙和 WSAQUERYSET
description: 使用 WSAQUERYSET 結構搭配 WSALookupServiceBegin 和 WSALookupServiceNext 函式，以取得服務查詢程式的相關資訊。
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- 服務查詢藍牙的藍牙和 WSAQUERYSET
- WSAQUERYSET 藍牙，用於服務查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467095"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>服務查詢的藍牙和 WSAQUERYSET

藍牙使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構搭配各種函式，以協助探索藍牙命名空間中的裝置和服務，也就是 NS \_ BTH。

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)和 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數會使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構來取得服務查詢程式的相關資料。 下表描述如何針對此目的設定 **WSAQUERYSET** 結構中的成員值。




| 成員 | WSALookupServiceBegin 的輸入 | 從 WSALookupServiceNext 傳回的值 | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize</strong> | 必須設定為 <strong>sizeof</strong> (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。 | <strong>sizeof</strong> (系統傳回的 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。 | 
| <strong>dwOutputFlags</strong> | 未使用。 | 未使用。 | 
| <strong>lpszServiceInstanceName</strong> | 未使用。 | 服務的顯示名稱，從藍牙 ServiceName SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。 如果指定 LUP_RETURN_NAME，則傳回。 | 
| <strong>lpServiceClassId</strong> | 必要。 針對正在進行搜尋的服務，最特定的單一藍牙 UUID。 例如，如果此值設定為 L2CAP 通訊協定的 UUID，它會傳回在目標裝置上使用 L2CAP 通訊協定的所有服務。 如果設定為特定服務的 UUID，則只會傳回該服務的實例。 | 未使用。 | 
| <strong>lpVersion</strong> | 未使用。 | 未使用。 | 
| <strong>lpszComment</strong> | 未使用。 | 服務的描述，從藍牙 ServiceDescription SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。 如果指定 <strong>LUP_RETURN_COMMENT</strong> ，則傳回。 | 
| <strong>dwNameSpace</strong> | 必須是 NS_BTH。 | 傳回 NS_BTH。 | 
| <strong>lpNSProviderId</strong> | 未使用。 | 未使用。 | 
| <strong>lpszCoNtext</strong> | 必要。 用來建立 SDP 連接和查詢服務的藍牙裝置位址。 這個值必須是使用 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> 函式呼叫來轉換的字串。 如果提供本機藍牙的裝置位址，則會搜尋本機的 SDP 資料庫。 | 未使用。 | 
| <strong>dwNumberOfProtocols</strong> | 未使用。 | 未使用。 | 
| <strong>lpafpProtocols</strong> | 未使用。 | 未使用。 | 
| <strong>lpszQueryString</strong> | 未使用。 | 未使用。 | 
| <strong>dwNumberOfCsAddrs</strong> | 未使用。 | 指出 <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> 結構陣列中的元素數目。 | 
| <strong>lpcsaBuffer</strong> | 未使用。 | <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a>結構的指標，其<strong>LocalAddr. lpSockaddr</strong>成員指向包含遠端服務完整可連接位址的<a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> ，並從藍牙 ProtocolDescriptorList SDP 屬性的第一個專案轉換。 如果指定 <strong>LUP_RETURN_ADDR</strong> ，則傳回。 | 
| <strong>lpBlob</strong> | 選擇性。 <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a>結構的指標，其中包含用來限制搜尋結果的 advanced 參數。 如果有提供， <strong>lpServiceClassId</strong> 會被忽略，且快取的查詢不會成功。 | <ul><li>如果執行服務搜尋：指向傳回服務控制碼之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。  (<strong>BLOB. cbSize</strong>) /<strong>sizeof</strong> (ULONG) 會計算控制碼的數目。 <strong>PBlobData</strong> 是 ULONG 值的陣列，代表服務控制碼。</li><li>如果執行屬性或 serviceAttribute 搜尋：指向會傳回二進位 SDP 記錄之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。 <strong>CbSize</strong> 是二進位 SDP 記錄的大小。 <strong>PBlobData</strong> 會指向記錄本身。 在許多情況下，二進位 SDP 記錄是必要的，因為只有有限數量的 SDP 屬性可以轉換成 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> 結構，而且只會轉換預設編碼的 utf-8 字串。 <a href="bluetooth-reference.md">藍牙參考</a>一節中提供協助剖析二進位 SDP 記錄的功能。</li><li>如果指定 LUP_RETURN_BLOB，則傳回。</li></ul> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定服務的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[裝置查詢的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[藍牙和 BLOB](bluetooth-and-blob.md)
</dt> <dt>

[藍牙和 WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

藍牙和 WSALookupServiceNext
</dt> <dt>

[藍牙參考](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**CSADDR \_ 資訊**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
