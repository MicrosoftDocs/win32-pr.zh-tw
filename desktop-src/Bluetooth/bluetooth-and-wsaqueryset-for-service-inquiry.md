---
title: 用於服務查詢的藍牙和 WSAQUERYSET
description: 使用 WSAQUERYSET 結構搭配 WSALookupServiceBegin 和 WSALookupServiceNext 函式，以取得服務查詢程式的相關資訊。
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- 藍牙與 WSAQUERYSET for 服務查詢藍牙
- WSAQUERYSET 藍牙，適用于服務查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683583"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>用於服務查詢的藍牙和 WSAQUERYSET

藍牙使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構搭配各種功能，協助您探索藍牙命名空間（NS BTH）中的裝置和服務 \_ 。

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)和 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數會使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構來取得服務查詢程式的相關資料。 下表描述如何針對此目的設定 **WSAQUERYSET** 結構中的成員值。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>成員</th>
<th>WSALookupServiceBegin 的輸入</th>
<th>從 WSALookupServiceNext 傳回的值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>必須設定為 <strong>sizeof</strong> (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</td>
<td><strong>sizeof</strong> (系統傳回的 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>未使用。</td>
<td>服務的顯示名稱，已從藍牙 ServiceName SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。 如果指定 LUP_RETURN_NAME，則傳回。</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>必要。 針對正在進行搜尋的服務，最特定的單一藍牙 UUID。 例如，如果此值設定為 L2CAP 通訊協定的 UUID，它會傳回在目標裝置上使用 L2CAP 通訊協定的所有服務。 如果設定為特定服務的 UUID，則只會傳回該服務的實例。</td>
<td>未使用。</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>未使用。</td>
<td>服務的描述，從 Bluetooth ServiceDescription SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。 如果指定 <strong>LUP_RETURN_COMMENT</strong> ，則傳回。</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>必須是 NS_BTH。</td>
<td>傳回 NS_BTH。</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="odd">
<td><strong>lpszCoNtext</strong></td>
<td>必要。 用來建立 SDP 連接和查詢服務的藍牙裝置位址。 這個值必須是使用 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> 函式呼叫來轉換的字串。 如果提供本機 Bluetooth 裝置位址，則會搜尋本機的 SDP 資料庫。</td>
<td>未使用。</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>未使用。</td>
<td>未使用。</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>未使用。</td>
<td>指出 <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> 結構陣列中的元素數目。</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>未使用。</td>
<td><a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a>結構的指標，其<strong>LocalAddr. lpSockaddr</strong>成員指向包含遠端服務完整可連接位址的<a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> ，並從藍牙 ProtocolDescriptorList SDP 屬性的第一個專案轉換。 如果指定 <strong>LUP_RETURN_ADDR</strong> ，則傳回。</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>選擇性。 <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a>結構的指標，其中包含用來限制搜尋結果的 advanced 參數。 如果有提供， <strong>lpServiceClassId</strong> 會被忽略，且快取的查詢不會成功。</td>
<td><ul>
<li>如果執行服務搜尋：指向傳回服務控制碼之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。  (<strong>BLOB. cbSize</strong>) /<strong>sizeof</strong> (ULONG) 會計算控制碼的數目。 <strong>PBlobData</strong> 是 ULONG 值的陣列，代表服務控制碼。</li>
<li>如果執行屬性或 serviceAttribute 搜尋：指向會傳回二進位 SDP 記錄之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。 <strong>CbSize</strong> 是二進位 SDP 記錄的大小。 <strong>PBlobData</strong> 會指向記錄本身。 在許多情況下，二進位 SDP 記錄是必要的，因為只有有限數量的 SDP 屬性可以轉換成 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> 結構，而且只會轉換預設編碼的 utf-8 字串。 在 [ <a href="bluetooth-reference.md">藍牙參考</a> ] 區段中，會提供協助剖析二進位 SDP 記錄的功能。</li>
<li>如果指定 LUP_RETURN_BLOB，則傳回。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于設定服務的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[適用于裝置查詢的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[藍牙和 BLOB](bluetooth-and-blob.md)
</dt> <dt>

[藍牙和 WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

藍牙和 WSALookupServiceNext
</dt> <dt>

[藍牙參考](bluetooth-reference.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
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

 

 