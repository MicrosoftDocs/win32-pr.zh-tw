---
description: 深入瞭解：資源參數
title: 資源參數
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac1a6aba2eda729c3e705cf5acdda837c2670564
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472444"
---
# <a name="resource-parameters"></a>資源參數


_**適用于：** Windows |Windows伺服器_

## <a name="resource-parameters"></a>資源參數

本主題包含用於資源的參數。

*JET_paramCachedClosedTables*  
125  

此參數會控制應用程式已關閉實例所代表的資料表之後，該實例所快取的 B + 樹系資源數目。

此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。 對於具有極大量資料表之架構的應用程式而言，這非常有用。


| | | <p>預設值：3</p> | <p>64</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1–2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsVista 和更新版本</p> | 



*JET_paramDisablePerfmon*  
107  

您可以使用這個參數來防止資料庫引擎將其效能的相關資料發佈至 Windows。 這樣做可以減少資料庫引擎的服務執行緒活動。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>否</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsVista 和更新版本</p> | 



*JET_paramGlobalMinVerPages*  
81  

此參數可讓在多重實例模式中運作的應用程式預先配置記憶體給全域集區中的版本頁面，以模擬較舊的行為。 如果應用程式想要保證特定大小的交易稍後可能會成功，即使記憶體變得很少，這項功能就很有用。

**Windows 2000：** 在 [JetInit](./jetinit-function.md)時，一律會保留足夠的記憶體來備份所有版本頁面。

**Windows XP：** 從 Windows XP，在單一實例模式中，這仍然是 true。 不過，在多重實例模式中時，會以動態方式配置版本頁面記憶體。


| | | <p>預設值：3</p> | <p>64</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1–2147483647</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>否</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>是</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramMaxCursors*  
8  

此參數會保留所要求的資料指標資源數目，供實例使用。 資料指標資源直接對應至 [JET_TABLEID](./jet-tableid.md) 資料類型。 此設定會影響可同時使用的資料指標數目。 不同的會話無法共用資料指標資源，因此這個參數必須設定為夠大的值，讓每個會話可以使用所需的資料指標數目。

**Windows 2000、Windows XP 和 Windows Server 2003：** 此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。


| | | <p>預設值：3</p> | <p>1024</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramMaxInstances*  
104  

此參數會控制可在單一進程中建立的實例數目上限。


| | | <p>預設值：3</p> | <p>16</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1-1024</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>否</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramMaxOpenTables*  
6  

此參數會保留要求的 B + 樹狀結構資源數目，以供實例使用。 此設定會影響可同時使用的資料表數目。 此參數必須相對於資料庫引擎所使用之資料庫的實體架構進行設定，如此一來，這項設定就不會像它一樣簡單。

一般情況下，每個資料表的每個次要索引都需要兩個資源，再加上一個資源，同時應用程式同時使用。

**Windows 2000、Windows XP 和 Windows Server 2003：** 此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。


| | | <p>預設值：3</p> | <p>300</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramMaxSessions*  
5  

此參數會保留實例所用的要求會話資源數目。 會話資源直接對應至 [JET_SESID](./jet-sesid.md) 資料類型。 此設定會影響可同時使用的會話數目。

**Windows 2000、Windows XP 和 Windows Server 2003：** 此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。


| | | <p>預設值：3</p> | <p>16</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-30000</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramMaxTemporaryTables*  
10  

此參數會保留所要求的臨時表資源數目，供實例使用。 此設定會影響可同時使用的臨時表數目。

**Windows 2000、Windows XP 和 Windows Server 2003：** 此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。

**Windows XP 和更新版本：** 如果這個系統參數設定為零，則不會建立暫存資料庫，而且任何需要使用暫存資料庫的活動都將會失敗。 這項設定有助於避免建立暫存資料庫所需的 i/o （如果已知不會使用）。

**注意**  使用臨時表也需要資料指標資源。


| | | <p>預設值：3</p> | <p>20</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>是</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramMaxVerPages*  
9  

