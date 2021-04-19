---
description: PNRP 使用 WSALookupServiceBegin 函式來啟動可讓應用程式執行下列作業的進程。
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP 和 WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106992288"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="b4d72-103">PNRP 和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="b4d72-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="b4d72-104">PNRP 使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 函式來啟動可讓應用程式執行下列作業的進程：</span><span class="sxs-lookup"><span data-stu-id="b4d72-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="b4d72-105">解析名稱</span><span class="sxs-lookup"><span data-stu-id="b4d72-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="b4d72-106">列舉網路雲</span><span class="sxs-lookup"><span data-stu-id="b4d72-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="b4d72-107">嘗試執行其中一個函式的用戶端會使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)、 **WSALookupServiceNext** 和 **WSALookupServiceEnd** 函數。</span><span class="sxs-lookup"><span data-stu-id="b4d72-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="b4d72-108">您可以使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md)，以非同步方式使用 lookup 服務。</span><span class="sxs-lookup"><span data-stu-id="b4d72-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="b4d72-109">如需以非同步方式使用查閱服務函數的詳細資訊，請參閱 [PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)。</span><span class="sxs-lookup"><span data-stu-id="b4d72-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="b4d72-110">使用對等名稱的程式與使用雲端的程式不同。</span><span class="sxs-lookup"><span data-stu-id="b4d72-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="b4d72-111">本主題會分別描述每個程式。</span><span class="sxs-lookup"><span data-stu-id="b4d72-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="b4d72-112">解析名稱</span><span class="sxs-lookup"><span data-stu-id="b4d72-112">Resolving a Name</span></span>

<span data-ttu-id="b4d72-113">應用程式會使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 來取得在另一部電腦上註冊之對等服務的 IP 位址、埠和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b4d72-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="b4d72-114">**WSALookupServiceBegin** 函式可用來啟動名稱解析程式，並設定參數和限制。</span><span class="sxs-lookup"><span data-stu-id="b4d72-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="b4d72-115">傳回控制碼，而且必須在呼叫 **WSALookupServiceNext** 和 **WSANSPIoctl** 時使用。</span><span class="sxs-lookup"><span data-stu-id="b4d72-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="b4d72-116">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="b4d72-116">lpqsRestrictions</span></span>

<span data-ttu-id="b4d72-117">解析對等名稱時， *lpqsRestrictions* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：</span><span class="sxs-lookup"><span data-stu-id="b4d72-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b4d72-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b4d72-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-119">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b4d72-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="b4d72-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-121">指定要解析的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d72-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="b4d72-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-123">必須是 **SVCID \_ PNRPNAME**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="b4d72-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-125">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="b4d72-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-127">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="b4d72-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-129">必須是 **ns \_ PNRPNAME** 或 **ns \_ ALL**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="b4d72-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-131">必須是 **NS \_ 提供者 \_ PNRPNAME** 或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="b4d72-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-133">必須是雲端名稱、空字串或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="b4d72-134">如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global \_ "。</span><span class="sxs-lookup"><span data-stu-id="b4d72-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="b4d72-135">否則，它必須指向有效的雲端名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d72-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="b4d72-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-137">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="b4d72-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-139">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="b4d72-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-141">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="b4d72-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-143">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="b4d72-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-145">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="b4d72-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-147">必須是 [**BLOB**](winsock-nsp-reference-links.md) 結構的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="b4d72-148">如果是 **Null**，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="b4d72-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="b4d72-149">如果設定， **lpBlob** 會指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構，而且必須設定 **PNRPINFO** 結構中的特定參數。</span><span class="sxs-lookup"><span data-stu-id="b4d72-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="b4d72-150">如需詳細資訊，請參閱下列 PNRPINFO 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="b4d72-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="b4d72-151">PNRPINFO 結構</span><span class="sxs-lookup"><span data-stu-id="b4d72-151">PNRPINFO Structure</span></span>

<span data-ttu-id="b4d72-152">如果設定 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構的 **lpBlob** 成員，就必須設定下列 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構的成員：</span><span class="sxs-lookup"><span data-stu-id="b4d72-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="b4d72-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b4d72-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-154">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b4d72-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="b4d72-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-156">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="b4d72-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-158">指定所要求的解析度數目。</span><span class="sxs-lookup"><span data-stu-id="b4d72-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="b4d72-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-160">指定要求的超時時間長度以等候回應。</span><span class="sxs-lookup"><span data-stu-id="b4d72-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="b4d72-161">預設值為 30 秒。</span><span class="sxs-lookup"><span data-stu-id="b4d72-161">The default is 30 seconds.</span></span> <span data-ttu-id="b4d72-162">最大值為600秒 (10 分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="b4d72-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-164">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="b4d72-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-166">必須是其中一個允許的值。</span><span class="sxs-lookup"><span data-stu-id="b4d72-166">Must be one of the allowed values.</span></span> <span data-ttu-id="b4d72-167">預設值為 **PNRP \_ 解析 \_ 準則 \_ 非 \_ 目前的 \_ 進程 \_ 對等 \_ 名稱**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="b4d72-168">有效的值是由 [**PNRP \_ 解析 \_ 準則**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)所指定。</span><span class="sxs-lookup"><span data-stu-id="b4d72-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b4d72-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-170">必須是零 (0) 或 **PNRPINFO \_ 提示**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="b4d72-171">預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="b4d72-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="b4d72-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-173">指定提示的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b4d72-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="b4d72-174">嘗試尋找最接近的對等名稱時，會使用提示。</span><span class="sxs-lookup"><span data-stu-id="b4d72-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="b4d72-175">提示的格式是 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="b4d72-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="b4d72-176">如果在尋找最接近的對等名稱時未指定 **saHint** ，則會改為使用本機電腦的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="b4d72-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="b4d72-177">如果未設定 **dwFlags** ，則會忽略這個成員。</span><span class="sxs-lookup"><span data-stu-id="b4d72-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="b4d72-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-179">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="b4d72-180">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="b4d72-180">dwControlFlags</span></span>

