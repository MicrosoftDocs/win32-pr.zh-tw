---
description: PNRP 使用 WSALookupServiceBegin 函式來啟動可讓應用程式執行下列作業的進程。
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP 和 WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553398"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP 和 WSALookupServiceBegin

PNRP 使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 函式來啟動可讓應用程式執行下列作業的進程：

-   [解析名稱](#resolving-a-name)
-   [列舉網路雲](#enumerating-network-clouds)

嘗試執行其中一個函式的用戶端會使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)、 **WSALookupServiceNext** 和 **WSALookupServiceEnd** 函數。

您可以使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md)，以非同步方式使用 lookup 服務。 如需以非同步方式使用查閱服務函數的詳細資訊，請參閱 [PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)。

使用對等名稱的程式與使用雲端的程式不同。 本主題會分別描述每個程式。

## <a name="resolving-a-name"></a>解析名稱

應用程式會使用 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 來取得在另一部電腦上註冊之對等服務的 IP 位址、埠和通訊協定。 **WSALookupServiceBegin** 函式可用來啟動名稱解析程式，並設定參數和限制。 傳回控制碼，而且必須在呼叫 **WSALookupServiceNext** 和 **WSANSPIoctl** 時使用。

### <a name="lpqsrestrictions"></a>lpqsRestrictions

解析對等名稱時， *lpqsRestrictions* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

指定要解析的對等名稱。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

必須是 **SVCID \_ PNRPNAME**。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

必須是 **ns \_ PNRPNAME** 或 **ns \_ ALL**。

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

必須是 **NS \_ 提供者 \_ PNRPNAME** 或 **Null**。

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**
</dt> <dd>

必須是雲端名稱、空字串或 **Null**。 如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global \_ "。 否則，它必須指向有效的雲端名稱。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

必須是 [**BLOB**](winsock-nsp-reference-links.md) 結構的指標或 **Null**。 如果是 **Null**，則會使用預設值。 如果設定， **lpBlob** 會指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構，而且必須設定 **PNRPINFO** 結構中的特定參數。 如需詳細資訊，請參閱下列 PNRPINFO 結構的描述。

</dd> </dl>

PNRPINFO 結構

如果設定 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構的 **lpBlob** 成員，就必須設定下列 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構的成員：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

指定所要求的解析度數目。

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

指定要求的超時時間長度以等候回應。 預設值為 30 秒。 最大值為600秒 (10 分鐘) 。

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

必須是其中一個允許的值。 預設值為 **PNRP \_ 解析 \_ 準則 \_ 非 \_ 目前的 \_ 進程 \_ 對等 \_ 名稱**。 有效的值是由 [**PNRP \_ 解析 \_ 準則**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)所指定。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

必須是零 (0) 或 **PNRPINFO \_ 提示**。 預設為零 (0)。

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

指定提示的 IP 位址。 嘗試尋找最接近的對等名稱時，會使用提示。 提示的格式是 IPv6 位址。 如果在尋找最接近的對等名稱時未指定 **saHint** ，則會改為使用本機電腦的 IPv6 位址。 如果未設定 **dwFlags** ，則會忽略這個成員。

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

保留，必須為零 (0) 。

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

PNRP 支援下列 LUP 傳回 \_ \_ \* 旗標：



| 值                | 描述                                |
|----------------------|--------------------------------------------|
| LUP \_ 傳回 \_ 名稱    | 傳回名稱和內容。                |
| LUP \_ 傳回 \_ 批註 | 傳回與名稱相關聯的批註。  |
| LUP \_ 傳回 \_ 位址    | 傳回與名稱相關聯的位址。 |



 

## <a name="enumerating-network-clouds"></a>列舉網路雲

### <a name="lpqsrestrictions"></a>lpqsRestrictions

列舉雲端時， *lpqsRestrictions* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

必須是 **Null**。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

必須是 **SVCID \_ PNRPCLOUD**。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

必須是 **NS \_ PNRPCLOUD**。

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

必須是 **NS \_ 提供者 \_ PNRPCLOUD** 或 **Null**。

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserved，必須是 **Null**。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

保留，必須為零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

指向 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。 如果 **lpBlob** 為 **Null**，則會列舉所有雲端。

</dd> </dl>

PNRPCLOUDINFO 結構

列舉雲端時，必須設定下列 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) 結構的成員：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**雲**
</dt> <dd>

指向指定準則的結構，您可以用來篩選搜尋結果。 **雲端。範圍** 成員可以是任何、 **pnrp \_ 全域 \_ 範圍**、 **pnrp \_ 網站 \_ 區域 \_ 範圍** 或 **pnrp \_ 連結 \_ 本機 \_ 範圍** 的 **pnrp \_ 範圍 \_**。 如果指定了 **\_ \_ ANY 的 PNRP 範圍** ，則會傳回所有的雲端。 否則，只會傳回符合 **雲端的雲端。範圍** 會傳回。

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

保留，必須為零 (0) 。

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

PNRP 支援下列 LUP 傳回 \_ \_ \* 旗標：



| 值             | 描述                                                       |
|-------------------|-------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 傳回名稱和內容。                                       |
| LUP \_ 傳回 \_ BLOB | 傳回與這個雲端相關聯的 [BLOB](pnrp-and-blob.md) 。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PNRP 和 BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP 和 WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP 和 WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP 和 WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP NSP 錯誤碼](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