此參數會保留實例所使用的版本存放區頁面所要求的數目。 版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。 這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。 這項設定會影響一次可以保留在記憶體中的更新數目。 這將會影響單一交易可執行檔更新數目上限、交易可保持開啟的最大持續時間、在系統上更新交易的最大並行載入，或是這些的組合。

此參數所設定的每個版本存放區頁面，在32位電腦上的大小為16KB，而在64位電腦上則為32KB。

**Windows Vista 和更新版本：** 版本存放區頁面大小可透過 JET_paramVerPageSize 讀取及變更。

**Windows 2000、Windows XP 和 Windows Server 2003：** 此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。

**注意**  這是最常用於資料庫引擎的資源。 請注意，必須將系統參數的設定以及應用程式的交易式負載的設定付費，以避免在正常操作下耗盡此資源。 當此資源耗盡時，資料庫的更新將會遭到拒絕，並 JET_errVersionStoreOutOfMemory。 若要釋放其中一些資源，最舊的未完成交易必須中止。


| | | <p>預設值：3</p> | <p>64</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1–2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>是</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramPageHintCacheSize*  
101  

此參數會控制特殊快取的大小，用來加速查閱資料庫頁面快取中 B + 樹狀目錄的子頁面指標。 快取的大小是以位元組為單位。


| | | <p>預設值：3</p> | <p>262144</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>是</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

此參數會嘗試將 B + 樹系資源的數目維持在低於指定的臨界值。

如果此參數設定為零，則會預設為100% 的 **JET_paramMaxOpenTables**。

**Windows Vista 和更新版本：** 此參數已過時，且不會影響資料庫引擎的操作。 應用程式應該改用 JET_paramMaxCachedClosedTables。


| | | <p>預設值：3</p> | <p>0 (100% 的 <strong>JET_paramMaxOpenTables</strong>) </p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramPreferredVerPages*  
63  

此參數代表一個相對於 **JET_paramMaxVerPages** 的臨界值，可控制 database engine 任意使用版本頁面。 如果版本存放區的大小超過此臨界值，則只會針對選擇性的背景工作（例如回收資料庫中已刪除的空間）使用任何資訊，而不會犧牲保存交易資訊的空間。

**Windows 2000、Windows XP 和 Windows Server 2003：** 將此參數設定為零會將臨界值設定為90% 的 **JET_paramMaxVerPages**。

**Windows Vista 和更新版本：** 已不再支援此參數，且此參數的預設值已變更，以闡明其行為。

此參數所設定的每個版本存放區頁面，在32位電腦上的大小為16KB，而在64位電腦上則為32KB。

**Windows Vista 和更新版本：** 版本存放區頁面大小可透過 JET_paramVerPageSize 讀取及變更。

**注意**  如果資料庫引擎太過頻繁地操作此閾值，則資料庫可能會降低效能。 發生這種情況的原因是，清除資料庫的背景進程無法正常運作，而不需要在此案例中擲回的選擇性資訊。 線上或離線磁碟重組將會阻礙此效果。


| | | <p>預設值：3</p> | <p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 0 (90% 的 JET_paramMaxVerPages) </p><p><strong>Windows Vista：</strong> 58</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1–2147483647</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>是</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>是</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramVerPageSize*  
128  

此參數可控制 database engine 用來保存交易資訊的版本存放區頁面大小。 此參數的值是版本頁面的所有其他系統參數的單位大小 (例如 JET_paramMaxVerPages) 。

資料庫引擎可能會選擇使用比要求更大的版本存放區頁面大小。


| | | <p>預設值：3</p> | <p>16384</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>1024、2048、4096、8192、16384、32768、65536</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>否</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsVista 和更新版本</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

此參數會控制可以在任何時間佇列至 database engine 執行緒集區的背景清除工作專案數目。


| | | <p>預設值：3</p> | <p>32</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p><strong>Windows XP 和 Windows Server 2003：</strong> 1 –63</p><p><strong>Windows Vista：</strong> 1-127</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p><strong>Windows XP 和 Windows Server 2003：</strong> 不</p><p><strong>Windows Vista：</strong> 是的</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
