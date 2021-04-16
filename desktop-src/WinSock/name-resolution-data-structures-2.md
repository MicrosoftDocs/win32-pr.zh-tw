---
description: Windows 通訊端中的名稱解析資料結構 (Winsock) 。
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: 名稱解析資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1f76607ade81503a1057dc21890ac38d5ec265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571493"
---
# <a name="name-resolution-data-structures"></a><span data-ttu-id="243e2-103">名稱解析資料結構</span><span class="sxs-lookup"><span data-stu-id="243e2-103">Name Resolution Data Structures</span></span>

<span data-ttu-id="243e2-104">在名稱解析函式中，有數個重要的資料結構廣泛使用。</span><span class="sxs-lookup"><span data-stu-id="243e2-104">There are several important data structures that are used extensively throughout the name resolution functions.</span></span>

## <a name="query-related-data-structures"></a><span data-ttu-id="243e2-105">Query-Related 資料結構</span><span class="sxs-lookup"><span data-stu-id="243e2-105">Query-Related Data Structures</span></span>

<span data-ttu-id="243e2-106">[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構是用來形成 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)的查詢，用來傳遞 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)的查詢結果。</span><span class="sxs-lookup"><span data-stu-id="243e2-106">The [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure is used to form queries for [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), and used to deliver query results for [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="243e2-107">這是複雜的結構，因為它包含多個其他結構的指標，其中有些參考仍是其他結構。</span><span class="sxs-lookup"><span data-stu-id="243e2-107">It is a complex structure since it contains pointers to several other structures, some of which reference still other structures.</span></span> <span data-ttu-id="243e2-108">[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構與其參考結構之間的關聯性如下所示。</span><span class="sxs-lookup"><span data-stu-id="243e2-108">The relationship between the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure and the structures it references is illustrated as follows.</span></span>

![wsaqueryset 與其相關結構之間的關聯性](images/ovrvw3-2.png)

<span data-ttu-id="243e2-110">在 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構內，大部分的成員都是一目了然的，但有一些額外的說明。</span><span class="sxs-lookup"><span data-stu-id="243e2-110">Within the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure, most of the member are self explanatory, but some deserve additional explanation.</span></span> <span data-ttu-id="243e2-111">**DwSize** 成員必須一律填入 Sizeof (**WSAQUERYSET**) ，因為這是由命名空間提供者用來偵測及調整可能會在一段時間內出現的不同 **WSAQUERYSET** 結構版本。</span><span class="sxs-lookup"><span data-stu-id="243e2-111">The **dwSize** member must always be filled in with sizeof(**WSAQUERYSET**), as this is used by namespace providers to detect and adapt to different versions of the **WSAQUERYSET** structure that may appear over time.</span></span>

<span data-ttu-id="243e2-112">命名空間提供者會使用 **dwOutputFlags** 成員來提供查詢結果的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="243e2-112">The **dwOutputFlags** member is used by a namespace provider to provide additional information about query results.</span></span> <span data-ttu-id="243e2-113">如需詳細資訊，請參閱 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="243e2-113">For details, see the [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

<span data-ttu-id="243e2-114">**Lpversion** 成員所參考的 [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)結構會用於查詢準則約束和結果。</span><span class="sxs-lookup"><span data-stu-id="243e2-114">The [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) structure referenced by the **lpversion** member is used for both query constraint and results.</span></span> <span data-ttu-id="243e2-115">若為查詢， **dwVersion** 成員會指出所需的服務版本。</span><span class="sxs-lookup"><span data-stu-id="243e2-115">For queries, the **dwVersion** member indicates the desired version of the service.</span></span> <span data-ttu-id="243e2-116">**EcHow** 成員是列舉型別，可指定如何進行比較。</span><span class="sxs-lookup"><span data-stu-id="243e2-116">The **ecHow** member is an enumerated type which specifies how the comparison can be made.</span></span> <span data-ttu-id="243e2-117">選項為 [複合 \_ EQUALS]，其需要在版本中進行完全相符，或 \_ 指定服務的版本號碼不小於 **dwVersion** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="243e2-117">The choices are COMP\_EQUALS which requires that an exact match in version occurs, or COMP\_NOTLESS which specifies that the service's version number be no less than the value of the **dwVersion** member.</span></span>

<span data-ttu-id="243e2-118">**DwNameSpace** 和 **lpNSProviderId** 的解讀取決於結構的使用方式，並在使用此結構的個別函式描述中進一步說明。</span><span class="sxs-lookup"><span data-stu-id="243e2-118">The interpretation of **dwNameSpace** and **lpNSProviderId** depends upon how the structure is being used and is described further in the individual function descriptions that utilize this structure.</span></span>

<span data-ttu-id="243e2-119">**LpszCoNtext** 成員會套用至階層命名空間，並指定查詢的起點或服務所在階層中的位置。</span><span class="sxs-lookup"><span data-stu-id="243e2-119">The **lpszContext** member applies to hierarchical namespaces, and specifies the starting point of a query or the location within the hierarchy where the service resides.</span></span> <span data-ttu-id="243e2-120">一般規則如下：</span><span class="sxs-lookup"><span data-stu-id="243e2-120">The general rules are:</span></span>

-   <span data-ttu-id="243e2-121">值為 **Null**、空白 ( "" ) 在預設內容中開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="243e2-121">A value of **NULL**, blank ("") starts the search at the default context.</span></span>
-   <span data-ttu-id="243e2-122">"" 的值會 \\ 在命名空間的頂端開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="243e2-122">A value of "\\" starts the search at the top of the namespace.</span></span>
-   <span data-ttu-id="243e2-123">任何其他值都會在指定的點開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="243e2-123">Any other value starts the search at the designated point.</span></span>

<span data-ttu-id="243e2-124">如果指定了 "" 或 "" 以外的任何專案，則不支援內含專案的提供者可能會傳回錯誤 \\ 。</span><span class="sxs-lookup"><span data-stu-id="243e2-124">Providers that do not support containment may return an error if anything other than "" or "\\" is specified.</span></span> <span data-ttu-id="243e2-125">支援有限內含專案的提供者（例如群組）應接受 ""，' \\ "或指定的點。</span><span class="sxs-lookup"><span data-stu-id="243e2-125">Providers that support limited containment, such as groups, should accept "", '\\", or a designated point.</span></span> <span data-ttu-id="243e2-126">內容是特定命名空間。</span><span class="sxs-lookup"><span data-stu-id="243e2-126">Contexts are namespace specific.</span></span> <span data-ttu-id="243e2-127">如果 **dwNameSpace** 成員是 NS \_ ALL，則只應將 "" 或 " \\ " 傳遞為內容，因為所有命名空間都能辨識這些成員。</span><span class="sxs-lookup"><span data-stu-id="243e2-127">If the **dwNameSpace** member is NS\_ALL, then only "" or "\\" should be passed as the context since these are recognized by all namespaces.</span></span>

<span data-ttu-id="243e2-128">**LpszQueryString** 成員是用來提供其他命名空間特定的查詢資訊，例如描述已知服務和傳輸通訊協定名稱的字串，例如 "FTP/TCP"。</span><span class="sxs-lookup"><span data-stu-id="243e2-128">The **lpszQueryString** member is used to supply additional, namespace-specific query information such as a string describing a well-known service and transport protocol name, as in "FTP/TCP".</span></span>

<span data-ttu-id="243e2-129">**LpafpProtocols** 成員所參考的 [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)結構只用于查詢用途，並提供用來限制查詢的通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="243e2-129">The [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) structure referenced by the **lpafpProtocols** member is used for query purposes only, and supplies a list of protocols to constrain the query.</span></span> <span data-ttu-id="243e2-130">這些通訊協定會以 (位址系列、通訊協定) 組表示，因為通訊協定值只有在位址系列的內容中才有意義。</span><span class="sxs-lookup"><span data-stu-id="243e2-130">These protocols are represented as (address family, protocol) pairs, since protocol values only have meaning within the context of an address family.</span></span>

<span data-ttu-id="243e2-131">**LpcsaBuffer** 成員所參考之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的陣列，包含服務在建立接聽時所需的所有資訊，或是用於建立服務連接的用戶端所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="243e2-131">The array of the [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure referenced by the **lpcsaBuffer** member contain all of the information needed for either a service to use in establishing a listen, or for a client to use in establishing a connection to the service.</span></span> <span data-ttu-id="243e2-132">**LocalAddr** 和 **RemoteAddr** 成員都直接包含 [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)結構。</span><span class="sxs-lookup"><span data-stu-id="243e2-132">The **LocalAddr** and **RemoteAddr** members both directly contain a [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) structure.</span></span>

<span data-ttu-id="243e2-133">服務會藉由使用 LocalAddr 的元組（ *lpSockaddr->sa \_ 系列*、 *iSocketType* 和 *iProtocol* 作為參數）呼叫 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式來建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="243e2-133">A service would create a socket by calling the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function using the tuple of *LocalAddr.lpSockaddr->sa\_family*, *iSocketType*, and *iProtocol* as parameters.</span></span> <span data-ttu-id="243e2-134">服務會將通訊端系結至本機位址，方法是使用 *LocalAddr. lpSockaddr* 和 *LocalAddr* 做為參數來呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind)函式。</span><span class="sxs-lookup"><span data-stu-id="243e2-134">A service would bind the socket to a local address by calling the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function using *LocalAddr.lpSockaddr* and *LocalAddr.lpSockaddrLength* as parameters.</span></span>

<span data-ttu-id="243e2-135">用戶端會使用 LocalAddr 的元組（ *lpSockaddr->sa \_ 系列*、 *iSocketType* 和 *iProtocol* 作為參數）來呼叫 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式，以建立其通訊端。</span><span class="sxs-lookup"><span data-stu-id="243e2-135">A client creates its socket by calling the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function using the tuple of *LocalAddr.lpSockaddr->sa\_family*, *iSocketType*, and *iProtocol* as parameters.</span></span> <span data-ttu-id="243e2-136">當使用 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)或 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)函數進行遠端連線時，用戶端會使用 *RemoteAddr. lpSockaddr* 和 *RemoteAddr* 的組合作為參數。</span><span class="sxs-lookup"><span data-stu-id="243e2-136">A client uses the combination of *RemoteAddr.lpSockaddr* and *RemoteAddr.lpSockaddrLength* as parameters when making a remote connection using the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), or [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) function.</span></span>

## <a name="service-class-data-structures"></a><span data-ttu-id="243e2-137">服務類別資料結構</span><span class="sxs-lookup"><span data-stu-id="243e2-137">Service Class Data Structures</span></span>

<span data-ttu-id="243e2-138">安裝新的服務類別時，必須備妥和提供 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。</span><span class="sxs-lookup"><span data-stu-id="243e2-138">When a new service class is installed, a [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) structure must be prepared and supplied.</span></span> <span data-ttu-id="243e2-139">此結構也包含包含一系列適用于特定命名空間之成員的子結構。</span><span class="sxs-lookup"><span data-stu-id="243e2-139">This structure also consists of substructures that contain a series of members that apply to specific namespaces.</span></span> <span data-ttu-id="243e2-140">類別資訊資料結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="243e2-140">A class info data structure is as follows:</span></span>

![服務類別資料結構架構](images/ovrvw3-3.png)

<span data-ttu-id="243e2-142">每個服務類別都有一個 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。</span><span class="sxs-lookup"><span data-stu-id="243e2-142">For each service class, there is a single [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) structure.</span></span> <span data-ttu-id="243e2-143">在 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構內，服務類別的唯一識別碼會包含在 **lpServiceClassId** 成員中，而 **lpServiceClassName** 成員會參考相關聯的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="243e2-143">Within the [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) structure, the service class' unique identifier is contained in the **lpServiceClassId** member, and an associated display string is referenced by the **lpServiceClassName** member.</span></span> <span data-ttu-id="243e2-144">這是 [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) 函數所傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="243e2-144">This is the string that is returned by the [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function.</span></span>

<span data-ttu-id="243e2-145">[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)結構中的 **lpClassInfos** 成員會參考 **WSANSCLASSINFO** 結構的陣列，其中每個結構都會提供套用至指定命名空間的命名和具類型成員。</span><span class="sxs-lookup"><span data-stu-id="243e2-145">The **lpClassInfos** member in the [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) structure references an array of **WSANSCLASSINFO** structures, each of which supplies a named and typed member that applies to a specified namespace.</span></span> <span data-ttu-id="243e2-146">**LpszName** 成員的值範例包括： "SapId"、"TcpPort"、"UdpPort" 等。這些字串通常是針對 **dwNameSpace** 成員中識別的命名空間所特有。</span><span class="sxs-lookup"><span data-stu-id="243e2-146">Examples of values for the **lpszName** member include: "SapId", "TcpPort", "UdpPort", etc. These strings are generally specific to the namespace identified in the **dwNameSpace** member.</span></span> <span data-ttu-id="243e2-147">**DwValueType** 成員的一般值可能是 reg \_ DWORD、reg \_ SZ 等等。**DwValueSize** 成員會指出 **lpValue** 所指向之資料項目的長度。</span><span class="sxs-lookup"><span data-stu-id="243e2-147">Typical values for the **dwValueType** member might be REG\_DWORD, REG\_SZ, etc. The **dwValueSize** member indicates the length of the data item pointed to by **lpValue**.</span></span>

<span data-ttu-id="243e2-148">叫用 [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)函式時，會為每個命名空間提供者提供 **WSASERVICECLASSINFO** 結構中所表示的整個資料集合。</span><span class="sxs-lookup"><span data-stu-id="243e2-148">The entire collection of data represented in a **WSASERVICECLASSINFO** structure is provided to each namespace provider when the [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) function is invoked.</span></span> <span data-ttu-id="243e2-149">接著，每個個別的命名空間提供者會 sifts **WSANSCLASSINFO** 結構的清單，並保留適用的資訊。</span><span class="sxs-lookup"><span data-stu-id="243e2-149">Each individual namespace provider then sifts through the list of **WSANSCLASSINFO** structures and retains the information applicable to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="243e2-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="243e2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="243e2-151">**AFPROTOCOLS**</span><span class="sxs-lookup"><span data-stu-id="243e2-151">**AFPROTOCOLS**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[<span data-ttu-id="243e2-152">**CSADDR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="243e2-152">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="243e2-153">名稱解析模型</span><span class="sxs-lookup"><span data-stu-id="243e2-153">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="243e2-154">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="243e2-154">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="243e2-155">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="243e2-155">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="243e2-156">**通訊端 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="243e2-156">**SOCKET\_ADDRESS**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[<span data-ttu-id="243e2-157">名稱解析函數的摘要</span><span class="sxs-lookup"><span data-stu-id="243e2-157">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[<span data-ttu-id="243e2-158">**WSAECOMPARATOR**</span><span class="sxs-lookup"><span data-stu-id="243e2-158">**WSAECOMPARATOR**</span></span>](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[<span data-ttu-id="243e2-159">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="243e2-159">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="243e2-160">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="243e2-160">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="243e2-161">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="243e2-161">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="243e2-162">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="243e2-162">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="243e2-163">**WSASERVICECLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="243e2-163">**WSASERVICECLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
