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
ms.openlocfilehash: 721931bfa05a96ca47fd69f643a02076201bb5f93eff003afa83714f2d14b519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950947"
---
# <a name="add-sslcert"></a>add sslcert

新增安全通訊端層 (SSL) 伺服器憑證系結，以及 IP 位址和埠的對應用戶端憑證原則。

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

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = IP 位址：埠\]**
</dt> <dd>

指定繫結的 IP 位址和連接埠。

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = 字串\]**
</dt> <dd>

指定憑證的 SHA 雜湊。 此雜湊的長度為20個位元組，並指定為十六進位字串。

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid = GUID\]**
</dt> <dd>

指定用來識別主控應用程式的 GUID。

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = 字串\]**
</dt> <dd>

指定憑證的存放區名稱。 預設為 MY。 憑證必須儲存在本機電腦內容中。

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {enable \| disable}\]**
</dt> <dd>

開啟或 turnsoff 用戶端憑證撤銷的驗證。

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {enable \| disable}\]**
</dt> <dd>

開啟或關閉只有快取用戶端憑證的使用方式，以進行撤銷檢查。

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {enable \| disable}\]**
</dt> <dd>

開啟或關閉使用方式檢查。 預設值為啟用。

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime = u-int\]**
</dt> <dd>

指定檢查是否有更新憑證撤銷清單 (CRL) 的時間間隔。 如果這個值為0，則只有在前一個 CRL 過期 (（以秒為單位）時，才會更新新的 CRL) 。

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout = u-int\]**
</dt> <dd>

指定嘗試取得遠端 URL 的憑證撤銷清單時的逾時間隔， (毫秒) 。

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier = 字串\]**
</dt> <dd>

列出可以信任的憑證簽發者。 此清單可以是電腦信任之憑證簽發者的子集。

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename = 字串\]**
</dt> <dd>

指定儲存 SslCtlIdentifier 的本機電腦下的存放區名稱 \_ 。

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {enable \| disable}\]**
</dt> <dd>

開啟或關閉 DS 對應程式數目。 預設值為停用。

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {enable \| disable}\]**
</dt> <dd>

開啟或關閉憑證的協商。 預設值為停用。

</dd> </dl>

## <a name="examples"></a>範例

**add sslcert ipport = 1.1.1.1：443**

**certhash = 0102030405060708090A0B0C0D0E0F1011121314**

**appid = {00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




