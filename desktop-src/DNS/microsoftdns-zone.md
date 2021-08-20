---
title: MicrosoftDNS_Zone 類別
description: MicrosoftDNS \_ 區域類別描述 DNS 區域。 MicrosoftDNS 區域類別的每個實例都 \_ 必須只指派給一部 DNS 伺服器。 區域可能會與多個 MicrosoftDNS \_ 網域或 MicrosoftDNS ResourceRecord 類別的實例相關聯 \_ 。
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone 類別 DNS
- MicrosoftDNS_Zone 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957177"
---
# <a name="microsoftdns_zone-class"></a>MicrosoftDNS \_ 區域類別

> [!NOTE]
> 本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。 從軟體中移除該字詞時，我們也會將其從本文中移除。

> [!NOTE]
> 本文包含「主伺服器」一詞的參考，也就是 Microsoft 不再使用的詞彙。 從軟體中移除該字詞時，我們也會將其從本文中移除。

**MicrosoftDNS \_ 區域** 類別描述 DNS 區域。 **MicrosoftDNS \_ 區域** 類別的每個實例都必須只指派給一部 DNS 伺服器。 區域可能會與多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md) 或 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ 區域** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ 區域** 類別具有這些方法。



| 方法                   | 描述                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | 啟用部分或所有非 NS 和非 SOA 記錄的過時。<br/>                                                                                                                                       |
| **ChangeZoneType**       | 變更區欄位型別。 <br/> 限定詞：實作為<br/>                                                                                                                                         |
| **CreateZone**           | 建立新的區域。 <br/> 限定詞：無。<br/>                                                                                                                                               |
| **ForceRefresh**         | 強制更新主要 DNS 伺服器的次要複本。 <br/> 限定詞：實作為<br/>                                                                                               |
| **GetDistinguishedName** | 取得區域的 DS 分辨名稱。 <br/> 限定詞：實作為<br/>                                                                                                                 |
| **PauseZone**            | 暫停區域。 <br/> 限定詞：實作為<br/>                                                                                                                                            |
| **ReloadZone**           | 重載區域。 <br/> 限定詞：實作為<br/>                                                                                                                                           |
| **ResetSecondaries**     | 重設次要 ip 位址陣列。 <br/> 限定詞：實作為<br/>                                                                                                                      |
| **ResumeZone**           | 繼續區域。 <br/> 限定詞：實作為<br/>                                                                                                                                           |
| **UpdateFromDS**         | 從目錄服務強制更新區域 (DS) 。 若要讓這個方法有效，ZoneType 必須是0。區域必須確實儲存在 DS 中。 <br/> 限定詞：實作為<br/> |
| **WriteBackZone**        | 將區域資料儲存至其區域檔案。 <br/> 限定詞：實作為、靜態<br/>                                                                                                                   |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ 區域** 類別具有這些屬性。

<dl> <dt>

**老化**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定區域的過時和清除行為。 零表示清除已停用。 停用清除時，區域中記錄的時間戳記不會重新整理，而且記錄不會被清除。 當設定為1時，會對記錄進行清除，並在伺服器收到記錄的動態更新要求時重新整理其時間戳記。 針對 Active Directory 整合的區域，此值會設定為建立區域之 DNS 伺服器的 *DefaultAgingState* 屬性。 標準主要區域的預設值為零。

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域是否接受動態更新要求。

</dd> <dt>

**自動建立**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域是否自動建立。

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定伺服器可能嘗試清除區域的時間。 即使已將區域設定為啟用清除，但在這段時間之前，DNS 伺服器不會嘗試清除此區域。 此值會設定為目前的時間加上區域的重新整理間隔（每次載入區域時）。 此參數會儲存在本機，而不會複寫至區域的其他複本。

</dd> <dt>

**檔**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域檔案的名稱。

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 WINS 記錄是否已複寫。 如果設定為 TRUE，則會停用 WINS 記錄複寫。

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定區域是否為 DS 整合。

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出當解析指定轉寄區域的名稱時，DNS 是否使用遞迴。 僅適用于條件式轉送區域。

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示在轉送區域下轉送名稱查詢的 DNS 伺服器在嘗試解決查詢本身之前，會等待轉寄站解析的時間（以秒為單位）。 此參數僅適用于轉寄區域。

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自1970年1月1日開始起算的秒數，因為區域的 SOA 序號是上次檢查時間。

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從1970年1月1日開始，自從上次從主伺服器傳送區域以來的秒數。

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此區域主要 DNS 伺服器的本機 IP 位址。 如果設定，這些主要 MasterServers 會在 Active Directory 中找到。

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此區域之主要 DNS 伺服器的 IP 位址。

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定上次更新記錄的時間戳記與重新整理時間戳記最早時間之間的時間間隔。

</dd> <dt>

**通知**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出主要區域是否會在其 Rr 資料庫中通知任何變更的次要複本。 設定為1以通知次要。

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉 DNS 伺服器 IP 位址的字串陣列，這些 IP 位址會在此區域中收到變更通知。

</dd> <dt>

**已暫停**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否暫停區域。

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定重新整理間隔，在這段期間，會將具有非零時間戳記的記錄重新整理為保留在區域中。 重新整理間隔到期尚未重新整理的記錄，可能會由伺服器執行的下一個清除作業移除。 此值絕不能小於區域中所註冊記錄的最長重新整理時間。 太小的值可能會導致移除有效的 DNS 記錄。 太大的值會延長過時記錄的存留期。 此值會設定為建立區域之 DNS 伺服器的 *DefaultRefreshInterval* 屬性。

</dd> <dt>

**Reverse**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域是否反向 (TRUE) 或轉寄 (FALSE) 。

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉 DNS 伺服器 IP 位址清單的字串陣列，這些 IP 位址允許對此區域的過時記錄進行清除。 如果未指定清單，則在符合其他必要條件時，允許區域的任何主要 DNS 伺服器會清除區域。

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉 DNS 伺服器 IP 位址的字串陣列，這些 IP 位址允許透過區域複寫接收此區域。

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否只允許區域傳輸給指定的次要資料庫。 指定的次要複本是 DNS 伺服器，其 IP 位址會列在 SecondariesIPAddressesArray 中。

</dd> <dt>

**關機**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域的複本是否已過期。 若為 TRUE，則表示區域已過期或已關閉。

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此布林值會指出區域是否使用 NBStat 反向查閱。

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出區域是否使用 WINS 查閱。

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示區域的類型。 有效值為：

-   DS 整合
-   Primary
-   次要

* * Windows Server 2003： * *

其他值：

-   快取
-   存根
-   轉寄站

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

[**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 CreateZone 方法 \_**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 PauseZone 方法 \_**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





