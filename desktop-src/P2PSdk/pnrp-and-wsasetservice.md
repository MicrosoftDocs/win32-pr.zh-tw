---
description: PNRP 會使用 WSASetService 函數來註冊或移除對等名稱。
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP 和 WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974683"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="aa6f3-103">PNRP 和 WSASetService</span><span class="sxs-lookup"><span data-stu-id="aa6f3-103">PNRP and WSASetService</span></span>

<span data-ttu-id="aa6f3-104">PNRP 會使用 [**WSASetService**](winsock-nsp-reference-links.md) 函數來註冊或移除 [對等名稱](peer-names.md)。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="aa6f3-105">註冊名稱</span><span class="sxs-lookup"><span data-stu-id="aa6f3-105">Registering a Name</span></span>

<span data-ttu-id="aa6f3-106">註冊包含對等名稱，以及可聯繫服務的端點集合。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="aa6f3-107">註冊適用于 PNRP 雲端。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="aa6f3-108">註冊對等之後，註冊與其他節點之間的註冊資訊與傳播之間會有延遲。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="aa6f3-109">在這段期間，其他節點可能無法解析新註冊的對等。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="aa6f3-110">服務註冊不是持續性。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="aa6f3-111">如果註冊對等名稱的用戶端進程結束或呼叫 [**WSACleanup**](winsock-nsp-reference-links.md)，則對等名稱會取消註冊。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="aa6f3-112">如果指定的對等名稱已由目前的進程在相同的雲端中註冊，則會以新的註冊值取代。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="aa6f3-113">註冊對等名稱時，必須指出下列參數值：</span><span class="sxs-lookup"><span data-stu-id="aa6f3-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="aa6f3-114">*essOperation* 參數的值必須是 **RNRSERVICE \_ REGISTER**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="aa6f3-115">*dwControlFlags* 參數必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="aa6f3-116">註冊對等名稱時， *lpqsRegInfo* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：</span><span class="sxs-lookup"><span data-stu-id="aa6f3-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="aa6f3-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-118">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-120">指定要註冊的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-120">Specifies a peer name to register.</span></span> <span data-ttu-id="aa6f3-121">如果 [對等名稱](peer-names.md) 是不安全的，則身分識別是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="aa6f3-122">如果將身分識別指定為 **Null**，PNRP 預設會使用電腦本機身分識別。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-124">必須是 SVCID \_ PNRPNAME。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-126">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-126">Ignored.</span></span> <span data-ttu-id="aa6f3-127">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-129">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-129">Ignored.</span></span> <span data-ttu-id="aa6f3-130">不過，字串仍然必須少於40個字元，包括 **Null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-132">必須是 **ns \_ PNRPNAME** 或 **ns \_ ALL**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-134">必須是 **NS \_ 提供者 \_ PNRPNAME** 或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-136">必須是雲端名稱、空字串或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="aa6f3-137">如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global"。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="aa6f3-138">否則，它必須指向有效的雲端名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-140">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-140">Ignored.</span></span> <span data-ttu-id="aa6f3-141">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-143">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-143">Ignored.</span></span> <span data-ttu-id="aa6f3-144">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-146">指定服務所註冊的位址數目。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="aa6f3-147">可以為單一名稱註冊的位址數目上限為10。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-149">要註冊之地址清單的指標。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-151">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-151">Ignored.</span></span> <span data-ttu-id="aa6f3-152">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-154">指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="aa6f3-155">必須設定 **PNRPINFO** 結構中的特定參數。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="aa6f3-156">如需詳細資訊，請參閱下列 **PNRPINFO** 結構一節。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="aa6f3-157">PNRPINFO 結構</span><span class="sxs-lookup"><span data-stu-id="aa6f3-157">PNRPINFO Structure</span></span>

