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
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="a7359-105">用於服務查詢的藍牙和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="a7359-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="a7359-106">藍牙使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構搭配各種功能，協助您探索藍牙命名空間（NS BTH）中的裝置和服務 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a7359-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="a7359-107">[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)和 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數會使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構來取得服務查詢程式的相關資料。</span><span class="sxs-lookup"><span data-stu-id="a7359-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="a7359-108">下表描述如何針對此目的設定 **WSAQUERYSET** 結構中的成員值。</span><span class="sxs-lookup"><span data-stu-id="a7359-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7359-109">成員</span><span class="sxs-lookup"><span data-stu-id="a7359-109">Member</span></span></th>
<th><span data-ttu-id="a7359-110">WSALookupServiceBegin 的輸入</span><span class="sxs-lookup"><span data-stu-id="a7359-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="a7359-111">從 WSALookupServiceNext 傳回的值</span><span class="sxs-lookup"><span data-stu-id="a7359-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7359-112"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="a7359-113">必須設定為 <strong>sizeof</strong> (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="a7359-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="a7359-114"><strong>sizeof</strong> (系統傳回的 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="a7359-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-115"><strong>dwOutputFlags</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="a7359-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-116">Not used.</span></span></td>
<td><span data-ttu-id="a7359-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-118"><strong>lpszServiceInstanceName</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="a7359-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-119">Not used.</span></span></td>
<td><span data-ttu-id="a7359-120">服務的顯示名稱，已從藍牙 ServiceName SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="a7359-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="a7359-121">如果指定 LUP_RETURN_NAME，則傳回。</span><span class="sxs-lookup"><span data-stu-id="a7359-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-122"><strong>lpServiceClassId</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="a7359-123">必要。</span><span class="sxs-lookup"><span data-stu-id="a7359-123">Required.</span></span> <span data-ttu-id="a7359-124">針對正在進行搜尋的服務，最特定的單一藍牙 UUID。</span><span class="sxs-lookup"><span data-stu-id="a7359-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="a7359-125">例如，如果此值設定為 L2CAP 通訊協定的 UUID，它會傳回在目標裝置上使用 L2CAP 通訊協定的所有服務。</span><span class="sxs-lookup"><span data-stu-id="a7359-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="a7359-126">如果設定為特定服務的 UUID，則只會傳回該服務的實例。</span><span class="sxs-lookup"><span data-stu-id="a7359-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="a7359-127">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-128"><strong>lpVersion</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="a7359-129">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-129">Not used.</span></span></td>
<td><span data-ttu-id="a7359-130">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-131"><strong>lpszComment</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="a7359-132">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-132">Not used.</span></span></td>
<td><span data-ttu-id="a7359-133">服務的描述，從 Bluetooth ServiceDescription SDP 屬性的預設語言編碼轉換為 UTF-8 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="a7359-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="a7359-134">如果指定 <strong>LUP_RETURN_COMMENT</strong> ，則傳回。</span><span class="sxs-lookup"><span data-stu-id="a7359-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-135"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="a7359-136">必須是 NS_BTH。</span><span class="sxs-lookup"><span data-stu-id="a7359-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="a7359-137">傳回 NS_BTH。</span><span class="sxs-lookup"><span data-stu-id="a7359-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-138"><strong>lpNSProviderId</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="a7359-139">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-139">Not used.</span></span></td>
<td><span data-ttu-id="a7359-140">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-141"><strong>lpszCoNtext</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="a7359-142">必要。</span><span class="sxs-lookup"><span data-stu-id="a7359-142">Required.</span></span> <span data-ttu-id="a7359-143">用來建立 SDP 連接和查詢服務的藍牙裝置位址。</span><span class="sxs-lookup"><span data-stu-id="a7359-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="a7359-144">這個值必須是使用 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> 函式呼叫來轉換的字串。</span><span class="sxs-lookup"><span data-stu-id="a7359-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="a7359-145">如果提供本機 Bluetooth 裝置位址，則會搜尋本機的 SDP 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a7359-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="a7359-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-147"><strong>dwNumberOfProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="a7359-148">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-148">Not used.</span></span></td>
<td><span data-ttu-id="a7359-149">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-150"><strong>lpafpProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="a7359-151">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-151">Not used.</span></span></td>
<td><span data-ttu-id="a7359-152">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-153"><strong>lpszQueryString</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="a7359-154">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-154">Not used.</span></span></td>
<td><span data-ttu-id="a7359-155">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-156"><strong>dwNumberOfCsAddrs</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="a7359-157">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-157">Not used.</span></span></td>
<td><span data-ttu-id="a7359-158">指出 <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> 結構陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a7359-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7359-159"><strong>lpcsaBuffer</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="a7359-160">未使用。</span><span class="sxs-lookup"><span data-stu-id="a7359-160">Not used.</span></span></td>
<td><span data-ttu-id="a7359-161"><a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a>結構的指標，其<strong>LocalAddr. lpSockaddr</strong>成員指向包含遠端服務完整可連接位址的<a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> ，並從藍牙 ProtocolDescriptorList SDP 屬性的第一個專案轉換。</span><span class="sxs-lookup"><span data-stu-id="a7359-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="a7359-162">如果指定 <strong>LUP_RETURN_ADDR</strong> ，則傳回。</span><span class="sxs-lookup"><span data-stu-id="a7359-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7359-163"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="a7359-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="a7359-164">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a7359-164">Optional.</span></span> <span data-ttu-id="a7359-165"><a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a>結構的指標，其中包含用來限制搜尋結果的 advanced 參數。</span><span class="sxs-lookup"><span data-stu-id="a7359-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="a7359-166">如果有提供， <strong>lpServiceClassId</strong> 會被忽略，且快取的查詢不會成功。</span><span class="sxs-lookup"><span data-stu-id="a7359-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="a7359-167">如果執行服務搜尋：指向傳回服務控制碼之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a7359-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="a7359-168"> (<strong>BLOB. cbSize</strong>) /<strong>sizeof</strong> (ULONG) 會計算控制碼的數目。</span><span class="sxs-lookup"><span data-stu-id="a7359-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="a7359-169"><strong>PBlobData</strong> 是 ULONG 值的陣列，代表服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7359-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="a7359-170">如果執行屬性或 serviceAttribute 搜尋：指向會傳回二進位 SDP 記錄之 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a7359-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="a7359-171"><strong>CbSize</strong> 是二進位 SDP 記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="a7359-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="a7359-172"><strong>PBlobData</strong> 會指向記錄本身。</span><span class="sxs-lookup"><span data-stu-id="a7359-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="a7359-173">在許多情況下，二進位 SDP 記錄是必要的，因為只有有限數量的 SDP 屬性可以轉換成 <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> 結構，而且只會轉換預設編碼的 utf-8 字串。</span><span class="sxs-lookup"><span data-stu-id="a7359-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="a7359-174">在 [ <a href="bluetooth-reference.md">藍牙參考</a> ] 區段中，會提供協助剖析二進位 SDP 記錄的功能。</span><span class="sxs-lookup"><span data-stu-id="a7359-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="a7359-175">如果指定 LUP_RETURN_BLOB，則傳回。</span><span class="sxs-lookup"><span data-stu-id="a7359-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a7359-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7359-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7359-177">適用于設定服務的藍牙和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="a7359-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="a7359-178">適用于裝置查詢的藍牙和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="a7359-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="a7359-179">藍牙和 BLOB</span><span class="sxs-lookup"><span data-stu-id="a7359-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="a7359-180">藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="a7359-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="a7359-181">藍牙和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="a7359-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="a7359-182">藍牙參考</span><span class="sxs-lookup"><span data-stu-id="a7359-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="a7359-183">**Blob**</span><span class="sxs-lookup"><span data-stu-id="a7359-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="a7359-184">**BTH \_ 查詢 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a7359-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="a7359-185">**CSADDR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a7359-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="a7359-186">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="a7359-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="a7359-187">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="a7359-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="a7359-188">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="a7359-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="a7359-189">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a7359-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 