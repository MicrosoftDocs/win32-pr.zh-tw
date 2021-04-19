---
description: PNRP 會使用 WSALookupServiceNext 函數來比對 WSALookupServiceBegin 先前呼叫中所指定的查詢。
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP 和 WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980986"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="8d63a-103">PNRP 和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="8d63a-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="8d63a-104">PNRP 會使用 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 函數來比對 **WSALookupServiceBegin** 先前呼叫中所指定的查詢。</span><span class="sxs-lookup"><span data-stu-id="8d63a-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="8d63a-105">**WSALookupServiceNext** 函式的結果是由在初始 **WSALookupServiceBegin** 函式呼叫中傳遞的 **WSAQUERYSET** 結構中的設定所決定。</span><span class="sxs-lookup"><span data-stu-id="8d63a-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="8d63a-106">此函式是用來執行下列兩個函數：</span><span class="sxs-lookup"><span data-stu-id="8d63a-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="8d63a-107">將對等名稱解析為地址清單</span><span class="sxs-lookup"><span data-stu-id="8d63a-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="8d63a-108">列舉網路雲</span><span class="sxs-lookup"><span data-stu-id="8d63a-108">Enumerating network clouds</span></span>

<span data-ttu-id="8d63a-109">您可以使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md)，以非同步方式使用 lookup 服務。</span><span class="sxs-lookup"><span data-stu-id="8d63a-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="8d63a-110">如需以非同步方式使用查閱服務函數的詳細資訊，請參閱 [PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)。</span><span class="sxs-lookup"><span data-stu-id="8d63a-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="8d63a-111">[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會封鎖，即使呼叫 **WSANSPIoctl** 也是一樣。</span><span class="sxs-lookup"><span data-stu-id="8d63a-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="8d63a-112">在呼叫 **WSALookupServiceNext** 之前，應用程式必須等到收到通知（如果封鎖發生問題）。</span><span class="sxs-lookup"><span data-stu-id="8d63a-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="8d63a-113">將對等名稱解析為地址清單</span><span class="sxs-lookup"><span data-stu-id="8d63a-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="8d63a-114">將對等名稱解析為地址清單時，在 *lpqsResults* 參數中傳回的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構會包含下列值：</span><span class="sxs-lookup"><span data-stu-id="8d63a-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8d63a-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8d63a-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-116">傳回結構的大小。</span><span class="sxs-lookup"><span data-stu-id="8d63a-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="8d63a-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-118">傳回對等名稱，如果 **LUP \_ 傳回 \_ 名稱**，則會指定 **LUP \_ return \_ ALL** 或 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="8d63a-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-120">傳回 **SVCID \_ PNRPNAME**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="8d63a-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-122">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="8d63a-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-124">傳回批註-如果 **LUP 傳回 \_ \_ 批註**、 **LUP 傳回 \_ \_ 全部**，或指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="8d63a-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-126">傳回 **NS \_ PNRPNAME**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="8d63a-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-128">傳回 **NS \_ 提供者 \_ PNRPNAME**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8d63a-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-130">如果指定了 LUP 傳回 **\_ \_ 名稱**、LUP 傳回 **\_ \_ 全部** 或 **Null** ，則會傳回雲端名稱。</span><span class="sxs-lookup"><span data-stu-id="8d63a-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="8d63a-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-132">傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="8d63a-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-134">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="8d63a-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-136">傳回 CSADDR 資訊陣列中的專案數 \_ （如果 **LUP 傳回 \_ \_ ADDR**、 **LUP \_ RETURN \_ ALL** 或 **Null** ）。</span><span class="sxs-lookup"><span data-stu-id="8d63a-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="8d63a-137">此值和 **lpcsaBuffer** 中的資訊是此結構中所傳回信息的金鑰位。</span><span class="sxs-lookup"><span data-stu-id="8d63a-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="8d63a-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-139">\_如果 **LUP 傳回 \_ \_ ADDR**、 **LUP \_ RETURN \_ ALL** 或 **Null** ，則傳回 CSADDR 資訊結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="8d63a-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="8d63a-140">這個緩衝區和 **dwNumberOfCsAddrs** 中的值是此結構中所傳回的金鑰資訊位。</span><span class="sxs-lookup"><span data-stu-id="8d63a-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="8d63a-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-142">傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="8d63a-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-144">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="8d63a-145">列舉網路雲</span><span class="sxs-lookup"><span data-stu-id="8d63a-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="8d63a-146">列舉雲端時， *lpqsResults* 參數中所傳回的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構包含下列值：</span><span class="sxs-lookup"><span data-stu-id="8d63a-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8d63a-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8d63a-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-148">傳回結構的大小。</span><span class="sxs-lookup"><span data-stu-id="8d63a-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="8d63a-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-150">傳回雲端名稱-如果 **LUP 傳回 \_ \_ 名稱**，則會指定 **LUP \_ return \_ ALL** 或 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="8d63a-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-152">傳回 **SVCID \_ PNRPCLOUD**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="8d63a-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-154">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="8d63a-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-156">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="8d63a-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-158">傳回 **NS \_ PNRPCLOUD**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="8d63a-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-160">傳回 **NS \_ 提供者 \_ PNRPCLOUD**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8d63a-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-162">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="8d63a-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-164">傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="8d63a-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-166">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="8d63a-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-168">傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="8d63a-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-170">傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d63a-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="8d63a-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-172">傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="8d63a-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-174">傳回指向 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標，如果 **LUP 傳回 \_ \_ BLOB**、 **LUP 傳回 \_ \_ 全部**，或指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8d63a-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="8d63a-175">PNRPCLOUDINFO 結構</span><span class="sxs-lookup"><span data-stu-id="8d63a-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="8d63a-176">列舉雲端名稱時， [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) 結構中會傳回下列值：</span><span class="sxs-lookup"><span data-stu-id="8d63a-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="8d63a-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8d63a-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-178">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="8d63a-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**雲**</span><span class="sxs-lookup"><span data-stu-id="8d63a-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-180">實際的雲端價值。</span><span class="sxs-lookup"><span data-stu-id="8d63a-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="8d63a-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-182">雲端的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8d63a-182">The current state of a cloud.</span></span> <span data-ttu-id="8d63a-183">[**PNRP \_雲端 \_ 狀態**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) 會指定有效的值。</span><span class="sxs-lookup"><span data-stu-id="8d63a-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="8d63a-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span><span class="sxs-lookup"><span data-stu-id="8d63a-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8d63a-185">指出雲端名稱在網路上有效，或僅適用于目前的電腦。</span><span class="sxs-lookup"><span data-stu-id="8d63a-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="8d63a-186">[**PNRP \_雲端 \_ 旗標**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) 會指定有效的值。</span><span class="sxs-lookup"><span data-stu-id="8d63a-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="8d63a-187">某些雲端名稱在相同網路上的任何電腦上都是有效的。</span><span class="sxs-lookup"><span data-stu-id="8d63a-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="8d63a-188">其他雲端名稱只有在目前的電腦上才有效，而且可能只會在一段時間內有效。</span><span class="sxs-lookup"><span data-stu-id="8d63a-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="8d63a-189">如果 **enCloudFlags** 設定為 **PNRP \_ 雲端 \_ 名稱 \_ LOCAL，** 則名稱只在本機有效。</span><span class="sxs-lookup"><span data-stu-id="8d63a-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="8d63a-190">如果未設定 **enCloudFlags** ，則雲端名稱可以轉移到其他電腦。</span><span class="sxs-lookup"><span data-stu-id="8d63a-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8d63a-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d63a-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d63a-192">PNRP 和 BLOB</span><span class="sxs-lookup"><span data-stu-id="8d63a-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="8d63a-193">PNRP 和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="8d63a-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="8d63a-194">PNRP 和 WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="8d63a-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="8d63a-195">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="8d63a-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="8d63a-196">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="8d63a-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="8d63a-197">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="8d63a-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="8d63a-198">PNRP NSP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8d63a-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="8d63a-199">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="8d63a-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