<span data-ttu-id="b4d72-181">PNRP 支援下列 LUP 傳回 \_ \_ \* 旗標：</span><span class="sxs-lookup"><span data-stu-id="b4d72-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="b4d72-182">值</span><span class="sxs-lookup"><span data-stu-id="b4d72-182">Value</span></span>                | <span data-ttu-id="b4d72-183">描述</span><span class="sxs-lookup"><span data-stu-id="b4d72-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="b4d72-184">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="b4d72-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="b4d72-185">傳回名稱和內容。</span><span class="sxs-lookup"><span data-stu-id="b4d72-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="b4d72-186">LUP \_ 傳回 \_ 批註</span><span class="sxs-lookup"><span data-stu-id="b4d72-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="b4d72-187">傳回與名稱相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="b4d72-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="b4d72-188">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="b4d72-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="b4d72-189">傳回與名稱相關聯的位址。</span><span class="sxs-lookup"><span data-stu-id="b4d72-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="b4d72-190">列舉網路雲</span><span class="sxs-lookup"><span data-stu-id="b4d72-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="b4d72-191">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="b4d72-191">lpqsRestrictions</span></span>

<span data-ttu-id="b4d72-192">列舉雲端時， *lpqsRestrictions* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：</span><span class="sxs-lookup"><span data-stu-id="b4d72-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b4d72-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b4d72-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-194">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b4d72-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="b4d72-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-196">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="b4d72-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-198">必須是 **SVCID \_ PNRPCLOUD**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="b4d72-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-200">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="b4d72-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-202">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="b4d72-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-204">必須是 **NS \_ PNRPCLOUD**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="b4d72-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-206">必須是 **NS \_ 提供者 \_ PNRPCLOUD** 或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**</span><span class="sxs-lookup"><span data-stu-id="b4d72-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-208">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="b4d72-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-210">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="b4d72-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-212">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="b4d72-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-214">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="b4d72-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-216">Reserved，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="b4d72-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-218">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="b4d72-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-220">指向 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b4d72-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="b4d72-221">如果 **lpBlob** 為 **Null**，則會列舉所有雲端。</span><span class="sxs-lookup"><span data-stu-id="b4d72-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="b4d72-222">PNRPCLOUDINFO 結構</span><span class="sxs-lookup"><span data-stu-id="b4d72-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="b4d72-223">列舉雲端時，必須設定下列 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) 結構的成員：</span><span class="sxs-lookup"><span data-stu-id="b4d72-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="b4d72-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b4d72-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-225">指定此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b4d72-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**雲**</span><span class="sxs-lookup"><span data-stu-id="b4d72-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-227">指向指定準則的結構，您可以用來篩選搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b4d72-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="b4d72-228">**雲端。範圍** 成員可以是任何、 **pnrp \_ 全域 \_ 範圍**、 **pnrp \_ 網站 \_ 區域 \_ 範圍** 或 **pnrp \_ 連結 \_ 本機 \_ 範圍** 的 **pnrp \_ 範圍 \_**。</span><span class="sxs-lookup"><span data-stu-id="b4d72-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="b4d72-229">如果指定了 **\_ \_ ANY 的 PNRP 範圍** ，則會傳回所有的雲端。</span><span class="sxs-lookup"><span data-stu-id="b4d72-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="b4d72-230">否則，只會傳回符合 **雲端的雲端。範圍** 會傳回。</span><span class="sxs-lookup"><span data-stu-id="b4d72-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="b4d72-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="b4d72-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="b4d72-232">保留，必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="b4d72-233">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="b4d72-233">dwControlFlags</span></span>

<span data-ttu-id="b4d72-234">PNRP 支援下列 LUP 傳回 \_ \_ \* 旗標：</span><span class="sxs-lookup"><span data-stu-id="b4d72-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="b4d72-235">值</span><span class="sxs-lookup"><span data-stu-id="b4d72-235">Value</span></span>             | <span data-ttu-id="b4d72-236">描述</span><span class="sxs-lookup"><span data-stu-id="b4d72-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b4d72-237">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="b4d72-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="b4d72-238">傳回名稱和內容。</span><span class="sxs-lookup"><span data-stu-id="b4d72-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="b4d72-239">LUP \_ 傳回 \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="b4d72-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="b4d72-240">傳回與這個雲端相關聯的 [BLOB](pnrp-and-blob.md) 。</span><span class="sxs-lookup"><span data-stu-id="b4d72-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b4d72-241">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4d72-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4d72-242">PNRP 和 BLOB</span><span class="sxs-lookup"><span data-stu-id="b4d72-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="b4d72-243">PNRP 和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="b4d72-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="b4d72-244">PNRP 和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="b4d72-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="b4d72-245">PNRP 和 WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="b4d72-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="b4d72-246">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="b4d72-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="b4d72-247">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="b4d72-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="b4d72-248">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="b4d72-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="b4d72-249">PNRP NSP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b4d72-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



