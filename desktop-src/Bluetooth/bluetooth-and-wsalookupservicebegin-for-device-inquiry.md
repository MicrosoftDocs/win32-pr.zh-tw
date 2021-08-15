---
title: 裝置查詢的藍牙和 WSALookupServiceBegin
description: 本主題說明如何使用 WSALookupServiceBegin 函式來執行可見和幻影裝置的查詢。 如需詳細資訊，請參閱探索藍牙的裝置和服務。
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- 裝置查詢藍牙的藍牙和 WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af56e1d75a66d21ea4eb94c827f6d37f77ae4336b8aeac5331665288bfeef49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959287"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>裝置查詢的藍牙和 WSALookupServiceBegin

本主題說明如何使用 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 函式來執行可見和幻影裝置的查詢。 如需詳細資訊，請參閱[探索藍牙的裝置和服務](discovering-bluetooth-devices-and-services.md)。

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式會在其第一個參數（ *lpqsRestrictions*）中使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構，以定義搜尋準則。 藍牙提供使用 **WSALookupServiceBegin** 函式和 **WSAQUERYSET** 的特定指導方針。

下表列出在查詢裝置時，套用至傳遞給 *lpqsRestrictions* 參數之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的限制。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>WSAQUERYSET 成員</th>
<th>限制</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>設定為 <strong>sizeof</strong> (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>此成員包含 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的選擇性指標。 如果指定了這個成員， <strong>LUP_FLUSHCACHE</strong> 的有效裝置查詢參數如下所示：
<ul>
<li><a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a>結構的<strong>cbSize</strong>成員必須是<strong>sizeof</strong> (<strong>BTH_QUERY_DEVICE</strong>) 。</li>
<li><strong>PBlobData</strong>成員是<a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a>結構的指標，其中<strong>膝上</strong>成員是藍牙查詢存取碼，而<strong>長度</strong>成員是查詢的長度（以秒為單位）。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>設定為 <strong>NS_BTH</strong>。</td>
</tr>
<tr class="even">
<td>其他成員</td>
<td><a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>結構的其他成員則會被忽略。</td>
</tr>
</tbody>
</table>



 

下表中所列的旗標是在 *dwControlFlags* 參數中用來控制查詢結果。 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式會使用 **LUP \_ 容器** 和 **LUP \_ FLUSHCACHE** 旗標; 其餘的旗標會用於 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數的呼叫中。

| 旗標               | 結果                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 容器    | 指定查詢用途是取得藍牙的裝置清單，而不是服務清單。 必須設定這個旗標。                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | 觸發本機裝置的查詢，或導致傳回先前查詢的快取結果。                                                                                                                                                                                                                                                                                                                |
| LUP \_ 傳回 \_ 類型  | 直接在 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpServiceClassId** 成員中，傳回裝置位的藍牙的 (類別類別) 。 此貨會對應到 GUID 的 **Data1** 成員。                                                                                                                                                                                                      |
| LUP \_ RES \_ 服務  | 傳回本機藍牙位址的資訊。 只有在同時指定 **LUP 傳回 \_ \_ 位址** 時，此旗標才會有作用。                                                                                                                                                                                                                                                                                       |
| LUP \_ 傳回 \_ 名稱  | 針對每個 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式的呼叫，傳回 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構之 **lpszServiceInstanceName** 成員中裝置的顯示名稱。 指定 **LUP 傳回 \_ \_ BLOB** 旗標時，也必須指定此旗標，以抓取 [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)結構的 **名稱** 成員。 |
| LUP \_ 傳回 \_ 位址  | 傳回 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構，其中包含每個 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式呼叫之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpcsaBuffer** 成員中，對等的48位位址。 **SOCKADDR \_ BTH** 結構中的其他成員將會是空的。                                                            |
| LUP \_ 傳回 \_ BLOB  | 在每次對 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)的後續呼叫上，傳回 [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)結構。                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | 略過下一個可用的裝置，並傳回其後的裝置。                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務探索藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[藍牙和 WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[裝置查詢的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 