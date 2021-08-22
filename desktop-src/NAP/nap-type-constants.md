---
title: 'NAP 類型常數 (NapTypes .h) '
description: 已定義下列 NAP 常數。
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0201f29d19969de6050ce3eeebf29a7bee73792dcc6b61b2359e5660db12d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685918"
---
# <a name="nap-type-constants"></a>NAP 類型常數

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

已定義下列 NAP 常數。

下列 NAP 常數定義于 NapTypes 中：

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



[**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)類型長度值的最大數目 (TLV) 與 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包相關聯的物件。


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



與健全狀況聲明相關聯之 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) 物件的大小上限（以位元組為單位） ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) 封包。


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的大小下限（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的最大大小（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/sizeof (DWORD) 
</dt> <dt>



與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 DWORD 值的最大數目。


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 IPv4 位址數目上限。


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 IPv6 位址數目上限。


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構所指定之字串的最大長度。


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

 (maxStringLength + 1) \* sizeof (WCHAR) 
</dt> <dt>



[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構所指定之字串的最大長度（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



系統健全狀況實體的最大數目，例如 Shv 和 Sha。


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[範圍 (0、maxSystemHealthEntityCount) \] 
</dt> <dt>



系統健康狀態實體數目的可能值範圍。


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



強制實體的最大數目，例如 Qec。


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[範圍 (0、maxEnforcerCount) \]
</dt> <dt>



強制實體數目的可能值範圍。


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



[**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata)結構的大小上限（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



與強制實體相關聯之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 物件的最大數目。


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



所有系統健全狀況和強制實體的最大快取 SoH 連接數目。


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



指定 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)是因為新的要求而非快取的要求所致。 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)物件上的 NAP 代理程式會使用此旗標。


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



指定需要進行修正。 此旗標是由 SHA 使用。


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



[**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)結構中所包含的失敗類別目錄數目。


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



元件是隔離強制用戶端 (QEC) ，可在連線驗證期間，在頻內傳送 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包。

> [!Note]  
> Sha 和 Shv 不會使用此值。

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



元件是一種 QEC，它會執行 [**INapCertRelyingParty**](inapcertrelyingparty.md) ，而且必須與健康情況憑證伺服器互動 (HCS) 才能取得健康情況憑證。

> [!Note]  
> Sha 和 Shv 不會使用此值。

 


</dt> </dl> </dd> </dl>

下列 NAP 常數定義于 NapEnforcementClient 中。

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



SoH 封包的預設最大大小（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



SoH 封包的最大可能大小（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



SoH 封包最小可能的最大大小（以位元組為單位）。 SoH 封包的實際大小可能小於 **minProtocolMaxSize**。


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

範圍 (minProtocolMaxSize、maxProtocolMaxSize) 
</dt> <dt>



SoH 封包大小上限的可能值範圍。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                                                                |
| 標頭<br/>                   | <dl> <dt>NapTypes .h;</dt><dt>NapEnforcementClient .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NAP 常數**](nap-constants.md)
</dt> </dl>

 

 