<span data-ttu-id="aa6f3-158">如果設定 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構的 **lpBlob** 成員，就必須設定下列 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構的成員：</span><span class="sxs-lookup"><span data-stu-id="aa6f3-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="aa6f3-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-160">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-162">指定使用 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)建立之對等名稱的身分識別。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="aa6f3-163">如果對等名稱是不安全的，則身分識別是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="aa6f3-164">如果將身分識別指定為 **Null**，PNRP 預設會使用電腦本機身分識別。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-166">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-166">Ignored.</span></span> <span data-ttu-id="aa6f3-167">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-169">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-169">Ignored.</span></span> <span data-ttu-id="aa6f3-170">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-172">指定重新整理作業之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-174">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-174">Ignored.</span></span> <span data-ttu-id="aa6f3-175">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-177">必須是零 (0) 或 **PNRPINFO \_ 提示**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="aa6f3-178">預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-178">The default is zero (0).</span></span> <span data-ttu-id="aa6f3-179">這表示 PNRP 識別碼的服務位置部分是使用 **saHint** 中的 IP 位址所建立。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="aa6f3-180">否則，會使用 **lpcsaBuffer** 成員的第一個 IPv6 專案中的第一個 IP 位址來建立服務位置。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-182">指定提示的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-184">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-184">Ignored.</span></span> <span data-ttu-id="aa6f3-185">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="aa6f3-186">取消註冊對等名稱</span><span class="sxs-lookup"><span data-stu-id="aa6f3-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="aa6f3-187">下列清單會識別有關取消註冊對等名稱的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="aa6f3-188">只有註冊對等名稱的應用程式才能將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="aa6f3-189">如果呼叫 [**WSACleanup**](winsock-nsp-reference-links.md) ，就會自動取消註冊對等名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="aa6f3-190">PNRP 一律會移除整個服務名稱註冊。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="aa6f3-191">不允許移除個別位址。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="aa6f3-192">取消註冊名稱時， *essOperation* 參數的值必須為 **RNRSERVICE \_ DELETE**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="aa6f3-193">PNRP 不支援 **RNRSERVICE 取消 \_ 註冊** 的值。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="aa6f3-194">*DwControlFlags* 參數必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="aa6f3-195">取消註冊名稱時， *lpqsRegInfo* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：</span><span class="sxs-lookup"><span data-stu-id="aa6f3-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="aa6f3-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-197">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-199">指定要取消註冊的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-201">必須是 **SVCID \_ PNRPNAME**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-203">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-203">Ignored.</span></span> <span data-ttu-id="aa6f3-204">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-206">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-206">Ignored.</span></span> <span data-ttu-id="aa6f3-207">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-209">必須是 **ns \_ PNRPNAME** 或 **ns \_ ALL**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-211">必須是 **NS \_ 提供者 \_ PNRPNAME** 或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-213">必須是雲端名稱、空字串或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="aa6f3-214">如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global"。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="aa6f3-215">否則，它必須指向有效的雲端名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-217">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-217">Ignored.</span></span> <span data-ttu-id="aa6f3-218">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-220">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-220">Ignored.</span></span> <span data-ttu-id="aa6f3-221">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-223">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-223">Ignored.</span></span> <span data-ttu-id="aa6f3-224">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-226">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-226">Ignored.</span></span> <span data-ttu-id="aa6f3-227">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-229">忽略。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-229">Ignored.</span></span> <span data-ttu-id="aa6f3-230">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="aa6f3-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="aa6f3-232">指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="aa6f3-233">**LpBlob** 結構的 **lpszIdentity** 成員會識別用來註冊對等名稱的身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="aa6f3-234">其餘成員必須設定為註冊名稱時所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="aa6f3-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="aa6f3-235">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa6f3-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa6f3-236">PNRP 和 BLOB</span><span class="sxs-lookup"><span data-stu-id="aa6f3-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="aa6f3-237">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="aa6f3-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="aa6f3-238">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="aa6f3-239">PNRP NSP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="aa6f3-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="aa6f3-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="aa6f3-241">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="aa6f3-241">**WSASetService**</span></span>
</dt> </dl>

 

 



