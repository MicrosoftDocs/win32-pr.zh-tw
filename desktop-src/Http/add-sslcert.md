---
title: add sslcert
description: 新增安全通訊端層 (SSL) 伺服器憑證系結，以及 IP 位址和埠的對應用戶端憑證原則。
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- 新增 sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644190"
---
# <a name="add-sslcert"></a><span data-ttu-id="246f4-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="246f4-104">add sslcert</span></span>

<span data-ttu-id="246f4-105">新增安全通訊端層 (SSL) 伺服器憑證系結，以及 IP 位址和埠的對應用戶端憑證原則。</span><span class="sxs-lookup"><span data-stu-id="246f4-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="246f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="246f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="246f4-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = IP 位址：埠\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-108">指定繫結的 IP 位址和連接埠。</span><span class="sxs-lookup"><span data-stu-id="246f4-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = 字串\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-110">指定憑證的 SHA 雜湊。</span><span class="sxs-lookup"><span data-stu-id="246f4-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="246f4-111">此雜湊的長度為20個位元組，並指定為十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="246f4-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid = GUID\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-113">指定用來識別主控應用程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="246f4-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = 字串\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-115">指定憑證的存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="246f4-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="246f4-116">預設為 MY。</span><span class="sxs-lookup"><span data-stu-id="246f4-116">Defaults to MY.</span></span> <span data-ttu-id="246f4-117">憑證必須儲存在本機電腦內容中。</span><span class="sxs-lookup"><span data-stu-id="246f4-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-119">開啟或 turnsoff 用戶端憑證撤銷的驗證。</span><span class="sxs-lookup"><span data-stu-id="246f4-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-121">開啟或關閉只有快取用戶端憑證的使用方式，以進行撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="246f4-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-123">開啟或關閉使用方式檢查。</span><span class="sxs-lookup"><span data-stu-id="246f4-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="246f4-124">預設值為啟用。</span><span class="sxs-lookup"><span data-stu-id="246f4-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-126">指定檢查是否有更新憑證撤銷清單 (CRL) 的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="246f4-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="246f4-127">如果這個值為0，則只有在前一個 CRL 過期 (（以秒為單位）時，才會更新新的 CRL) 。</span><span class="sxs-lookup"><span data-stu-id="246f4-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="246f4-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-129">指定嘗試取得遠端 URL 的憑證撤銷清單時的逾時間隔， (毫秒) 。</span><span class="sxs-lookup"><span data-stu-id="246f4-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="246f4-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier = 字串\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-131">列出可以信任的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="246f4-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="246f4-132">此清單可以是電腦信任之憑證簽發者的子集。</span><span class="sxs-lookup"><span data-stu-id="246f4-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename = 字串\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-134">指定儲存 SslCtlIdentifier 的本機電腦下的存放區名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="246f4-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-136">開啟或關閉 DS 對應程式數目。</span><span class="sxs-lookup"><span data-stu-id="246f4-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="246f4-137">預設值為停用。</span><span class="sxs-lookup"><span data-stu-id="246f4-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="246f4-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="246f4-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="246f4-139">開啟或關閉憑證的協商。</span><span class="sxs-lookup"><span data-stu-id="246f4-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="246f4-140">預設值為停用。</span><span class="sxs-lookup"><span data-stu-id="246f4-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="246f4-141">範例</span><span class="sxs-lookup"><span data-stu-id="246f4-141">Examples</span></span>

<span data-ttu-id="246f4-142">**add sslcert ipport = 1.1.1.1：443**</span><span class="sxs-lookup"><span data-stu-id="246f4-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="246f4-143">**certhash = 0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="246f4-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="246f4-144">**appid = {00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="246f4-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




