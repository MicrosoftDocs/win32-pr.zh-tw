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
# <a name="pnrp-and-wsasetservice"></a>PNRP 和 WSASetService

PNRP 會使用 [**WSASetService**](winsock-nsp-reference-links.md) 函數來註冊或移除 [對等名稱](peer-names.md)。

## <a name="registering-a-name"></a>註冊名稱

註冊包含對等名稱，以及可聯繫服務的端點集合。 註冊適用于 PNRP 雲端。 註冊對等之後，註冊與其他節點之間的註冊資訊與傳播之間會有延遲。 在這段期間，其他節點可能無法解析新註冊的對等。

服務註冊不是持續性。

-   如果註冊對等名稱的用戶端進程結束或呼叫 [**WSACleanup**](winsock-nsp-reference-links.md)，則對等名稱會取消註冊。
-   如果指定的對等名稱已由目前的進程在相同的雲端中註冊，則會以新的註冊值取代。

註冊對等名稱時，必須指出下列參數值：

-   *essOperation* 參數的值必須是 **RNRSERVICE \_ REGISTER**。
-   *dwControlFlags* 參數必須為零 (0) 。

註冊對等名稱時， *lpqsRegInfo* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

指定要註冊的對等名稱。 如果 [對等名稱](peer-names.md) 是不安全的，則身分識別是選擇性的。 如果將身分識別指定為 **Null**，PNRP 預設會使用電腦本機身分識別。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

必須是 SVCID \_ PNRPNAME。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

忽略。 不過，字串仍然必須少於40個字元，包括 **Null** 結束字元。

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

必須是雲端名稱、空字串或 **Null**。 如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global"。 否則，它必須指向有效的雲端名稱。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

指定服務所註冊的位址數目。 可以為單一名稱註冊的位址數目上限為10。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

要註冊之地址清單的指標。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。 必須設定 **PNRPINFO** 結構中的特定參數。 如需詳細資訊，請參閱下列 **PNRPINFO** 結構一節。

</dd> </dl>

## <a name="pnrpinfo-structure"></a>PNRPINFO 結構

如果設定 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構的 **lpBlob** 成員，就必須設定下列 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構的成員：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

指定使用 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)建立之對等名稱的身分識別。 如果對等名稱是不安全的，則身分識別是選擇性的。 如果將身分識別指定為 **Null**，PNRP 預設會使用電腦本機身分識別。

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

指定重新整理作業之間的秒數。

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

必須是零 (0) 或 **PNRPINFO \_ 提示**。 預設為零 (0)。 這表示 PNRP 識別碼的服務位置部分是使用 **saHint** 中的 IP 位址所建立。 否則，會使用 **lpcsaBuffer** 成員的第一個 IPv6 專案中的第一個 IP 位址來建立服務位置。

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

指定提示的 IPv6 位址。

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>取消註冊對等名稱

下列清單會識別有關取消註冊對等名稱的重要資訊。

-   只有註冊對等名稱的應用程式才能將其取消註冊。
-   如果呼叫 [**WSACleanup**](winsock-nsp-reference-links.md) ，就會自動取消註冊對等名稱。
-   PNRP 一律會移除整個服務名稱註冊。 不允許移除個別位址。
-   取消註冊名稱時， *essOperation* 參數的值必須為 **RNRSERVICE \_ DELETE**。
-   PNRP 不支援 **RNRSERVICE 取消 \_ 註冊** 的值。
-   *DwControlFlags* 參數必須為零 (0) 。

取消註冊名稱時， *lpqsRegInfo* 參數所參考的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

指定此結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

指定要取消註冊的對等名稱。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

必須是 **SVCID \_ PNRPNAME**。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

忽略。 設定為 **Null**。

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

必須是雲端名稱、空字串或 **Null**。 如果這個值是 **Null** 或空字串，則會使用預設的雲端 "Global"。 否則，它必須指向有效的雲端名稱。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

忽略。 設定為 **Null**。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

忽略。 設定為零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標。 **LpBlob** 結構的 **lpszIdentity** 成員會識別用來註冊對等名稱的身分識別名稱。 其餘成員必須設定為註冊名稱時所使用的相同值。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PNRP 和 BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP 和 WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP NSP 錯誤碼](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSASetService**
</dt> </dl>

 

 



