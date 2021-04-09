---
title: MicrosoftDNS_Server 類別
description: MicrosoftDNS \_ 伺服器類別描述 DNS 伺服器。 這個類別的每個實例都可以與一個 MicrosoftDNS 快取的實例 \_ 、一個 MicrosoftDNS \_ RootHints 的實例，以及 MicrosoftDNS 區域的多個實例相關聯 \_ 。
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server 類別 DNS
- MicrosoftDNS_Server 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933985"
---
# <a name="microsoftdns_server-class"></a>MicrosoftDNS \_ 伺服器類別

**MicrosoftDNS \_ 伺服器** 類別描述 DNS 伺服器。 這個類別的每個實例都可以與一個 MicrosoftDNS 快取的實例、一個 [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)的實例，以及 [**MicrosoftDNS \_ 區域**](microsoftdns-zone.md)的多個實例相關聯。 [**\_**](microsoftdns-cache.md)

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ 伺服器** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ 伺服器** 類別有這些方法。



| 方法                   | 描述                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | 捕獲區域的 DNS 辨別名稱。<br/>                        |
| **StartScavenging**      | 開始清除要清除之區域中的過時記錄。<br/> |
| **StartService**         | 啟動 DNS 伺服器。<br/>                                                |
| **StopService**          | 停止 DNS 伺服器。<br/>                                                 |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ 伺服器** 類別具有這些屬性。

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

回應位址要求時傳回的主機記錄數目上限。 介於5和28之間的值是有效的。

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 DNS 伺服器是否接受動態更新要求。 有效的值如下表所示。



| 值                                                                                                | 意義                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 無限制。<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 不允許對 SOA 記錄進行動態更新。<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 不允許在區域根目錄進行 NS 記錄的動態更新。<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 不允許在區域根目錄 (委派 NS 記錄) 的情況動態更新 NS 記錄。<br/> |



 

將這些值加總以決定設定值。

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否嘗試使用根伺服器的資料來更新其快取專案。 當 DNS 伺服器開機時，它需要根伺服器的 [提示] NS 的清單，以及過去稱為快取檔案的伺服器記錄。 Microsoft DNS 伺服器的功能，可讓使用者根據根伺服器的回應，嘗試寫回新的快取檔案。

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當名稱伺服器變更時，必須更新 DNS 伺服器名稱所授權的標準主要區域。 下列是有效值：



| 值                                                                                                | 意義                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 無。<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 僅允許動態更新的伺服器。<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 僅限不允許動態更新的伺服器。<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 所有伺服器。<br/>                                    |



 

預設值為 1。

* * Windows Server 2003： * *

數位3代表所有伺服器。

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

決定傳送至非 Microsoft DNS 伺服器次要資料庫時的 AXFR 訊息格式。 當設定為 TRUE 時，DNS 伺服器會以未壓縮的格式將傳輸傳送至非 Microsoft DNS 伺服器次要複本。 若為 FALSE，則會以 fast 格式傳送所有傳輸。

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器的初始化方法。 有效的值如下表所示。



| 值                                                                                                | 意義                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 初始 化。<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 從檔案開機。<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 從登錄開機。<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | 從目錄和登錄開機。<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

為此 DNS 伺服器上建立的所有 Active Directory 整合區域設定的預設 **ScavengingInterval** 值。 預設值為零，表示清除已停用。

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

無重新整理間隔（以小時為單位），設定為在此 DNS 伺服器上建立的所有 Active Directory 整合區域。 預設值為168小時 (七天) 。

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

針對在此 DNS 伺服器上建立的所有 Active Directory 整合區域，設定的重新整理間隔（以小時為單位）。 預設值為168小時 (七天) 。

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否自動建立標準反向查閱區域。

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出用來將查詢傳送到遠端 DNS 伺服器之通訊端的預設埠系結是否可以覆寫。

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器上是否有可用的 DS。

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

輪詢 DS 整合區域的間隔（以秒為單位）。

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

目錄服務整合區域中已加上邏輯化記錄的存留期（以秒為單位）。

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

快取資訊的存留期（以秒為單位），描述其他 DNS 伺服器所支援的 EDNS 版本。

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否在 DNS 伺服器上啟用應用程式目錄分割的支援。

* * Windows Server 2003： * *

這個方法的名稱是 EnableDirectoryPartitionSupport。

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

在下表中，指定 DNS 伺服器是否包含回應中的 DNSSEC 專屬 Rr、KEY、SIG 和 NXT：



