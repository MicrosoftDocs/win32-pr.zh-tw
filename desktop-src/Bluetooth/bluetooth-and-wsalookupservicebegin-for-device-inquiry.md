---
title: 適用于裝置查詢的藍牙和 WSALookupServiceBegin
description: 本主題說明如何使用 WSALookupServiceBegin 函式來執行可見和幻影裝置的查詢。 如需詳細資訊，請參閱探索藍牙裝置和服務。
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- 適用于裝置的藍牙與 WSALookupServiceBegin 查詢藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104093432"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="3fa26-105">適用于裝置查詢的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="3fa26-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="3fa26-106">本主題說明如何使用 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 函式來執行可見和幻影裝置的查詢。</span><span class="sxs-lookup"><span data-stu-id="3fa26-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="3fa26-107">如需詳細資訊，請參閱 [探索藍牙裝置和服務](discovering-bluetooth-devices-and-services.md)。</span><span class="sxs-lookup"><span data-stu-id="3fa26-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="3fa26-108">[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式會在其第一個參數（ *lpqsRestrictions*）中使用 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構，以定義搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="3fa26-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="3fa26-109">藍牙提供使用 **WSALookupServiceBegin** 函式和 **WSAQUERYSET** 的特定指導方針。</span><span class="sxs-lookup"><span data-stu-id="3fa26-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="3fa26-110">下表列出在查詢裝置時，套用至傳遞給 *lpqsRestrictions* 參數之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的限制。</span><span class="sxs-lookup"><span data-stu-id="3fa26-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fa26-111">WSAQUERYSET 成員</span><span class="sxs-lookup"><span data-stu-id="3fa26-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="3fa26-112">限制</span><span class="sxs-lookup"><span data-stu-id="3fa26-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3fa26-113"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="3fa26-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="3fa26-114">設定為 <strong>sizeof</strong> (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="3fa26-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fa26-115"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="3fa26-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="3fa26-116">此成員包含 <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> 結構的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="3fa26-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="3fa26-117">如果指定了這個成員， <strong>LUP_FLUSHCACHE</strong> 的有效裝置查詢參數如下所示：</span><span class="sxs-lookup"><span data-stu-id="3fa26-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="3fa26-118"><a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a>結構的<strong>cbSize</strong>成員必須是<strong>sizeof</strong> (<strong>BTH_QUERY_DEVICE</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="3fa26-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="3fa26-119"><strong>PBlobData</strong>成員是<a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a>結構的指標，其<strong>膝上</strong>成員為藍牙查詢存取碼，而<strong>長度</strong>成員是查詢的長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fa26-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fa26-120"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="3fa26-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="3fa26-121">設定為 <strong>NS_BTH</strong>。</span><span class="sxs-lookup"><span data-stu-id="3fa26-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fa26-122">其他成員</span><span class="sxs-lookup"><span data-stu-id="3fa26-122">Other members</span></span></td>
<td><span data-ttu-id="3fa26-123"><a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>結構的其他成員則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="3fa26-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3fa26-124">下表中所列的旗標是在 *dwControlFlags* 參數中用來控制查詢結果。</span><span class="sxs-lookup"><span data-stu-id="3fa26-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="3fa26-125">[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式會使用 **LUP \_ 容器** 和 **LUP \_ FLUSHCACHE** 旗標; 其餘的旗標會用於 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函數的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="3fa26-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="3fa26-126">旗標</span><span class="sxs-lookup"><span data-stu-id="3fa26-126">Flag</span></span>               | <span data-ttu-id="3fa26-127">結果</span><span class="sxs-lookup"><span data-stu-id="3fa26-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa26-128">LUP \_ 容器</span><span class="sxs-lookup"><span data-stu-id="3fa26-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="3fa26-129">指定查詢用途是取得藍牙裝置清單，而不是服務清單。</span><span class="sxs-lookup"><span data-stu-id="3fa26-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="3fa26-130">必須設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="3fa26-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3fa26-131">LUP \_ FLUSHCACHE</span><span class="sxs-lookup"><span data-stu-id="3fa26-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="3fa26-132">觸發本機裝置的查詢，或導致傳回先前查詢的快取結果。</span><span class="sxs-lookup"><span data-stu-id="3fa26-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3fa26-133">LUP \_ 傳回 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="3fa26-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="3fa26-134">直接在 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpServiceClassId** 成員中，傳回裝置位的 Bluetooth (類別) 。</span><span class="sxs-lookup"><span data-stu-id="3fa26-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="3fa26-135">此貨會對應到 GUID 的 **Data1** 成員。</span><span class="sxs-lookup"><span data-stu-id="3fa26-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="3fa26-136">LUP \_ RES \_ 服務</span><span class="sxs-lookup"><span data-stu-id="3fa26-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="3fa26-137">傳回本機藍牙位址的資訊。</span><span class="sxs-lookup"><span data-stu-id="3fa26-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="3fa26-138">只有在同時指定 **LUP 傳回 \_ \_ 位址** 時，此旗標才會有作用。</span><span class="sxs-lookup"><span data-stu-id="3fa26-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3fa26-139">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="3fa26-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="3fa26-140">針對每個 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式的呼叫，傳回 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構之 **lpszServiceInstanceName** 成員中裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3fa26-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="3fa26-141">指定 **LUP 傳回 \_ \_ BLOB** 旗標時，也必須指定此旗標，以抓取 [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)結構的 **名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="3fa26-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="3fa26-142">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="3fa26-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="3fa26-143">傳回 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構，其中包含每個 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式呼叫之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpcsaBuffer** 成員中，對等的48位位址。</span><span class="sxs-lookup"><span data-stu-id="3fa26-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="3fa26-144">**SOCKADDR \_ BTH** 結構中的其他成員將會是空的。</span><span class="sxs-lookup"><span data-stu-id="3fa26-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="3fa26-145">LUP \_ 傳回 \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="3fa26-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="3fa26-146">在每次對 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)的後續呼叫上，傳回 [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)結構。</span><span class="sxs-lookup"><span data-stu-id="3fa26-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3fa26-147">LUP \_ FLUSHPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="3fa26-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="3fa26-148">略過下一個可用的裝置，並傳回其後的裝置。</span><span class="sxs-lookup"><span data-stu-id="3fa26-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="3fa26-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fa26-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fa26-150">適用于服務探索的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="3fa26-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="3fa26-151">藍牙和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="3fa26-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="3fa26-152">適用于裝置查詢的藍牙和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="3fa26-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="3fa26-153">探索藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="3fa26-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="3fa26-154">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="3fa26-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="3fa26-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="3fa26-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="3fa26-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="3fa26-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="3fa26-157">**Blob**</span><span class="sxs-lookup"><span data-stu-id="3fa26-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="3fa26-158">**BTH \_ 查詢 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="3fa26-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="3fa26-159">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="3fa26-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="3fa26-160">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="3fa26-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="3fa26-161">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="3fa26-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 