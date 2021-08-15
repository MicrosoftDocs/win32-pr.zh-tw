---
description: 深入瞭解：可擴充的儲存體引擎檔案
title: 可擴充的儲存體引擎檔案
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: a955da455cb2a2397010fd7869f6320970ef9f85ac1e1602f4439239dc56b167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256299"
---
# <a name="extensible-storage-engine-files"></a>可擴充的儲存體引擎檔案


_**適用于：** Windows |Windows伺服器_

## <a name="extensible-storage-engine-files"></a>可擴充的儲存體引擎檔案

可擴充的儲存體引擎會使用下列類型的檔案：

- [交易記錄檔](#transaction-log-files)

- [暫存交易記錄檔](#temporary-transaction-log-files)

- [保留的交易記錄檔](#reserved-transaction-log-files)

- [檢查點檔案](#checkpoint-files)

- [資料庫檔案](#database-files)

- [暫存資料庫](#temporary-databases)

- [清除對應檔](#flush-map-files)

下表包含由 ESE 管理之資料檔案名稱的總覽。 針對 Windows Vista 和更新版本，JET_paramLegacyNames 設定會影響所使用的檔案名。

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p>作業系統</p>
    </th>
    <th>
      <p>WindowsServer 2003 及更早版本<br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p>WindowsVista 和更新版本 (用戶端)  <br />
WindowsServer 2008 和更新版本 (server) 
</p>
    </th>
    <th>
      <p>Windows 10年度更新版和更新版本 (用戶端)  <br />
Windows Server 2016 和更新版本 (伺服器) 
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p>
        <strong>JET_paramLegacyNames 設定</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>N/A</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>無</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>JET_bitESE98FileNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>與 Windows Vista/Server 2008 相同</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>目前的記錄</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td>
      <p>&lt;inst &gt; . jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>預先初始化記錄檔</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp .log</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp. jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp .log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>輪替的記錄</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX 記錄檔</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX 在 FFFFF 切換至 &lt; inst xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 之後 jtx &gt; 。 jtx</p>
    </td>
    <td>
      <p>&lt;&gt;在 FFFFF 切換至 inst xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 之後，inst XXXXX. 記錄檔 &lt; &gt; 。</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">檢查點檔案</a>
      </p>
    </td>
    <td>
      <p>&lt;inst &gt;</p>
    </td>
    <td>
      <p>&lt;inst &gt; . jcp</p>
    </td>
    <td>
      <p>&lt;inst &gt;</p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">暫存資料庫</a>
      </p>
    </td>
    <td>
      <p>&lt;暫存資料庫檔案名 &gt; 預設： .tmp</p>
    </td>
    <td>
      <p>&lt;暫存資料庫檔案名 &gt; 預設： .tmp</p>
    </td>
    <td>
      <p>&lt;暫存資料庫檔案名 &gt; 預設： .tmp</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">保留的交易記錄檔</a>
      </p>
    </td>
    <td>
      <p>res1 .log &amp; res2</p>
    </td>
    <td>
      <p>&lt;inst &gt; RESXXXXX. jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;inst &gt; RESXXXXX. jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">資料庫檔案</a>
      </p>
    </td>
    <td>
      <p>&lt;資料庫檔案名&gt;</p>
    </td>
    <td>
      <p>&lt;資料庫檔案名&gt;</p>
    </td>
    <td>
      <p>&lt;資料庫檔案名&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">清除對應檔</a>
      </p>
    </td>
    <td>
      <p>N/A</p>
    </td>
    <td>
      <p>N/A</p>
    </td>
    <td>
      <p>N/A</p>
    </td>
    <td>
      <p>&lt;沒有副檔名的資料庫檔案名 &gt; 。 jfm</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>交易記錄檔

交易記錄檔包含對資料庫檔案的作業。 它們包含足夠的資訊，可在非預期的進程終止或系統關機之後，讓資料庫保持邏輯一致的狀態。

記錄檔的名稱相依于三個字母的基底名稱，可使用 [JET_paramBaseName](./transaction-log-parameters.md)設定。 下列範例會使用 "edb" 的基底名稱，因為這是預設的基底名稱。 交易記錄檔的副檔名會是 .log 或. jtx，視 JET_bitESE98FileNames 是否在 JET_paramLegacyFileNames 參數中設定而定。 如需詳細資訊，請參閱[可擴展的儲存體引擎系統參數](./extensible-storage-engine-system-parameters.md)。

交易記錄檔的名稱為 \<base\> \<generation-number\> .log，從1開始。 記錄產生編號採用十六進位格式。 例如，edb00001 是第一個記錄檔，而 edb000ff 則是255th 記錄。 記錄檔的記錄檔名稱中有五個十六進位數位，在1048576th 記錄檔之前，記錄檔的開頭是以11.3 格式命名 (例如 edb00100000) 。 \<base\>.log 一律是目前正在使用的記錄檔。 如果資料庫引擎不在使用中，則可以使用下列命令來識別世代的世代： **esentutl.exe-ml .edb**. a. log。

雖然交易記錄檔具有。記錄檔延伸通常與文字檔相關聯，而交易記錄檔則是二進位格式，而且不應該由使用者編輯。資料庫作業會先寫入至記錄檔。 資料可以稍後寫入資料庫檔案;可能會在稍後可能會有很多。 如果未預期的進程或系統終止，作業仍會存在於記錄檔中，而不完整的交易則可以復原。 重新執行交易記錄檔的動作稱為「 *軟* 復原」，其會在呼叫 [JetInit](./jetinit-function.md) 或 [JetInit2](./jetinit2-function.md) 時自動完成。 您也可以使用 Esentutl.exe 程式的 "-r" 選項，以手動方式執行軟復原。 在從備份還原的資料庫上重新執行交易記錄檔的動作，稱為「 *硬* 復原」。

記錄檔是固定大小，可透過 [JET_paramLogFileSize](./transaction-log-parameters.md)自訂。 當目前的記錄檔 (時，將會填入 .edb) ，它會重新命名為 \<base\> \<generation-number\> .log，而交易記錄資料流程中需要新的交易記錄檔。

每個資料庫實例都有與其相關聯的單一記錄檔順序。 WindowsXP 引進了[JetCreateInstance](./jetcreateinstance-function.md)，可讓單一進程使用多個交易記錄檔順序。 但是，不能有多個交易記錄檔順序存在於相同的目錄中。

交易記錄檔幾乎不應手動操作、重新命名、移動或刪除，因為可能會導致資料損毀。

資料庫引擎會在完整備份期間刪除交易記錄檔 (如有啟用迴圈記錄，請參閱 [JetBackup](./jetbackup-function.md)、 [JetTruncateLog](./jettruncatelog-function.md)、 [JetTruncateLogInstance](./jettruncateloginstance-function.md)) 或正常作業期間。

填滿交易記錄檔之後，資料庫引擎必須建立新的記錄檔。 迴圈記錄是一種方法，也就是資料庫引擎在損毀復原不再需要記錄檔時，會自動清除記錄檔。 此程式是將記錄檔當作執行備份的產品來移除的替代方案。 您可以使用 [JET_paramCircularLog](./transaction-log-parameters.md) 系統參數來控制迴圈記錄。 交易記錄檔不應使用任何其他方法來刪除。

### <a name="temporary-transaction-log-files"></a>暫存交易記錄檔

當 edb. log 填滿時，ESE 必須建立新的檔案。 新的記錄檔交易檔在 ESE 使用之前稱為暫存交易記錄檔。

當建立新的記錄檔，並將其大小延伸時，就會被稱為 \<base\> tmp .log。 建立新檔案可能是可能耗費成本的作業，因此 ESE 會以背景工作的方式主動建立下一個記錄檔。

由於暫存交易記錄檔是在需要新交易記錄檔的情況下建立的，因此不包含任何有用的資訊。

### <a name="reserved-transaction-log-files"></a>保留的交易記錄檔

當引擎開始允許記錄重要作業以取得正常關機時，會建立保留的交易記錄檔。

**Windows Vista：** 在 Windows Vista 和更新版本中，保留的交易記錄檔會命名為 \<base\> RESXXXXX. jrs。

**Windows Server 2003：** 在 Windows Server 2003 及更早版本中，保留的交易記錄檔會命名為 res1 .log 和 res2。

當資料庫引擎用盡磁碟空間時，就無法建立新的記錄檔。 最安全的作法是完全關閉，但仍必須記錄某些作業 (例如復原作業) 。 在這個階段中，大部分的資料庫作業都會失敗。

由於保留的交易記錄檔是在非磁片案例中，針對交易記錄檔的需要而建立的，因此不包含任何有用的資訊。

### <a name="checkpoint-files"></a>檢查點檔案

檢查點檔案會儲存特定交易記錄檔順序的檢查點。 檢查點檔案的名稱是 \<base\> .chk 或 \<base\> jcp，取決於 JET_bitESE98FileNames 是否在 JET_paramLegacyFileNames 參數中設定，而且它的位置是由 [JET_paramSystemPath](./transaction-log-parameters.md)提供。

資料庫作業會先寫入記錄檔，然後再快取到記憶體中。 稍後會將作業寫入資料庫檔案，但基於效能的考慮，作業寫入資料庫檔案的順序可能不符合最初記錄這些作業的順序。 寫入交易記錄檔的作業會處於下列其中一種狀態：

  - 寫入交易記錄檔和資料庫檔案。

  - 寫入交易記錄檔，但尚未寫入資料庫檔案。

許多資料庫作業都可以儲存在單一交易記錄檔中。 給定的記錄檔可以包含下列專案：

  - 寫入資料庫檔案的所有作業。

  - 未將任何作業寫入資料庫檔案

  - 寫入資料庫檔案和尚未寫入資料庫檔案之作業的混合作業。

檢查點指的是交易記錄資料流程中，檢查點之前所有作業都已寫入資料庫檔案的時間點。 檢查點之後發生的作業並不會有任何保證。有些可能會在記憶體中，有些則可能寫入資料庫中。

因為檢查點之前記錄檔中的所有作業都是在資料庫檔案中表示，所以只需要檢查點之後的交易記錄檔即可進行軟復原，使特定資料庫進入乾淨狀態。

### <a name="database-files"></a>資料庫檔案

資料庫檔案包含資料庫中所有資料表的架構、資料庫中所有資料表的記錄，以及資料表的索引。 其位置會使用 [JetCreateDatabase](./jetcreatedatabase-function.md)、 [JetCreateDatabase2](./jetcreatedatabase2-function.md)、 [JetAttachDatabase](./jetattachdatabase-function.md)或 [JetAttachDatabase2](./jetattachdatabase2-function.md)來提供。

只有在成功呼叫 [JetTerm](./jetterm-function.md) 或 [JetTerm2](./jetterm2-function.md)之後，資料庫才會完全關閉。

Esentutl.exe 的程式可以使用 "-mh" 選項來偵測資料庫是否已完全關閉。 例如，"esentutl.exe mh sample" 將會讀取名為 sample 之資料庫的資料庫標頭，並印出範例 .edb 的狀態。 它可能會印出「狀態：乾淨關機」或「狀態：中途關機」。

未完全關機的資料庫處於中途關機狀態。 在 Windows XP 之前，此狀態稱為「*不一致*」。 不一致的 (不一致的) 資料庫可透過軟復原進入乾淨狀態。 損毀的資料庫與 ( 「不一致」的 ) 資料庫不同。

損毀的資料庫指的是實體或邏輯損毀，而且無法使用軟修復來修正。 實體損毀可以是位翻轉，通常會由資料庫頁面上的總和檢查碼捕捉。 資料庫檔案中的總和檢查碼失敗，會將本身列為 JET_errReadVerifyFailure 錯誤。

只有完全關機的資料庫可以安全地四處移動或重新命名。 如果資料庫未完全關閉，就無法自動安全地移動或重新命名。

多個資料庫可以與單一交易記錄檔順序相關聯。

### <a name="temporary-databases"></a>暫存資料庫

暫存資料庫是用來做為 temptables 的備份存放區，而且也會在建立索引時使用。

名稱和位置會設定 [JET_paramTempPath](./temporary-database-parameters.md)。

Temptables 是使用 [JetOpenTempTable](./jetopentemptable-function.md)、 [JetOpenTempTable2](./jetopentemptable2-function.md)、 [JetOpenTempTable3](./jetopentemptable3-function.md)、 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)來建立。 它們也會由某些 API 呼叫來建立，並用來傳回架構資訊 (例如 [JetGetIndexInfo](./jetgetindexinfo-function.md)) 。

## <a name="flush-map-files"></a>清除對應檔

從 Windows 10 周年更新 (用戶端) 和 Windows Server 2016 (伺服器) ，ESE 新增額外的保護層級，以防止遺失寫入 (或遺失排清) 1，讓它能夠偵測這類事件跨進程重新 initialization2。 這項功能需要將中繼資料保存到稱為「排清對應」檔案的個別檔案。

為每個資料庫檔案建立一個排清對應檔案，而且位於相同的目錄中。 檔案的命名方式與資料庫檔案類似，但副檔名不同。 例如，如果用戶端應用程式建立具有完整路徑 C： \\ MyDirectory MyDabatase 的資料庫 \\ ，其對應的排清對應檔案為 c： \\ MyDirectory \\ MyDabatase. jfm。

這項增強功能導入了兩個資料庫檔案必須命名的需求：

  - 相同目錄中的兩個資料庫不能具有具有不同副檔名的相同檔案名。 例如： C： \\ MyDirectory \\ MyDabatase. Db1 和 C： \\ MyDirectory \\ MyDabatase db2。

  - 2 \。 資料庫不能有 jfm 副檔名。

當您手動複製或移動資料庫檔案時，其對應的排清對應檔案也應該分別複製或移至相同的目的地目錄。 如果在新的資料庫附件 (透過 [JetAttachDatabase](./jetattachdatabase-function.md)時不存在排清對應檔案，則會建立新的對應檔案，並視需要重新填入，因為頁面會從資料庫中讀取。 混合不相符的資料庫和清除對應檔案是由 ESE 處理，並強制刪除不相符的排清對應，並從頭開始重新建立。

排清對應檔案的大小會與相關聯的資料庫檔案直接成正比，大約等於 (所有大小（以位元組為單位），因此必須將結果進位至 8192) 的下一個倍數：

`8,192 + ((<database file size> / <database page size>) / 4)`

例如：針對使用32KB 頁面大小的 1.5 GB 資料庫，排清對應的近似大小為24576個位元組 (或 24KB) 。

清除對應檔必須在資料庫頁面排清時重新整理。 如果已啟用交易式記錄 (例如， [JET_paramRecovery](./transaction-log-parameters.md) 設定為 "on"，則會在用戶端應用程式對資料庫進行修改時，執行重新整理排清對應的預設) 。 平均而言，會將整個排清對應寫入至非變動媒體一次，以產生每20% 的 [JET_paramCheckpointDepthMax](./database-cache-parameters.md) 值得的交易記錄) 的位元組 (。 寫入作業的數目取決於資料庫在整個資料庫中的散發方式。 但最多可 (位元組大小) ：

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

如果已停用交易式記錄 (例如， [JET_paramRecovery](./transaction-log-parameters.md)設定為 "off" ) ，則只有在透過[JetDetachDatabase](./jetdetachdatabase-function.md)明確卸 (離資料庫時，才會重新整理排清對應一次，或者只要 (未傳遞 JET_bitTermDirty，[就會以](./jetterm2-function.md)隱含方式明確地卸離其[相關聯的](./jetterm-function.md)ESE 實例) 。

1遺失的寫入 (或遺失排清) 定義為寫入作業，該作業會從作業系統成功傳回至 ESE 資料庫引擎，但實際資料永遠不會保存到非暫時性媒體中的資料庫檔案。 這通常是因為存放裝置堆疊的故障或設定不正確所致 (軟體或硬體) 。 如果資料位於進行遺失寫入事件的區域中，用戶端應用程式可能會從需要從資料庫讀取資料的 ESE 函數收到 [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) 錯誤。

2在進程存留期內偵測遺失寫入的功能已經存在，因為 Windows 8 (用戶端) 和 Windows Server 2012 (伺服器) 。