| 值                                                                                                | 意義                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 除非查詢要求 DNSSEC 記錄類型的資源記錄集，否則回應中不會包含任何 DNSSEC 記錄。<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 根據 RFC 2535，DNSSEC 記錄會包含在回應中。<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 只有當原始用戶端查詢包含根據 RFC 2671 的 OPT 資源記錄時，DNSSEC 記錄才會包含在回應中<br/> |



 

如果查詢要求 DNSSEC 類型的資源記錄集，則 DNS 伺服器一律會回應這類記錄（如果有的話）。

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 DNS 伺服器的行為。 若為 TRUE，則 DNS 伺服器一律會根據 RFC 2671 以 OPT 資源記錄回應，除非遠端伺服器指出它不支援先前交換中的 EDNS。 若為 FALSE，則只有當選擇在原始查詢中傳送時，DNS 伺服器才會以選擇來回應查詢。

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器在事件檢視器系統記錄檔中所記錄的事件。 使用下列值。



| 值                                                                                                | 意義                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 無。<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 只記錄錯誤。<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 只記錄警告和錯誤。<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 記錄所有事件。<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否轉送委派子領域的查詢。

</dd> <dt>

**轉送**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

列舉 DNS 伺服器轉送查詢的轉寄站 IP 位址清單。

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

以秒為單位的時間，DNS 伺服器轉送查詢將會等待轉寄 [*站的解析，然後再*](f-gly.md) 嘗試解決查詢本身。

如果轉送伺服器未設定為使用遞迴，此值就沒有意義。 若要判斷這一點，請檢查 IsSlave 的布林值屬性。

</dd> <dt>

**IsSlave**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**如果透過** 轉寄站的名稱解析失敗，則 DNS 伺服器不使用遞迴。

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

列舉 DNS 伺服器可以接收查詢的 IP 位址清單。

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當傳回記錄時，DNS 伺服器是否將優先順序提供給本機的網路位址。

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器的偵錯工具記錄檔大小（以位元組為單位）。

</dd> <dt>

**>logfilepath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器 debug 記錄檔的檔案名和路徑。 預設值為% system32% \\ dns \\ dns .log。 相對路徑相對於% Systemroot% \\ System32。 您可以使用絕對路徑，但不支援 UNC 路徑。

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來篩選寫入至偵錯工具記錄檔之 DNS 事件的 IP 位址清單。

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出事件檢視器系統記錄檔中啟用的原則。

