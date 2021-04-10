---
title: 適用于服務探索的藍牙和 WSALookupServiceBegin
description: 用戶端會使用 WSALookupServiceBegin、WSALookupServiceNext 和 WSALookupServiceEnd 功能，來探索藍牙伺服器上的特定服務是否存在。
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- 藍牙與 WSALookupServiceBegin for Service Discovery 藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842835"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>適用于服務探索的藍牙和 WSALookupServiceBegin

用戶端會使用 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)和 [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) 功能，來探索藍牙伺服器上的特定服務是否存在。 您可以針對本機和遠端位址執行查詢，但只能與遠端位址建立連接。 在此作業期間探索到的服務控制碼，無法透過 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)來刪除服務。 RFCOMM 不支援回送。

您可以執行兩種基本類型的服務探索查詢：

-   查詢本機裝置上的一或多個服務
-   查詢指定的對等裝置上的一或多個服務

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函數會在其 *lpqsRestrictions* 參數中收到 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構。 **WSALookupServiceBegin** 會根據 **WSAQUERYSET** 包含的一組搜尋限制來執行用戶端查詢。 當使用 **WSALookupServiceBegin** 函數來查詢服務時，藍牙用戶端必須在 **WSAQUERYSET** 結構中指定下表所列的限制。



| WSAQUERYSET 成員    | 限制                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | 設定為 **sizeof** ([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) 。                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | 設定為可用於判斷查詢範圍的最特定藍牙 UUID。 例如，將 **lpServiceClassId** 設定為 L2CAP 通訊協定的 UUID 會導致所有傳回的 L2CAP 服務，基本上會列舉目標上的所有 SD 記錄。 但是，將 UUID 設定為特定服務，只會傳回該服務的實例。<br/> |
| **dwNameSpace**       | 設定為 **NS \_ BTH**。                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | 設定為0。                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszCoNtext**       | 設定為要用來建立用來執行服務查詢之 SDP 連接的藍牙裝置位址。 此成員必須是使用 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) 函數進行轉換的字串。 如果提供了本機無線電位址，則會搜尋本機的 SDP 記錄。<br/>                                             |
| 其他成員         | [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的所有其他成員都會被忽略。                                                                                                                                                                                                                                                                                        |



 

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式完成服務查詢之後，與遠端裝置的 SDP 連接不會保持作用中狀態;連接會在 **WSALookupServiceBegin** 傳回之前終止。 在服務查詢完成之後，需要 SDP 連線才能保持使用中的應用程式，應該在發出 Windows Socket [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函數呼叫時，使用 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構的 **serviceClassId** 成員來指定要連接的服務類別 UUID。

下表所列的旗標，用於 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)和 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數的 *dwControlFlags* 參數，以控制查詢結果。 **WSALookupServiceBegin** 函式會使用 **LUP \_ 容器** 和 **LUP \_ FLUSHCACHE** 旗標; 其餘的旗標會用於 **WSALookupServiceNext** 函數的呼叫中。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>旗標</th>
<th>結果</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>不得設定。</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>應用程式通常應該指定 <strong>LUP_FLUSHCACHE</strong>。 此旗標會指示系統忽略任何快取的資訊，並建立與指定裝置的無線 SDP 連線，以執行 SDP 搜尋。 這種非快取的作業可能需要幾秒鐘的時間 (而快取的搜尋會迅速傳回) 。 藍牙目前不會主動快取來自鄰近裝置的 SDP 記錄，也不會主動快取先前的查詢。 因此，如果未指定<strong>LUP_FLUSHCACHE</strong> ，應用程式應該預期查詢可能不會傳回任何結果 (錯誤碼為<strong>WSASERVICE_NOT_FOUND</strong>) 。 使用 Windows 通訊端介面所提供的快取資料可能會在未來增強。</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>傳回本機藍牙位址的相關資訊。 只有在同時指定 <strong>LUP_RETURN_ADDR</strong> 時，此旗標才會有作用。</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>針對每個<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>函數的呼叫，傳回<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>結構之<strong>lpszServiceInstanceName</strong>成員中的服務顯示名稱。</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>傳回<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>結構之<strong>lpServiceClassId</strong>成員中的服務類別識別碼。
<blockquote>
[!Note]<br />
此旗標的使用只適用于 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>WSALookupServiceBegin</strong></a> 函數。 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>的這個值一律為零。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>傳回 <strong>lpcsaBuffer</strong> 成員中要搭配 <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>連接</strong></a> 函式呼叫使用的位址。 傳回的位址包含埠號碼。</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>傳回 <strong>lpBlob</strong> 成員中相符的 SD 記錄，並根據藍牙 SDP 記錄規格進行格式化。</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>傳回上述所有旗標的資訊。</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>針對每個<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>函式呼叫，傳回<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>結構之<strong>lpszComment</strong>成員中的服務描述。</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>略過下一個可用的記錄，然後傳回其後的記錄。</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Advanced Services 查詢

上一節所描述的查詢作業可以用來傳回單一 GUID 的所有結果，這對大部分的應用程式而言都是足夠的。 Advanced query 可讓應用程式建立更明確的查詢;它提供在傳回的資訊中比對 Uuid 和屬性的功能。

若要執行服務的 advanced query，藍牙用戶端必須在傳遞至 *lpqsRestrictions* 參數的 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構中指定下列限制。



| WSAQUERYSET 成員   | 限制                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | 設定為 **sizeof** ([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) 。                                                                                                                                                                                                                                                                        |
| **lpszCoNtext**      | 設定為要用來建立用來執行服務查詢之 SDP 連接的藍牙裝置位址。 此成員必須是使用 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) 函數進行轉換的字串。 如果提供了本機無線電位址，則會搜尋本機的 SDP 記錄。<br/> |
| **lpBlob.pBlobData** | [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構的指標，其中包含所有限制查詢結果的參數。                                                                                                                                                                                           |
| **dwNameSpace**      | 設定為 **NS \_ BTH**。                                                                                                                                                                                                                                                                                                                 |
| 其他成員        | [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的所有其他成員都會被忽略。                                                                                                                                                                                                                                            |



 

下列旗標會在 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)的 *dwControlFlags* 參數中傳遞，以控制 advanced 查詢的結果。

| 旗標                     | 結果                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **LUP \_ 容器**      | 不得設定。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | 應用程式通常應該會指定 **LUP \_ FLUSHCACHE**。 此旗標會指示系統忽略任何快取的資訊，並建立與指定裝置的無線 SDP 連線，以執行 SDP 搜尋。 這種非快取的作業可能需要幾秒鐘的時間 (而快取的搜尋會迅速傳回) 。 藍牙不會主動快取鄰近裝置的 SDP 記錄，也不會積極快取先前的查詢。 因此，如果未指定 **LUP \_ FLUSHCACHE** ，應用程式應該會預期查詢可能會頻繁地傳回結果， (找 **\_ 不 \_ 到 WSASERVICE**) 。 使用 Windows 通訊端介面所提供的快取資料可能會在未來增強。 |
| **LUP \_ RES \_ 服務**    | 傳回本機藍牙位址的資訊。 只有在同時指定 **LUP 傳回 \_ \_ ADDRR** 時，才會設定這個旗標的效果。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **LUP \_ 傳回 \_ 名稱**    | 傳回服務的顯示名稱。 針對 **SDP \_ 服務 \_ 搜尋 \_ 要求**，會忽略此旗標。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **LUP \_ 傳回 \_ 類型**    | 傳回服務類別識別碼。 針對 **SDP \_ 服務 \_ 搜尋 \_ 要求**，會忽略此旗標。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ 傳回 \_ 位址**    | 傳回 **lpcsaBuffer** 成員中要搭配 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式呼叫使用的位址。 傳回的位址包含埠號碼。 針對 **SDP \_ 服務 \_ 搜尋 \_ 要求**，會忽略此旗標。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **LUP \_ 傳回 \_ BLOB**    | 以符合藍牙 SDP 記錄規格的格式傳回相符的 SD 記錄。 針對 **SDP \_ 服務 \_ 搜尋 \_ 要求**，後續呼叫 [**WSALOOKUPSERVICENEXT**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)的 **lpBlob** 結果是藍牙 SDP 控點的陣列。 針對 **sdp \_ 服務 \_ 屬性 \_ 要求** 和 **sdp \_ 服務 \_ 搜尋 \_ 屬性 \_ 要求**，每個後續呼叫 **WSALookupServiceNext** 的結果都是二進位 Bluetooth SDP 記錄，其屬性會限制為查詢的 **pRange** 成員所指定的屬性。 此旗標是 **SDP \_ 服務 \_ 搜尋 \_ 要求** 的必要項。                                                               |
| **LUP \_ 傳回 \_ 批註** | 針對每個 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式呼叫，傳回 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構之 **lpszComment** 成員中的服務描述。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | 略過下一個可用的記錄，然後傳回其後的記錄。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

在輸入時， **lpBlob** -> **pBlobData** 會指向 [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構，其中包含下表所列的值。

> [!Note]  
> 初始搜尋要求必須能夠符合一個 L2CAP 封包。 不過，回應可能會分成許多 L2CAP 封包。

 



| 成員            | 值                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | 要執行的搜尋類型。 此值可以是 **sdp \_ 服務 \_ 搜尋 \_ 要求**、 **sdp \_ 服務 \_ 屬性 \_ 要求** 或 **sdp \_ 服務 \_ 搜尋 \_ 屬性 \_ 要求** 的其中一個。 每種搜尋類型都與藍牙 SDP 規格所定義的基礎搜尋機制相關聯。 每個傳回的結果都是 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構所描述的表單，這是稍早在此 (Advanced services 查詢) 一節中所定義。 |
| **serviceHandle** | 用於屬性搜尋。 這個值會指定用來查詢 **pRange** 成員中屬性的服務控制碼。                                                                                                                                                                                                                                                                                                                                            |
| **uuid**         | 用於服務和 **serviceAttribute** 搜尋。 此值指定記錄必須包含以符合搜尋的 Uuid。 如果要查詢 **\_ 查詢 uuid \_ 中 \_ 的最大 uuid** ，此值會將緊接在最後一個有效 UUID 之後的 SdpQueryUuid 元素設定為全部零。                                                                                                                                                                       |
| **numRange**      | 用於屬性和 **serviceAttribute** 搜尋。 這個值會指定 **pRange** 中的元素數目。                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | 用於屬性和 **serviceAttribute** 搜尋。 此值會指定要針對任何相符記錄取得的屬性值。                                                                                                                                                                                                                                                                                                                                        |



 

在每次成功呼叫 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數之後， **lpBlob** -> **pBlobData** 會指向包含下表所列值的資料區塊。

| 值                                                                                | 描述                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SDP \_ 服務 \_ 搜尋 \_ 要求**                                                    | SDP 記錄控制碼的陣列，與藍牙 1.1 SDP 4.5.2 所定義的 **ServiceRecordHandleList** 相同。 傳回的 SDP 控制碼數目是由 (**lpBlob**->cbSize) /**sizeof** (ULONG) 所計算。 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式的單一呼叫會傳回所有結果。 |
| **SDP \_服務 \_ 屬性 \_ 要求** 或 **SDP \_ 服務 \_ 搜尋 \_ 屬性 \_ 要求** | 二進位 Bluetooth SDP 記錄。 針對 **SDP \_ 服務 \_ 屬性 \_ 要求**， [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) 函式的單一呼叫會傳回所有結果。                                                                                                                                                       |



 

> [!Note]  
> 如果未在服務查詢的輸入期間指定 **lpBlob** 成員，就會針對 **lpServiceClassId** 成員中指定的服務，執行從0到0xffff 的屬性的服務和屬性搜尋。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用於服務查詢的藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[藍牙和 WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[適用于裝置查詢的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**連線**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
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