應根據下列演算法設定為特定值：事件檢視器系統記錄) 中 (要啟用的每個原則都會指派特定值。



| 值                                                                                                                  | 意義                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | 查詢。<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | 通知。<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Update。<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Nonquery 交易。<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | 問題。<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | 答案。<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Send。<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | 接收。<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Udp。<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP。<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | 所有封包。<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | NT 目錄服務寫入交易。<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | NT 目錄服務更新交易。<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | 完整封包。<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | 寫入。<br/>                           |



 

這個屬性會指出對應至要啟動之所有原則的值總和。

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否執行鬆散式萬用字元。 如果未定義或為零，則伺服器會遵循 DNS RFC 中指定的萬用字元行為。 在此情況下，建議系統管理員針對所有無法接收郵件的主機包含 MX 記錄。 如果是非零值，伺服器會搜尋最接近的萬用字元節點;在此情況下，系統管理員應該將 MX 記錄放在區域根目錄和萬用字元節點 ( ' \* ' ) 直接放在區域根目錄正下方。 此外，系統管理員也應該在接收自己的郵件的主機上放置自我參考的 MX 記錄。

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

遞迴名稱查詢的記錄可能會保留在 DNS 伺服器快取中的最長時間（以秒為單位）。 當此專案的值到期時，DNS 伺服器會從快取中刪除記錄，即使記錄中的 TTL 欄位值較大也是如此。

這個屬性的預設值為86400秒 (1 天) 。

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

遞迴查詢中名稱錯誤結果的最長時間（以秒為單位）可能會保留在 DNS 伺服器快取中。 當此計時器過期時，DNS 會刪除快取中的記錄，即使 TTL 欄位更大也是如此。 預設值為 86400 (一天) 。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

DNS 伺服器的完整功能變數名稱 (FQDN) 或 IP 位址。

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出要在 DNS 名稱中使用的一組合格字元。 使用下列值。



| 值                                                                                                | 意義                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Strict RFC (ANSI) <br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 非 RFC (ANSI) <br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | 多位元組 (UTF8) <br/>  |



 

* * Windows Server 2003： * *

"2" 的值表示「任何」。

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否執行遞迴查詢。 TRUE 表示不執行遞迴查詢。

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

重試遞迴查閱之前經過的秒數。 如果屬性未定義或為零，則會在三秒後進行重試。 不建議使用者變更此屬性。 在某些情況下，應該變更屬性;其中一個範例是當 DNS 伺服器透過低速連結將遠端伺服器連線，而且 DNS 伺服器在接收來自遠端 DNS 的回應之前正在重試。 在此情況下，比起從遠端 DNS 觀察到的回應時間，將時間提高一點會很合理。

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器放棄遞迴查詢之前經過的秒數。 如果屬性未定義或為零，則 DNS 伺服器會在15秒後放棄。 一般來說，有15秒的時間足以讓任何未完成的回應恢復到 DNS 伺服器。

不建議使用者變更此屬性。 其中一個內容應變更的情況是，當 DNS 伺服器透過低速連結將遠端伺服器連線，而且觀察到 DNS 伺服器在 \_ 收到回應之前拒絕伺服器失敗) 的查詢 (。

用戶端解析程式也會重試查詢，因此需要仔細調查，以判斷遠端回應是否真的與超時的查詢相關聯。在此情況下，將超時值提高為比從遠端 DNS 觀察到的回應時間稍微長一點，是合理的。

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否四捨五入 robins 多個記錄。

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來執行管理 RPC 的 RPC 通訊協定或通訊協定。 下列演算法用來指派特定值：



| 值                                                                                                | 意義                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 無<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 具名管道<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Lpc<br/>         |



 

值的總和表示使用的通訊協定。

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器所執行的兩個連續清除作業之間的間隔時間（以小時為單位）。 零表示清除已停用。 預設值為168小時 (七天) 。

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否以獨佔方式將名稱記錄儲存在與提供它們的伺服器相同的子樹中。

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器將 UDP 查詢傳送到其他伺服器的埠。 根據預設，DNS 伺服器會在系結至 DNS 埠的通訊端上傳送查詢。

在某些情況下，這不是最佳的設定。 其中一個明顯的情況是當系統管理員封鎖具有防火牆的 DNS 埠以防止外部存取 DNS 伺服器，但仍希望伺服器能夠連線到網際網路 DNS 伺服器，以提供內部用戶端的名稱解析。 另一種情況是當 DNS 伺服器支援不連續的神經網路時 (屬性 **DisjointNets** 設定為 TRUE 會識別此案例) 。 在這些情況下，將 **SendOnNonDnsPort** 屬性設定為非零值，會指示 DNS 伺服器系結至任意埠，以傳送至遠端 DNS 伺服器。

如果 **SendOnNonDnsPort** 值大於1024，DNS 伺服器會明確地系結至指定的埠值。 當系統管理員需要針對防火牆用途修正 DNS 查詢埠時，此設定選項會很有用。

* * Windows Server 2003： * *

將 [傳送埠] 屬性設定為非零值，會導致 DNS 伺服器系結至任意埠，以傳送至遠端 DNS 伺服器。

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉 DNS 伺服器的 IP 位址清單。

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 DNS 伺服器是否嚴格剖析 [*區域*](z-gly.md) 檔案。 如果未定義或為零，伺服器會記錄並忽略區域檔案中的錯誤資料，並繼續載入。 如果是非零值，伺服器將會記錄並因區域檔案錯誤而失敗。

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限制可在伺服器上動態更新的記錄類型，除了伺服器和區域物件上的 **AllowUpdate** 設定以外，還會用到它。

* * Windows Server 2003： * *

0：沒有限制。

1：不允許對 SOA 記錄進行動態更新。

2：不允許在區域根目錄進行 NS 記錄的動態更新。

4：不允許不在區域根 (委派 NS 記錄) 的 NS 記錄進行動態更新。

將這些值加總以決定設定值。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

DNS 伺服器的版本。

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 DNS 伺服器是否會在成功回應時，將 NS 和 SOA 記錄寫入授權單位區段。

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

DNS 伺服器在嘗試區域傳輸時，等候遠端伺服器的 TCP 連線成功的時間（以秒為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS 伺服器類別的 StartService 方法 \_**](microsoftdns-server-startservice.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 StopService 方法 \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





