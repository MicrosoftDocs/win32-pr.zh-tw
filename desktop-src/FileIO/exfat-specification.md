---
description: ExFat 檔案系統的規格。
title: exFAT 檔案系統規格
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 62c51daff1aba3c9416cd5368e1b92570a377c208256b57ef5154d5e24433e4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050988"
---
# <a name="exfat-file-system-specification"></a>exFAT 檔案系統規格

## <a name="1-introduction"></a>1 簡介

ExFAT 檔案系統是 FAT32 在 FAT 檔案系統中的後續版本。 此規格描述 exFAT 檔案系統，並提供執行 exFAT 檔案系統所需的所有資訊。

### <a name="11-design-goals"></a>1.1 設計目標

ExFAT 檔案系統有三個集中設計目標 (請參閱以下) 的清單。

1. *保留以 FAT 為基礎之檔案系統的簡潔性。*

   > FAT 型檔案系統的兩大優點是它們的相對簡單和簡化。 在其前身的精神中，實作者應該發現 exFAT 相當簡單，而且易於實行。

2. *啟用非常大型的檔案和存放裝置。*

   > ExFAT 檔案系統會使用64位來描述檔案大小，進而啟用相依于大型檔案的應用程式。 ExFAT 檔案系統也可讓叢集大到32MB，有效啟用極大型的儲存裝置。

3. *納入擴充性以進行未來的創新。*

   > ExFAT 檔案系統將擴充性納入其設計中，讓檔案系統能夠與儲存體中的創新和使用方式的變更保持一致。

### <a name="12-specific-terminology"></a>1.2 特定術語

在此規格的內容中，特定詞彙 (請參閱 [表 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) 針對 exFAT 檔案系統的設計和執行提供特定意義。

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**「表1」定義具有非常明確意義的詞彙**

<table>
<thead>
<tr class="header">
<th><strong>字詞</strong></th>
<th><strong>[定義]</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>應向</td>
<td>此規格會使用「應有」詞彙來描述強制性的行為。</td>
</tr>
<tr class="even">
<td>應該</td>
<td>此規格會使用「應該」一詞來描述強烈建議的行為，但不會強制執行。</td>
</tr>
<tr class="odd">
<td>五月</td>
<td>此規格使用「可能」一詞來描述選擇性的行為。</td>
</tr>
<tr class="even">
<td>強制性</td>
<td>此字詞描述的欄位或結構，是由實作為此規格所描述的進行修改，並應加以解讀。</td>
</tr>
<tr class="odd">
<td>選擇性</td>
<td>此詞彙描述可能或可能不支援的欄位或結構。 如果實作為支援指定的選擇性欄位或結構，則它應該修改，而且應該在此規格中解讀此欄位或結構。</td>
</tr>
<tr class="even">
<td>未定義</td>
<td>此詞彙描述可視需要修改的欄位或結構內容 (例如，在設定周圍欄位或) 結構時，清除為零，則不應解讀以保存任何特定意義。</td>
</tr>
<tr class="odd">
<td>保留</td>
<td><p>此字詞描述執行下列各項的欄位或結構內容：</p>
<ol type="1">
<li><p>應初始化為零，而且不應該用於任何用途</p></li>
<li><p>除非計算總和檢查碼，否則不應解讀</p></li>
<li><p>應該在修改周圍欄位或結構的作業之間保留</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1.3 共通字的全文檢索

此規格在個人電腦產業中使用一般用途的縮寫 (請參閱 [ [表 2](#table-2-full-text-of-common-acronyms) ]) 。

<div id="table-2-full-text-of-common-acronyms" />

**表2共通的全文本縮寫**

| **縮略字** | **全文檢索**                                      |
|-------------|----------------------------------------------------|
| ASCII       | 美國訊息交換標準代碼 (ASCII)  |
| BIOS        | 基本輸入輸出系統                          |
| CPU         | 中央處理單位                            |
| exFAT       | 可擴充的檔案配置表                   |
| FAT         | 檔案配置表                              |
| FAT12       | 檔案配置表，12位叢集索引      |
| FAT16       | 檔案配置表，16位叢集索引      |
| FAT32       | 檔案配置表，32位叢集索引      |
| GPT         | GUID 磁碟分割表格                               |
| GUID        | 全域唯一識別碼 (請參閱 [10.1 節](#101-globally-unique-identifiers-guids))       |
| INT         | 中斷                                          |
| MBR         | 主開機記錄                                 |
| texFAT      | 交易安全 exFAT                             |
| UTC         | 國際標準時間                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1.4 預設欄位和結構限定詞

此規格中的欄位和結構具有下列限定詞 (請參閱以下) 的清單，除非指定其他規格的附注。

1. 未簽署

2. 使用小數點標記法來描述值，如果未另行注明則為。此規格會使用修正後字母 "h" 來表示十六進位數位，並將 Guid 括在大括弧中

3. 以位元組由小到大格式

4. 字串不需要以 null 結尾的字元

### <a name="15-windows-ce-and-texfat"></a>1.5 Windows CE 和 TexFAT

TexFAT 是 exFAT 的延伸模組，可在基底檔案系統之上新增交易安全操作的語法。 Windows CE 會使用 TexFAT。
TexFAT 需要使用兩個 FATs 和配置點陣圖，才能在交易中使用。 它也會定義數個額外的結構，包括填補描述項和安全描述項。

## <a name="2-volume-structure"></a>2個磁片區結構

磁片區是儲存和取出使用者資料所需的所有檔案系統結構和資料空間的集合。 所有 exFAT 磁片區都包含四個區域 (請參閱 [表 3](#table-3-volume-structure)) 。

<div id="table-3-volume-structure" />

**表3磁片區結構**

<table>
<thead>
<tr class="header">
<th><strong>子領域名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (磁區) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (磁區) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>主要開機區域</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>主要開機磁區</td>
<td>0</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#31-main-and-backup-boot-sector-sub-regions">區段 3.1</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>主要延伸的開機磁區</td>
<td>1</td>
<td>8</td>
<td>此子領域是必要的，且 <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">區段 3.2</a>) 定義其內容。</td>
</tr>
<tr class="even">
<td>主要 OEM 參數</td>
<td>9</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#33-main-and-backup-oem-parameters-sub-regions">區段 3.3</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>主要保留</td>
<td>10</td>
<td>1</td>
<td>此子領域是強制性的，且其內容為保留。</td>
</tr>
<tr class="even">
<td>主要開機總和檢查碼</td>
<td>11</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#34-main-and-backup-boot-checksum-sub-regions">區段 3.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td><strong>備份開機區域</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>備份開機磁區</td>
<td>12</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#31-main-and-backup-boot-sector-sub-regions">區段 3.1</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>備份擴充的開機磁區</td>
<td>13</td>
<td>8</td>
<td>此子領域是必要的，且 <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">區段 3.2</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>備份 OEM 參數</td>
<td>21</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#33-main-and-backup-oem-parameters-sub-regions">區段 3.3</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>備份保留</td>
<td>22</td>
<td>1</td>
<td>此子領域是強制性的，且其內容為保留。</td>
</tr>
<tr class="even">
<td>備份開機總和檢查碼</td>
<td>23</td>
<td>1</td>
<td>此子領域是必要的，且 <a href="#34-main-and-backup-boot-checksum-sub-regions">區段 3.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td><strong>FAT 區域</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>FAT 對齊</td>
<td>24</td>
<td>FatOffset –24</td>
<td><p>此子領域是必要的，而且其內容（如果有的話）不會定義。</p>
<p>注意：主要和備份開機磁區都包含 FatOffset 欄位。</p></td>
</tr>
<tr class="odd">
<td>第一個 FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>此子領域是必要的，且 <a href="#41-first-and-second-fat-sub-regions">區段 4.1</a> 會定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 FatOffset 和 FatLength 欄位。</p></td>
</tr>
<tr class="even">
<td>第二個 FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1) </td>
<td><p>此子領域是必要的，且 <a href="#41-first-and-second-fat-sub-regions">區段 4.1</a> 會定義其內容（如果有的話）。</p>
<p>注意：主要和備份開機磁區都包含 FatOffset、FatLength 和 NumberOfFats 欄位。 NumberOfFats 欄位只能保留值1和2。</p></td>
</tr>
<tr class="odd">
<td><strong>資料區域</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>叢集堆積對齊</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOfFats) </td>
<td><p>此子領域是必要的，而且其內容（如果有的話）不會定義。</p>
<p>注意：主要和備份開機磁區都包含 FatOffset、FatLength、NumberOfFats 和 ClusterHeapOffset 欄位。 NumberOfFats 欄位的有效值為1和2。</p></td>
</tr>
<tr class="odd">
<td>叢集堆積</td>
<td>ClusterHeapOffset</td>
<td>ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td><p>此子領域是必要的，且 <a href="#51-cluster-heap-sub-region">區段 5.1</a> 會定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 ClusterHeapOffset、ClusterCount 和 SectorsPerClusterShift 欄位。</p></td>
</tr>
<tr class="even">
<td>多餘的空間</td>
<td>ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup>) </td>
<td><p>此子領域是必要的，而且其內容（如果有的話）不會定義。</p>
<p>注意：主要和備份開機磁區都包含 ClusterHeapOffset、ClusterCount、SectorsPerClusterShift 和 VolumeLength 欄位。</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3個主要和備份開機區域

主要開機區域會提供所有必要的開機搭接接指令、識別資訊和檔案系統參數，讓執行執行下列動作：

1. 從 exFAT 磁片區將電腦系統開機。

2. 將磁片區上的檔案系統識別為 exFAT。

3. 探索 exFAT 檔案系統結構的位置。

備份開機區域是主要開機區域的備份。 當主要開機區域處於不一致的狀態時，它會協助復原 exFAT 磁片區。 除非在罕見的情況下（例如更新開機搭接接指令），否則不應該修改備份開機區域的內容。

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3.1 主要和備份開機磁區子領域

主要開機磁區包含搭接接自 exFAT 磁片區的開機程式碼，以及描述磁片區結構的基本 exFAT 參數， (參閱 [表 4](#table-4-main-and-backup-boot-sector-structure)) 。 BIOS、MBR 或其他開機搭接接代理程式可能會檢查此磁區，而且可能會載入並執行其中所包含的任何開機搭接接指示。

備份開機磁區是主要開機磁區的備份，而且具有相同的結構 (請參閱 [ [表 4](#table-4-main-and-backup-boot-sector-structure) ]) 。 備份開機磁區可協助復原作業;但是，執行應該會將 VolumeFlags 和 PercentInUse 欄位的內容視為過時。

在使用主要或備份開機磁區的內容之前，必須先驗證其各自的開機總和檢查碼，並確保其所有欄位都在有效的值範圍內，藉以驗證它們的內容。

初始格式作業將會初始化主要和備份開機磁區的內容，而執行程式可能會 (更新這些磁區，而且也應該視需要更新其各自的開機總和檢查碼) 。 不過，執行可能會更新 VolumeFlags 或 PercentInUse 欄位，而不會更新其各自的開機總和檢查碼， (總和檢查碼明確地排除這兩個欄位) 。

<div id="table-4-main-and-backup-boot-sector-structure" />

**表4主要和備份開機磁區結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>此為必要欄位，而且 <a href="#311-jumpboot-field">區段 3.1.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#312-filesystemname-field">區段 3.1.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>此為必要欄位，而且 <a href="#313-mustbezero-field">區段 3.1.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#314-partitionoffset-field">區段 3.1.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>此為必要欄位，而 <a href="#315-volumelength-field">3.1.5 區段</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#316-fatoffset-field">區段 3.1.6</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#317-fatlength-field">區段 3.1.7</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#318-clusterheapoffset-field">區段 3.1.8</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>ClusterCount</td>
<td>92</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#319-clustercount-field">區段 3.1.9</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3110-firstclusterofrootdirectory-field">區段 3.1.10</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3111-volumeserialnumber-field">區段 3.1.11</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#3112-filesystemrevision-field">區段 3.1.12</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#3113-volumeflags-field">區段 3.1.13</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#3114-bytespersectorshift-field">區段 3.1.14</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#3115-sectorsperclustershift-field">區段 3.1.15</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#3116-numberoffats-field">區段 3.1.16</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#3117-driveselect-field">區段 3.1.17</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#3118-percentinuse-field">區段 3.1.18</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>保留</td>
<td>113</td>
<td>7</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="even">
<td>代碼</td>
<td>120</td>
<td>390</td>
<td>此為必要欄位，而且 <a href="#3119-bootcode-field">區段 3.1.19</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#3120-bootsignature-field">區段 3.1.20</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> –512</td>
<td><p>此為必要欄位，而且其內容（如果有的話）未定義。</p>
<p>注意：主要和備份開機磁區都包含 BytesPerSectorShift 欄位。</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot 欄位

JumpBoot 欄位必須包含個人電腦中常見 Cpu 的跳躍指示，在執行時，會在執行程式碼欄位中「跳過」 CPU 來執行開機搭接接指令。

此欄位的有效值是依低序位位元組至高序位位元組) EBh 76h 90h 的順序 (。

#### <a name="312-filesystemname-field"></a>3.1.2 FileSystemName 欄位

FileSystemName 欄位應包含磁片區上檔案系統的名稱。

此欄位的有效值為 ASCII 字元 "EXFAT"，其中包含三個尾端空白字元。

#### <a name="313-mustbezero-field"></a>3.1.3 MustBeZero 欄位

MustBeZero 欄位應該會直接對應到封裝 BIOS 參數區塊在 FAT12/16/32 磁片區上使用的位元組範圍。

此欄位的有效值為0，這有助於防止 FAT12/16/32 的執行錯誤地裝載 exFAT 的磁片區。

#### <a name="314-partitionoffset-field"></a>3.1.4 PartitionOffset 欄位

PartitionOffset 欄位應描述裝載指定 exFAT 磁片區之分割區的媒體相關磁區位移。 此欄位使用個人電腦上的外延 INT 13h，協助搭接接從磁片區進行開機。

此欄位的所有可能值都是有效的;不過，值0表示實值應忽略此欄位。

#### <a name="315-volumelength-field"></a>3.1.5 VolumeLength 欄位

VolumeLength 欄位必須描述指定之 exFAT 磁片區在磁區中的大小。

此欄位的有效值範圍應為：

- 至少 2<sup>20</sup>/2<sup>BytesPerSectorShift</sup>，可確保最小的磁片區小於1mb

- 最大值為 2<sup>64</sup>-1，此欄位可描述的最大值

但是，如果多餘空間子領域的大小為0，則此欄位的值為 ClusterHeapOffset + (2<sup>32</sup>-11) \* 2<sup>SectorsPerClusterShift</sup>。

#### <a name="316-fatoffset-field"></a>3.1.6 FatOffset 欄位

FatOffset 欄位應描述第一個 FAT 的磁片區相對磁區位移。 此欄位可讓您將第一個 FAT 對齊基礎儲存媒體的特性。

此欄位的有效值範圍應為：

- 至少24，主要開機和備份開機區域所耗用的磁區帳戶

- 最多 ClusterHeapOffset- (FatLength \* NumberOfFats) ，其為叢集堆積所耗用的磁區帳戶

#### <a name="317-fatlength-field"></a>3.1.7 FatLength 欄位

FatLength 欄位應描述每個 FAT 資料表的長度（以磁區為限） (磁片區最多可包含兩個 FATs) 。

此欄位的有效值範圍應為：

- 至少 (ClusterCount + 2) \* 2<sup>2</sup>/2<sup>BytesPerSectorShift</sup>進位至最接近的整數，以確保每個 FAT 都有足夠的空間來描述叢集堆積中的所有群集

- 最多 (ClusterHeapOffset FatOffset) /NumberOfFats 四捨五入至最接近的整數，以確保 FATs 存在於叢集堆積之前

這個欄位可能會包含超出其下限 (的值，如上面所述) 若要啟用第二個 FAT （如果有的話）也會對齊基礎儲存體媒體的特性。 未定義空間的內容，超過 FAT 本身需要的內容（如果有的話）。

#### <a name="318-clusterheapoffset-field"></a>3.1.8 ClusterHeapOffset 欄位

ClusterHeapOffset 欄位應描述叢集堆積的磁片區相對磁區位移。 此欄位可讓您將叢集堆積對齊基礎儲存媒體的特性。

此欄位的有效值範圍應為：

- 至少 FatOffset + FatLength \* NumberOfFats，以考慮上述所有區域所耗用的磁區

- 最多2個<sup>32</sup>-1 或 VolumeLength- (ClusterCount \* 2<sup>SectorsPerClusterShift</sup>) ，以較少的計算

#### <a name="319-clustercount-field"></a>3.1.9 ClusterCount 欄位

ClusterCount 欄位應描述叢集堆積包含的叢集數目。

此欄位的有效值應為下列較小的值：

-  (VolumeLength-ClusterHeapOffset) /2<sup>SectorsPerClusterShift</sup>四捨五入到最接近的整數，也就是叢集堆積和磁片區結尾之間可容納的叢集數目

- 2<sup>32</sup>-11，也就是 FAT 可以描述的叢集數目上限

ClusterCount 欄位的值會決定 FAT 的大小下限。 為了避免極度龐大的 FATs，可透過 [SectorsPerClusterShift] 欄位) 增加叢集大小 (，藉以控制叢集中的叢集數目。 此規格建議在叢集堆積中不超過2個<sup>24</sup>-2 的叢集。 不過，在叢集中，執行應該能夠處理最多有2個<sup>32</sup>-11 個叢集的磁片區。

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 FirstClusterOfRootDirectory 欄位

FirstClusterOfRootDirectory 欄位必須包含根目錄第一個叢集的叢集索引。 當配置點陣圖和向上案例資料表耗用叢集之後，執行的每一項工作都應該盡力將根目錄的第一個叢集放在第一個非錯誤的叢集中。

此欄位的有效值範圍應為：

- 至少2個叢集堆積中第一個叢集的索引

- 最多 ClusterCount + 1，也就是叢集堆積中最後一個叢集的索引

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 VolumeSerialNumber 欄位

VolumeSerialNumber 欄位必須包含唯一的序號。 這可協助您區分不同的 exFAT 磁片區。
執行程式應結合 exFAT 磁片區格式化的日期和時間，以產生序號。 結合日期和時間以形成序號的機制是實特定的。

此欄位的所有可能值都是有效的。

#### <a name="3112-filesystemrevision-field"></a>3.1.12 FileSystemRevision 欄位

FileSystemRevision 欄位必須描述指定磁片區上 exFAT 結構的主要和次要修訂編號。

高序位位元組是主要修訂編號，低序位位元組是次要修訂編號。 例如，如果高序位位元組包含值01h，而且低序位位元組包含值05h，則 FileSystemRevision 欄位會描述修訂編號1.05。
同樣地，如果高序位位元組包含值0Ah，且低序位位元組包含值0Fh，則 FileSystemRevision 欄位會描述修訂編號10.15。

此欄位的有效值範圍應為：

- 低序位位元組至少為0，高序位位元組為1

- 高序位位元組的低序位位元組和99最多99

此規格所描述的 exFAT 修訂編號為1.00。
此規格的執行應該裝載任何具有主要修訂編號1的 exFAT 磁片區，而且不應該掛接任何其他主要修訂編號的 exFAT 磁片區。 執行作業應接受次要修訂編號，且不會執行作業或建立任何未在指定的次要修訂編號的對應規格中描述的檔案系統結構。

#### <a name="3113-volumeflags-field"></a>3.1.13 VolumeFlags 欄位

VolumeFlags 欄位必須包含旗標，指出 exFAT 磁片區上各種檔案系統結構的狀態 (參閱 [表 5](#table-5-volumeflags-field-structure)) 。

在計算其各自的主要開機或備份開機區域總和檢查碼時，不應包含此欄位。 參考備份開機磁區時，執行應該會將此欄位視為過時。

<div id="table-5-volumeflags-field-structure" />

**表 5 VolumeFlags 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#31131-activefat-field">區段 3.1.13.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#31132-volumedirty-field">區段 3.1.13.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#31133-mediafailure-field">區段 3.1.13.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#31134-cleartozero-field">區段 3.1.13.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>保留</td>
<td>4</td>
<td>12</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 ActiveFat 欄位

ActiveFat 欄位應該會說明哪些 FAT 和配置點陣圖是作用中的 (而實作為應使用) ，如下所示：

- 0，表示第一個 FAT 和第一個配置點陣圖為作用中

- 1，這表示第二個 FAT 和第二個配置點陣圖為使用中，而且只有在 NumberOfFats 欄位包含值2時，才可能使用

實作為應將非使用中的 FAT 和配置點陣圖視為過時。 只有 TexFAT 感知的執行應該切換使用中的 FAT 和配置點陣圖 (請參閱 [7.1) 一節](#71-allocation-bitmap-directory-entry) 。

##### <a name="31132-volumedirty-field"></a>3.1.13.2 VolumeDirty 欄位

VolumeDirty 欄位應描述磁片區是否已變更，如下所示：

- 0，表示磁片區可能處於一致的狀態

- 1，表示磁片區可能處於不一致的狀態

在遇到無法解析的檔案系統中繼資料不一致時，實值應該將此欄位的值設定為1。 如果在裝載磁片區時，此欄位的值為1，則只有解析檔案系統中繼資料不一致的執行程式可能會將此欄位的值清除為0。 這類的執行應該只在確定檔案系統處於一致狀態之後，才將此欄位的值清除為0。

如果在裝載磁片區時，此欄位的值為0，則在更新檔案系統中繼資料之前，應該將此欄位設定為1，並在之後將此欄位清除為0，類似于 [8.1 章節](#81-recommended-write-ordering)中所述的建議寫入順序。

##### <a name="31133-mediafailure-field"></a>3.1.13.3 MediaFailure 欄位

MediaFailure 欄位應描述某個執行是否發現媒體失敗，如下所示：

- 0，表示裝載媒體尚未回報失敗，或任何已知的失敗都已記錄在 FAT 中為「不當」叢集

- 1，這表示裝載媒體已回報失敗 (亦即，讀取或寫入作業失敗) 

執行時，應該將此欄位設為1：

1. 裝載媒體無法嘗試存取磁片區中的任何區域

2. 此執行已用盡存取重試演算法（如果有的話）

如果在裝載磁片區時，此欄位的值為1，則為掃描整個磁片區以進行媒體故障的執行，並將所有失敗記錄為 FAT (的「不良」叢集，或以其他方式解決媒體失敗) 可能會將此欄位的值清除為0。

##### <a name="31134-cleartozero-field"></a>3.1.13.4 ClearToZero 欄位

ClearToZero 欄位在此規格中沒有重大意義。

此欄位的有效值為：

- 0，沒有任何特殊意義

- 1，這表示在修改任何檔案系統結構、目錄或檔案之前，必須先將此欄位清除為0

#### <a name="3114-bytespersectorshift-field"></a>3.1.14 BytesPerSectorShift 欄位

BytesPerSectorShift 欄位應描述每個磁區的位元組（以記錄<sub>2</sub> 表示） (N) ，其中 N 是每個磁區的位元組數目。 例如，針對每個磁區512個位元組，此欄位的值為9。

此欄位的有效值範圍應為：

- 至少有9個 (磁區大小為512個位元組) ，這是 exFAT 磁片區的最小磁區

- 最多12個 (磁區大小為4096個位元組) ，也就是個人電腦中常見 Cpu 的記憶體頁面大小

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 SectorsPerClusterShift 欄位

SectorsPerClusterShift 欄位應描述每個叢集的磁區（以記錄<sub>2</sub> (N) 表示），其中 n 是每個叢集的磁區數目。 例如，針對每個叢集8個磁區，此欄位的值為3。

此欄位的有效值範圍應為：

- 每個叢集至少有 0 (1 個磁區) ，也就是最小的叢集

- 最多25個 BytesPerSectorShift，其評估為 32 MB 的叢集大小

#### <a name="3116-numberoffats-field"></a>3.1.16 NumberOfFats 欄位

NumberOfFats 欄位應描述磁片區包含的 FATs 和配置點陣圖數目。

此欄位的有效值範圍應為：

- 1，表示磁片區只包含第一個 FAT 和第一個配置點陣圖

- 2，表示磁片區包含第一個 FAT、第二個 FAT、第一個配置點陣圖和第二個配置點陣圖;此值只對 TexFAT 磁片區有效

#### <a name="3117-driveselect-field"></a>3.1.17 DriveSelect 欄位

DriveSelect 欄位必須包含擴充的 INT 13h 磁片磁碟機編號，以協助在個人電腦上使用擴充的 INT 13h，從這個磁片區進行開機搭接接。

此欄位的所有可能值都是有效的。 舊版 FAT 檔案系統中類似的欄位經常包含值80h。

#### <a name="3118-percentinuse-field"></a>3.1.18 PercentInUse 欄位

PercentInUse 欄位應描述叢集堆積中配置的群集百分比。

此欄位的有效值範圍應為：

- 介於0與100（含）之間，這是叢集堆積中已配置叢集的百分比，舍入到最接近的整數

- 完全 FFh，表示叢集堆積中配置的叢集百分比無法使用

「執行」應變更此欄位的值，以反映在叢集堆積中配置叢集的變更，或應該將它變更為 FFh。

在計算其各自的主要開機或備份開機區域總和檢查碼時，不應包含此欄位。 參考備份開機磁區時，執行應該會將此欄位視為過時。

#### <a name="3119-bootcode-field"></a>3.1.19 啟動代碼欄位

啟動控制欄位必須包含開機搭接接指令。
執行程式可能會在此欄位中填入開機-搭接接電腦系統所需的 CPU 指示。 未提供開機搭接接指令的執行程式應初始化此欄位中的每個位元組，以 F4h (個人電腦中常見 Cpu 的停止指令，) 作為其格式作業的一部分。

#### <a name="3120-bootsignature-field"></a>3.1.20 BootSignature 欄位

BootSignature 欄位應描述指定的磁區意圖是否為開機磁區。

此欄位的有效值為 AA55h。 此欄位中的任何其他值都會使其各自的開機磁區失效。 根據其各自的開機磁區中的任何其他欄位，執行前應先驗證此欄位的內容。

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3.2 主要和備份延伸開機磁區子領域

主要延伸開機磁區的每個磁區都有相同的結構;不過，每個磁區都可能保存不同的開機搭接接指令 (請參閱表 6) 。 搭接接代理程式（例如主要開機磁區的開機搭接接指令、替代的 BIOS 程式或內嵌系統的固件）可能會載入這些磁區，並執行它們所包含的指示。

備份擴充的開機磁區是主要延伸開機磁區的備份，而且具有相同的結構 (請參閱 [表 6](#table-6-extended-boot-sector-structure)) 。

在執行主要或備份擴充開機磁區的指示之前，執行程式應確定每個磁區的 ExtendedBootSignature 欄位都包含其指定的值，以驗證其內容。

雖然初始格式作業將會初始化主要和備份延伸開機磁區的內容，但執行可能會將這些磁區 (更新，並且也應該視需要更新其各自的開機總和檢查碼) 。

<div id="table-6-extended-boot-sector-structure" />

**表6擴充開機磁區結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> –4</td>
<td><p>此為必要欄位， <a href="#321-extendedbootcode-field">第3.2.1 節</a> 定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 BytesPerSectorShift 欄位。</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> –4</td>
<td>4</td>
<td><p>此為必要欄位，而且 <a href="#322-extendedbootsignature-field">區段 3.2.2</a> 會定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 BytesPerSectorShift 欄位。</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 ExtendedBootCode 欄位

ExtendedBootCode 欄位應包含開機搭接接指令。
執行程式可能會在此欄位中填入開機-搭接接電腦系統所需的 CPU 指示。 未提供開機搭接接指示的執行，應該將此欄位中的每個位元組初始化為其格式作業的一部分。

#### <a name="322-extendedbootsignature-field"></a>3.2.2 ExtendedBootSignature 欄位

ExtendedBootSignature 欄位應描述指定的磁區意圖是否為擴充的開機磁區。

此欄位的有效值為 AA550000h。 此欄位中的任何其他值都會使其各自的主要或備份擴充開機磁區失效。
根據個別的擴充開機磁區中的任何其他欄位，執行前應該先驗證此欄位的內容。

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3.3 主要和備份 OEM 參數子領域

主要 OEM 參數子領域包含十個參數結構，其中可能包含製造商專屬的資訊 (請參閱 [ [表 7](#table-7-oem-parameters-structure) ]) 。 這十個參數結構中的每一個都是衍生自泛型參數範本 (請參閱 [3.3.2) 一節](#332-generic-parameters-template) 。 製造商可以從一般參數範本衍生自己的自訂參數結構。 此規格本身會定義兩個參數結構： Null 參數 (請參閱 3.3.3) 和 Flash 參數 [一節](#333-null-parameters) (請參閱 [3.3.4) 一節](#334-flash-parameters) 。

備份 OEM 參數是主要 OEM 參數的備份，且具有相同的結構 (請參閱 [ [表 7](#table-7-oem-parameters-structure) ]) 。

在使用主要或備份 OEM 參數的內容之前，必須先驗證其各自的開機總和檢查碼，以驗證其內容。

製造商應該使用自己的自訂參數結構（如果有的話）和任何其他參數結構來填入主要和備份 OEM 參數。 後續的格式作業應該會保留主要和備份 OEM 參數的內容。

視需要更新主要和備份 OEM 參數 (，也應更新其各自的開機總和檢查碼) 。

<div id="table-7-oem-parameters-structure" />

**表 7 OEM 參數結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>參數 [0]</td>
<td>0</td>
<td>48</td>
<td>此為必要欄位，而且 <a href="#331-parameters0--parameters9">區段 3.3.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>參數 [9]</td>
<td>432</td>
<td>48</td>
<td>此為必要欄位，而且 <a href="#331-parameters0--parameters9">區段 3.3.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>保留</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> –480</td>
<td><p>此為必要欄位，而且其內容為保留。</p>
<p>注意：主要和備份開機磁區都包含 BytesPerSectorShift 欄位。</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 參數 \[ 0 \] .。。參數 \[ 9\]

這個陣列中的每個參數欄位都包含一個參數結構，此結構衍生自泛型參數範本 (請參閱 [3.3.2) 一節](#332-generic-parameters-template) 。
任何未使用的參數欄位都必須描述為包含 Null 參數結構 (請參閱 [3.3.3) 一節](#333-null-parameters) 。

#### <a name="332-generic-parameters-template"></a>3.3.2 一般參數範本

泛型參數範本會提供參數結構的基底定義 (請參閱 [表 8](#table-8-generic-parameters-template)) 。 所有的參數結構都會衍生自這個範本。 此泛型參數範本的支援是必要的。

<div id="table-8-generic-parameters-template" />

**表8一般參數範本**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#3321-parametersguid-field">區段 3.3.2.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>此為必要欄位，而且衍生自這個範本的結構會定義其內容。</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 ParametersGuid 欄位

ParametersGuid 欄位必須描述 GUID，以決定指定參數結構的其餘部分的配置。

此欄位的所有可能值都是有效的;不過，製造商應該使用 GUID 產生工具（例如 GuidGen.exe），從這個範本衍生自訂參數結構時選取 GUID。

#### <a name="333-null-parameters"></a>3.3.3 Null 參數

Null 參數結構衍生自泛型參數範本 (請參閱 [3.3.2 一節](#332-generic-parameters-template)) ，而且應該描述未使用的參數欄位 (請參閱 [ [表 9](#table-9-null-parameters-structure) ]) 。 建立或更新 OEM 參數結構時，實值會以 Null 參數結構填入未使用的參數欄位。 此外，在建立或更新 OEM 參數結構時，實值應該在陣列的結尾合併 Null 參數結構，藉此將所有其他參數結構保留在 OEM 參數結構的開頭。

Null 參數結構的支援是必要的。

<div id="table-9-null-parameters-structure" />

**表 9 Null 參數結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#3331-parametersguid-field">區段 3.3.3.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>保留</td>
<td>16</td>
<td>32</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 ParametersGuid 欄位

ParametersGuid 欄位必須符合泛型參數範本所提供的定義 (請參閱 3.3.2.1) [一節](#3321-parametersguid-field) 。

此欄位的有效值（以 GUID 標記法表示）為 {00000000-0000-0000-0000-000000000000} 。

#### <a name="334-flash-parameters"></a>3.3.4 Flash 參數

Flash 參數結構衍生自「一般參數」範本 (請參閱 [3.3.2) 一節](#332-generic-parameters-template) ，其中包含 Flash 媒體的參數 (請參閱 [ [表 10](#table-10-flash-parameters-structure) ]) 。 Flash 型存放裝置的製造商可能會填入參數欄位， (最好是參數 \[ 0 \] 欄位) 使用此參數結構。 執行程式可能會使用 Flash 參數結構中的資訊，將讀取/寫入期間的存取作業優化，以及調整媒體 durning 格式的檔案系統結構。

Flash 參數結構的支援是選擇性的。

<div id="table-10-flash-parameters-structure" />

**表 10 Flash 參數結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#3341-parametersguid-field">區段 3.3.4.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3342-eraseblocksize-field">區段 3.3.4.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3343-pagesize-field">區段 3.3.4.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3344-sparesectors-field">區段 3.3.4.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3345-randomaccesstime-field">區段 3.3.4.5</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3346-programmingtime-field">區段 3.3.4.6</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3347-readcycle-field">區段 3.3.4.7</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#3348-writecycle-field">區段 3.3.4.8</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>保留</td>
<td>44</td>
<td>4</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

所有 Flash 參數欄位的所有可能值（ParametersGuid 欄位除外）都是有效的。 不過，值0表示欄位實際上是無意義的 (實作為應忽略指定的欄位) 。

##### <a name="3341-parametersguid-field"></a>3.3.4.1 ParametersGuid 欄位

ParametersGuid 欄位必須符合泛型參數範本中提供的定義 (請參閱 3.3.2.1) [一節](#3321-parametersguid-field) 。

此欄位的有效值（以 GUID 標記法表示）為 {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}。

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 EraseBlockSize 欄位

EraseBlockSize 欄位應描述 flash 媒體清除區塊的大小（以位元組為單位）。

##### <a name="3343-pagesize-field"></a>3.3.4.3 PageSize 欄位

PageSize 欄位應描述 flash 媒體頁面的大小（以位元組為單位）。

##### <a name="3344-sparesectors-field"></a>3.3.4.4 SpareSectors 欄位

SpareSectors 欄位應描述 flash 媒體可供其內部備用作業使用的磁區數目。

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 RandomAccessTime 欄位

RandomAccessTime 欄位應描述 flash 媒體的平均隨機存取時間（以納秒為單位）。

##### <a name="3346-programmingtime-field"></a>3.3.4.6 ProgrammingTime 欄位

ProgrammingTime 欄位應描述 flash 媒體的平均程式設計時間（以毫微秒為單位）。

##### <a name="3347-readcycle-field"></a>3.3.4.7 ReadCycle 欄位

ReadCycle 欄位應描述 flash 媒體的平均讀取週期時間（以毫微秒為單位）。

##### <a name="3348-writecycle-field"></a>3.3.4.8 WriteCycle 欄位

WriteCycle 欄位應該描述平均寫入週期時間（以納秒為單位）。

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3.4 主要和備份開機總和檢查碼子領域

主要和備份開機總和檢查碼各自包含各自的開機區域中，所有其他子領域之內容的四位元組總和檢查碼的重複模式。 總和檢查碼計算不應該在其各自的開機磁區中包含 VolumeFlags 和 PercentInUse 欄位 (請參閱 [ [圖 1](#figure-1-boot-checksum-computation) ]) 。 四位元組總和檢查碼的重複模式會將其各自的開機總和檢查碼子領域從子領域的開頭填滿。

在主要或備份啟動區域中使用任何其他子領域的內容之前，必須先驗證其各自的開機總和檢查碼，以驗證它們的內容。

初始格式作業會將主要和備份開機總和檢查碼填入重複的總和檢查碼模式，而在其個別開機區域中的其他磁區內容變更時，則必須更新這些磁區。

<div id="figure-1-boot-checksum-computation" />

**圖1開機總和檢查碼計算**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4個檔案配置資料表區域

檔案配置表 (FAT) 區域最多可包含兩個 FATs，一個位於第一個 FAT 子領域，另一個位於第二個 FAT 子領域。
NumberOfFats 欄位描述此區域包含的 FATs 數目。 NumberOfFats 欄位的有效值為1和2。 因此，第一個 FAT 子領域一律會包含 FAT。 如果 NumberOfFats 欄位是2，則第二個 FAT 子領域也會包含 FAT。

[VolumeFlags] 欄位的 [ActiveFat] 欄位描述作用中的是哪個 FAT。 只有主要開機磁區中的 VolumeFlags 欄位是最新的。
必須將不是作用中的 FAT 視為過時。 使用非使用中的 FAT 和在 FATs 之間切換是特定的執行。

### <a name="41-first-and-second-fat-sub-regions"></a>4.1 第一個和第二個 FAT 子領域

FAT 應描述叢集堆積中的叢集鏈 (請參閱 [表 11](#table-11-file-allocation-table-structure)) 。
叢集鏈是一系列的群集，可提供空間來記錄檔案、目錄和其他檔案系統結構的內容。 FAT 將叢集鏈表示為叢集索引的單一連結清單。 除了前兩個專案之外，每個 FAT 中的每個專案都只代表一個群集。

<div id="table-11-file-allocation-table-structure" />

**表11檔案配置資料表結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry [0]</td>
<td>0</td>
<td>4</td>
<td>此為必要欄位，第 <a href="#412-fatentry1-field">4.1.2 節</a> 定義其內容。</td>
</tr>
<tr class="even">
<td>FatEntry [1]</td>
<td>4</td>
<td>4</td>
<td>此為必要欄位，第 <a href="#412-fatentry1-field">4.1.2 節</a> 定義其內容。</td>
</tr>
<tr class="odd">
<td>FatEntry [2]</td>
<td>8</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#413-fatentry2--fatentryclustercount1-fields">區段 4.1.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry [ClusterCount + 1]</td>
<td> (ClusterCount + 1) * 4</td>
<td>4</td>
<td><p>此為必要欄位，而且 <a href="#413-fatentry2--fatentryclustercount1-fields">區段 4.1.3</a> 會定義其內容。</p>
<p>ClusterCount + 1 永遠不能超過 FFFFFFF6h。</p>
<p>注意：主要和備份開機磁區都包含 ClusterCount 欄位。</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td> (ClusterCount + 2) * 4</td>
<td> (FatLength * 2<sup>BytesPerSectorShift</sup>) – ( (ClusterCount + 2) * 4) </td>
<td><p>此為必要欄位，而且其內容（如果有的話）未定義。</p>
<p>注意：主要和備份開機磁區都包含 ClusterCount、FatLength 和 BytesPerSectorShift 欄位。</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 FatEntry \[ 0 \] 欄位

FatEntry \[ 0 \] 欄位應描述第一個位元組中的媒體類型 (最低順序位元組) ，而且在其餘三個位元組中應包含 FFh。

應 F8h 第一個位元組)  (的媒體類型。

#### <a name="412-fatentry1-field"></a>4.1.2 FatEntry \[ 1 \] 欄位

FatEntry \[ 1 \] 欄位只會因為歷程記錄優先順序而存在，而且不會描述感興趣的任何事物。

此欄位的有效值為 FFFFFFFFh。 實值應該將此欄位初始化為其指定的值，而且不應該將此欄位用於任何用途。 「執行」不應解讀此欄位，而且應該在修改周圍欄位的作業之間保留其內容。

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] .。。FatEntry \[ ClusterCount + 1 個 \] 欄位

此陣列中的每個 FatEntry 欄位都應代表叢集堆積中的叢集。 FatEntry \[ 2 \] 代表叢集堆積中的第一個叢集，而 FatEntry \[ ClusterCount + 1 代表叢集中的 \] 最後一個叢集。

這些欄位之值的有效範圍應為：

- 介於2和 ClusterCount + 1 之間（含），指向指定叢集鏈中的下一個 FatEntry;指定的 FatEntry 不應指向位於指定叢集鏈中的任何 FatEntry

- 完全 FFFFFFF7h，將指定 FatEntry 的對應叢集標示為「不良」

- 完全 FFFFFFFFh，它會將指定的 FatEntry 對應叢集標示為叢集鏈的最後一個叢集;這是任何指定叢集鏈最後一個 FatEntry 的唯一有效值

## <a name="5-data-region"></a>5個數據區域

資料區域包含叢集堆積，可為檔案系統結構、目錄和檔案提供受控空間。

### <a name="51-cluster-heap-sub-region"></a>5.1 叢集堆積子領域

叢集堆積的結構非常簡單 (請參閱 [表 12](#table-12-cluster-heap-structure)) ;每一系列連續的磁區都會描述一個叢集，如同 SectorsPerClusterShift 欄位所定義。 重要的是，叢集堆積的第一個叢集有索引二，這會直接對應至 FatEntry 2 的索引 \[ \] 。

在 exFAT 磁片區中，配置點陣圖 (請參閱 [7.1.5 區段](#715-allocation-bitmap) ，) 維護所有叢集之配置狀態的記錄。 這與 exFAT 的前身 (FAT12、FAT16 和 FAT32) 有很大的差異，其中 FAT 會維護叢集堆積中所有叢集的配置狀態記錄。

<div id="table-12-cluster-heap-structure" />

**表12叢集堆積結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (磁區) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (磁區) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>叢集 [2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>此為必要欄位， <a href="#511-cluster2--clusterclustercount1-fields">第5.1.1 節</a> 定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 ClusterHeapOffset 和 SectorsPerClusterShift 欄位。</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster [ClusterCount + 1]</td>
<td>ClusterHeapOffset + (ClusterCount – 1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>此為必要欄位， <a href="#511-cluster2--clusterclustercount1-fields">第5.1.1 節</a> 定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 ClusterCount、ClusterHeapOffset 和 SectorsPerClusterShift 欄位。</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ 2 \] .。。Cluster \[ ClusterCount + 1 個 \] 欄位

此陣列中的每個叢集欄位都是一連串連續的磁區，其大小是由 SectorsPerClusterShift 欄位所定義。

## <a name="6-directory-structure"></a>6個目錄結構

ExFAT 檔案系統使用目錄樹狀結構方法來管理存在於叢集堆積中的檔案系統結構和檔案。 目錄樹狀結構中的父系和子系之間的目錄具有一對多關聯性。

FirstClusterOfRootDirectory 欄位所參考的目錄是目錄樹狀結構的根。 所有其他目錄都會以單向連結的方式從根目錄中下降。

每個目錄都是由一系列的目錄專案所組成 (請參閱 [ [表 13](#table-13-directory-structure) ]) 。

一或多個目錄專案會合並到目錄專案集，以描述感興趣的內容，例如檔案系統結構、子目錄或檔案。

<div id="table-13-directory-structure" />

**表13目錄結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry [0]</td>
<td>0</td>
<td>32</td>
<td>此為必要欄位，第 <a href="#61-directoryentry0--directoryentryn--1">6.1 節</a> 定義其內容。</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry [N-1]</td>
<td> (N-1) * 32</td>
<td>32</td>
<td><p>此為必要欄位，第 <a href="#61-directoryentry0--directoryentryn--1">6.1 節</a> 定義其內容。</p>
<p>N （DirectoryEntry 欄位數目）是叢集鏈的大小（以位元組為單位），其中包含指定的目錄，並除以 DirectoryEntry 欄位的大小32個位元組。</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6.1 DirectoryEntry \[ 0 \] .。。DirectoryEntry \[ N--1\]

這個陣列中的每個 DirectoryEntry 欄位都是衍生自一般 DirectoryEntry 範本 (請參閱 [6.2) 一節](#62-generic-directoryentry-template) 。

### <a name="62-generic-directoryentry-template"></a>6.2 一般 DirectoryEntry 範本

一般 DirectoryEntry 範本會提供目錄專案的基底定義 (請參閱 [表 14](#table-14-generic-directoryentry-template)) 。 所有的目錄專案結構都是衍生自這個範本，而且只有 Microsoft 定義的目錄輸入結構有效 (exFAT 除了 [7.8 節](#78-vendor-extension-directory-entry) 和 [7.9 節](#79-vendor-allocation-directory-entry)) 中所定義以外，不會提供製造商定義之目錄輸入結構的規定。 可解讀泛型 DirectoryEntry 範本的功能是必要的。

<div id="table-14-generic-directoryentry-template" />

**表14一般 DirectoryEntry 範本**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#621-entrytype-field">區段 6.2.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>此為必要欄位，而且衍生自這個範本的結構可能會定義其內容。</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#622-firstcluster-field">區段 6.2.2</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#623-datalength-field">區段上面 6.2.3</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 >entrytype 欄位

>entrytype 欄位有三種使用模式，欄位的值會定義 (請參閱以下) 的清單。

- 00h （這是目錄結束記號，並適用下列條件）：

  - 指定 DirectoryEntry 中的所有其他欄位實際上都是保留的

  - 指定目錄中的所有後續目錄專案也都是目錄結束記號

  - 目錄結束記號只在目錄專案集外有效

  - 視需要覆寫可能會覆寫目錄結尾的標記

- 介於01h 和7Fh （可為）之間，這是未使用的目錄專案標記，而且適用下列情況：

  - 指定 DirectoryEntry 中的所有其他欄位實際上都未定義

  - 未使用的目錄專案只在目錄專案集之外有效

  - 視需要覆寫可能會覆寫未使用的目錄專案

  - 這一範圍的值會對應到 InUse 欄位 (請參閱 [區段 6.2.1.4](#6214-inuse-field)) ，其中包含值0

- 在81h 與 FFh 之間，其為一般目錄專案，而且適用下列條件：

  - >entrytype 欄位的內容 (請參閱 [表 15](#table-15-generic-entrytype-field-structure)) 判斷 DirectoryEntry 結構其餘部分的版面配置

  - 此值範圍（只有此值範圍）在目錄專案集內是有效的

  - 這一範圍的值會直接對應到 InUse 欄位 (請參閱) 包含值1的[區段 6.2.1.4](#6214-inuse-field)

若要防止修改 InUse 欄位 (請參閱) [6.2.1.4 一節](#6214-inuse-field) ，以錯誤的方式產生目錄結束記號，值80h 無效。

<div id="table-15-generic-entrytype-field-structure" />

**表15一般 >entrytype 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>此為必要欄位，而且 <a href="#6211-typecode-field">區段 6.2.1.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>此為必要欄位，而且區段 <a href="#6212-typeimportance-field">區段 6.2.1.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6213-typecategory-field">區段 6.2.1.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6214-inuse-field">區段 6.2.1.4</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 TypeCode 欄位

TypeCode 欄位會部分描述指定之目錄專案的特定類型。 此欄位加上 TypeImportance 和 TypeCategory 欄位 (分別參閱6.2.1.2 和[section 6.2.1.3](#6213-typecategory-field)[一節](#6212-typeimportance-field)，) 唯一識別指定目錄專案的型別。

除非 TypeImportance 和 TypeCategory 欄位都包含0值，否則此欄位的所有可能值都是有效的。在此情況下，值0對此欄位而言是不正確。

##### <a name="6212-typeimportance-field"></a>6.2.1.2 TypeImportance 欄位

TypeImportance 欄位必須描述指定之目錄專案的重要性。

此欄位的有效值應為：

- 0表示指定的目錄專案很重要 (請分別參閱重要主要和重要次要目錄專案的6.3.1.2.1 和[區段 6.4.1.2.1](#64121-critical-secondary-directory-entries) [一](#63121-critical-primary-directory-entries)節) 

- 1，這表示指定的目錄專案是良性的 (參閱 [6.3.1.2.2](#63122-benign-primary-directory-entries) 和 [6.4.1.2.2](#64122-benign-secondary-directory-entries) 一節，以取得無害的主要和良性次要目錄專案，分別是) 

##### <a name="6213-typecategory-field"></a>6.2.1.3 TypeCategory 欄位

TypeCategory 欄位必須描述指定之目錄專案的類別。

此欄位的有效值應為：

- 0，表示指定的目錄專案是主要 (請參閱 [6.3 節](#63-generic-primary-directoryentry-template)) 

- 1，表示指定的目錄專案是次要 (請參閱 [6.4 節](#64-generic-secondary-directoryentry-template)) 

##### <a name="6214-inuse-field"></a>6.2.1.4 InUse 欄位

InUse 欄位應描述是否正在使用指定的目錄專案。

此欄位的有效值應為：

- 0，表示指定的目錄專案未使用;這表示指定的結構實際上是未使用的目錄專案

- 1，表示指定的目錄專案正在使用中;這表示指定的結構是一般目錄專案

#### <a name="622-firstcluster-field"></a>6.2.2 FirstCluster 欄位

FirstCluster 欄位必須包含與給定目錄專案相關聯之叢集堆積中配置的第一個叢集索引。

此欄位的有效值範圍應為：

- 正好是0，表示沒有叢集配置存在

- 介於2和 ClusterCount + 1 之間，也就是有效叢集索引的範圍

如果叢集配置與衍生結構不相容，則衍生自這個範本的結構可能會重新定義 FirstCluster 和 DataLength 欄位。

#### <a name="623-datalength-field"></a>上面 6.2.3 DataLength 欄位

DataLength 欄位描述相關聯的叢集配置所包含之資料的大小（以位元組為單位）。

此欄位值的有效範圍為：

- 至少為 0;如果 FirstCluster 欄位包含值0，則這個欄位的唯一有效值為0

- 最多 ClusterCount \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

如果衍生結構無法進行叢集配置，則從這個範本衍生的結構可能會重新定義 FirstCluster 和 DataLength 欄位。

### <a name="63-generic-primary-directoryentry-template"></a>6.3 一般主要 DirectoryEntry 範本

目錄專案集的第一個目錄專案必須是主要目錄專案。 目錄專案組中所有後續的目錄專案（如果有的話）都必須是次要目錄專案 (請參閱 [6.4) 一節](#64-generic-secondary-directoryentry-template) 。

可解讀泛型主要 DirectoryEntry 範本的功能是必要的。

所有的主要目錄專案結構都衍生自一般主要 DirectoryEntry 範本 (請參閱) 衍生自一般 DirectoryEntry 範本的 [ [表 16](#table-16-generic-primary-directoryentry-template) ]， (參閱 [6.2) 一節](#62-generic-directoryentry-template) 。

<div id="table-16-generic-primary-directoryentry-template" />

**表16一般主要 DirectoryEntry 範本**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#631-entrytype-field">區段 6.3.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#632-secondarycount-field">區段 6.3.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#633-setchecksum-field">區段 6.3.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#634-generalprimaryflags-field">區段 6.3.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>此為必要欄位，而且衍生自這個範本的結構會定義其內容。</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#635-firstcluster-field">區段 6.3.5</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#636-datalength-field">區段 6.3.6</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 >entrytype 欄位

>entrytype 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1) [一節](#621-entrytype-field) 。

##### <a name="6311-typecode-field"></a>6.3.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.1) [一節](#6211-typecode-field) 。

##### <a name="6312-typeimportance-field"></a>6.3.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.2) [一節](#6212-typeimportance-field) 。

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 重要的主要目錄專案

重要的主要目錄專案包含對 exFAT 磁片區適當管理很重要的資訊。 只有根目錄包含重要的主要目錄專案 (檔案目錄專案是例外狀況，請參閱 [7.4 節](#74-file-directory-entry)) 。

重要主要目錄專案的定義與主要 exFAT 修訂編號相關聯。 執行必須支援所有重要的主要目錄專案，而且只會記錄此規格所定義的重要主要目錄專案結構。

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 良性的主要目錄專案

無害的主要目錄專案包含額外的資訊，可能有助於管理 exFAT 磁片區。 任何目錄都可能包含良性的主要目錄專案。

良性主要目錄專案的定義與次要 exFAT 修訂編號相關聯。 此規格或任何後續規格的任何良性主要目錄專案支援都是選擇性的。 無法辨識的良性主要目錄專案會將整個目錄專案集轉譯為無法辨識的 (，超出適用的目錄專案範本) 的定義。

##### <a name="6313-typecategory-field"></a>6.3.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.3) [一節](#6213-typecategory-field) 。

針對此範本，此欄位的有效值應為0。

##### <a name="6314-inuse-field"></a>6.3.1.4 InUse 欄位

InUse 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.4) [一節](#6214-inuse-field) 。

#### <a name="632-secondarycount-field"></a>6.3.2 SecondaryCount 欄位

SecondaryCount 欄位應描述緊接在指定的主要目錄專案後面的次要目錄專案數目。 這些次要目錄專案以及指定的主要目錄專案，包含目錄專案集。

此欄位的有效值範圍應為：

- 至少為0，表示此主要目錄專案是目錄專案集中唯一的專案

- 最多255，這表示下一個255目錄專案和此主要目錄專案組成目錄專案集

從這個範本衍生的重要主要目錄專案結構可能會重新定義 SecondaryCount 和 SetChecksum 欄位。

#### <a name="633-setchecksum-field"></a>6.3.3 SetChecksum 欄位

SetChecksum 欄位應包含指定目錄專案集中所有目錄專案的總和檢查碼。 不過，總和檢查碼會排除此欄位 (請參閱 [ [圖 2](#figure-2-entrysetchecksum-computation) ]) 。 在使用指定的目錄專案集內的任何其他目錄專案之前，必須先驗證此欄位的內容是否有效。

從這個範本衍生的重要主要目錄專案結構可能會重新定義 SecondaryCount 和 SetChecksum 欄位。

<div id="figure-2-entrysetchecksum-computation" />

**圖 2 EntrySetChecksum 計算**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>6.3.4 GeneralPrimaryFlags 欄位

GeneralPrimaryFlags 欄位包含旗標 (請參閱 [表 17](#table-17-generic-generalprimaryflags-field-structure)) 。

從這個範本衍生的重要主要目錄專案結構可能會重新定義此欄位。

<div id="table-17-generic-generalprimaryflags-field-structure" />

**表17一般 GeneralPrimaryFlags 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6341-allocationpossible-field">區段 6.3.4.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6342-nofatchain-field">區段 6.3.4.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>此為必要欄位，而且衍生自這個範本的結構可能會定義此欄位。</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 AllocationPossible 欄位

AllocationPossible 欄位說明是否可以針對指定的目錄專案，描述叢集堆積中的配置。

此欄位的有效值應為：

- 0表示無法建立相關聯的叢集配置，且 FirstCluster 和 DataLength 欄位實際上是未定義的 (結構（衍生自這個範本）可能會重新定義這些欄位) 

- 1，表示可以有相關聯的叢集配置，且 FirstCluster 和 DataLength 欄位已定義

##### <a name="6342-nofatchain-field"></a>6.3.4.2 NoFatChain 欄位

NoFatChain 欄位會指出作用中的 FAT 是否描述指定配置的叢集鏈。

此欄位的有效值應為：

- 0，這表示配置的叢集鏈的對應 FAT 專案是有效的，而且必須加以解讀。如果 AllocationPossible 欄位包含值0，或如果 AllocationPossible 欄位包含值1，且 FirstCluster 欄位包含值0，則這個欄位的唯一有效值為0

- 1，這表示相關聯的配置是一系列連續的群集;叢集的對應 FAT 專案無效，且不應解讀它們;執行可能會使用下列方程式來計算關聯配置的大小： DataLength/ (2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) 進位到最接近的整數

如果從這個範本衍生的重要主要目錄專案結構重新定義 GeneralPrimaryFlags 欄位，則任何相關聯配置之叢集鏈的對應 FAT 專案都是有效的。

#### <a name="635-firstcluster-field"></a>6.3.5 FirstCluster 欄位

FirstCluster 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.2) [一節](#622-firstcluster-field) 。

如果 NoFatChain 位為1，則 FirstCluster 必須指向叢集堆積中的有效群集。

從這個範本衍生的重要主要目錄專案結構可能會重新定義 FirstCluster 和 DataLength 欄位。 只有當 AllocationPossible 欄位包含值0時，其他衍生自這個範本的結構才可以重新定義 FirstCluster 和 DataLength 欄位。

#### <a name="636-datalength-field"></a>6.3.6 DataLength 欄位

DataLength 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱上面 6.2.3) [一節](#623-datalength-field) 。

如果 NoFatChain 位為1，則 DataLength 不得為零。 如果 FirstCluster 欄位為零，則 DataLength 也必須為零。

從這個範本衍生的重要主要目錄專案結構可能會重新定義 FirstCluster 和 DataLength 欄位。 只有當 AllocationPossible 欄位包含值0時，其他衍生自這個範本的結構才可以重新定義 FirstCluster 和 DataLength 欄位。

### <a name="64-generic-secondary-directoryentry-template"></a>6.4 一般次要 DirectoryEntry 範本

次要目錄專案的主要用途是提供目錄專案集的其他相關資訊。 可解讀泛型次要 DirectoryEntry 範本的功能是必要的。

重大和良性次要目錄專案的定義與次要 exFAT 修訂編號相關聯。 此規格或後續規格的任何重大或良性次要目錄專案支援都是選擇性的。

所有次要目錄專案結構都衍生自一般次要 DirectoryEntry 範本 (請參閱 [表 18](#table-18-generic-secondary-directoryentry-template)) ，其衍生自一般 DirectoryEntry 範本 (請參閱 [6.2 節](#62-generic-directoryentry-template)) 。

<div id="table-18-generic-secondary-directoryentry-template" />

**表18一般次要 DirectoryEntry 範本**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且區段 <a href="#641-entrytype-field">區段 6.4.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#642-generalsecondaryflags-field">區段 6.4.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>此為必要欄位，而且衍生自這個範本的結構會定義其內容。</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#643-firstcluster-field">區段 6.4.3</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#644-datalength-field">區段 6.4.4</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 >entrytype 欄位

>entrytype 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 [6.2.1 一節](#621-entrytype-field)) 

##### <a name="6411-typecode-field"></a>6.4.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.1) [一節](#6211-typecode-field) 。

##### <a name="6412-typeimportance-field"></a>6.4.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.2) [一節](#6212-typeimportance-field) 。

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 重要的次要目錄專案

重要的次要目錄專案包含適當管理其包含目錄專案集的重要資訊。
雖然您可以選擇是否要對任何特定的重要次要目錄專案提供支援，但無法辨識的重要目錄專案會將整個目錄專案集轉譯為無法辨識的 (，而不是適用的目錄專案範本) 的定義。

但是，如果目錄專案集至少包含一個執行無法辨識的重要次要目錄專案，則此執行最多應該會解讀目錄專案集內目錄專案的範本，而不是與目錄專案 (集內任何目錄專案相關聯的資料，而不是與目錄專案集內任何目錄專案相關聯的資料，請參閱 [7.4 節](#74-file-directory-entry)) 。

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 良性次要目錄專案

良性次要目錄專案包含額外的資訊，可能有助於管理其包含的目錄專案集。 任何特定良性次要目錄專案的支援是選擇性的。
無法辨識的良性次要目錄專案不會將整個目錄專案集轉譯為無法辨識。

執行可能會忽略它無法辨識的任何無害次要專案。

##### <a name="6413-typecategory-field"></a>6.4.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.3) [一節](#6213-typecategory-field) 。

針對此範本，此欄位的有效值為1。

##### <a name="6414-inuse-field"></a>6.4.1.4 InUse 欄位

InUse 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.1.4) [一節](#6214-inuse-field) 。

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 GeneralSecondaryFlags 欄位

GeneralSecondaryFlags 欄位包含旗標 (請參閱 [ [表 19](#table-19-generic-generalsecondaryflags-field-structure) ]) 。

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**表19一般 GeneralSecondaryFlags 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6421-allocationpossible-field">區段 6.4.2.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#6422-nofatchain-field">區段 6.4.2.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>此為必要欄位，而且衍生自這個範本的結構可能會定義此欄位。</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 AllocationPossible 欄位

AllocationPossible 欄位的定義必須與一般主要 DirectoryEntry 範本中相同的命名欄位相同 (請參閱 [6.3.4.1) 一節](#6341-allocationpossible-field) 。

##### <a name="6422-nofatchain-field"></a>6.4.2.2 NoFatChain 欄位

NoFatChain 欄位的定義必須與一般主要 DirectoryEntry 範本中相同的命名欄位相同 (請參閱 [6.3.4.2) 一節](#6342-nofatchain-field) 。

#### <a name="643-firstcluster-field"></a>6.4.3 FirstCluster 欄位

FirstCluster 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱 6.2.2) [一節](#622-firstcluster-field) 。

如果 NoFatChain 位為1，則 FirstCluster 必須指向叢集堆積中的有效群集。

#### <a name="644-datalength-field"></a>6.4.4 DataLength 欄位

DataLength 欄位必須符合一般 DirectoryEntry 範本中提供的定義 (請參閱上面 6.2.3) [一節](#623-datalength-field) 。

如果 NoFatChain 位為1，則 DataLength 不得為零。 如果 FirstCluster 欄位為零，則 DataLength 也必須為零。

## <a name="7-directory-entry-definitions"></a>7個目錄專案定義

ExFAT 檔案系統的修訂1.00 定義了下列目錄專案：

- 重大主要

  - 配置點陣圖 ([區段 7.1](#71-allocation-bitmap-directory-entry)) 

  - 上案例資料表 ([區段 7.2](#72-up-case-table-directory-entry)) 

  - 磁片區標籤 ([區段 7.3](#73-volume-label-directory-entry)) 

  - 檔 ([區段 7.4](#74-file-directory-entry)) 

- 無害的主要

  - 磁片區 GUID ([區段 7.5](#75-volume-guid-directory-entry)) 

  - TexFAT 填補 ([區段 7.10](#710-texfat-padding-directory-entry)) 

<!-- -->

- 重要次要

  - 資料流程延伸模組 ([區段 7.6](#76-stream-extension-directory-entry)) 

  - 檔案名 ([區段 7.7](#77-file-name-directory-entry)) 

- 良性次要

  - 廠商延伸模組 ([第7.8 節](#78-vendor-extension-directory-entry)) 

  - 廠商配置 ([區段 7.9](#79-vendor-allocation-directory-entry)) 

### <a name="71-allocation-bitmap-directory-entry"></a>7.1 配置點陣圖目錄專案

在 exFAT 檔案系統中，FAT 不會描述叢集的配置狀態;配置點陣圖則是如此。 配置點陣圖存在於叢集堆積中 (請參閱 [7.1.5) 一節](#715-allocation-bitmap) ，在根目錄中有對應的重要主要目錄專案 (請參閱 [表 20](#table-20-allocation-bitmap-directoryentry-structure)) 。

NumberOfFats 欄位會決定根目錄中有效配置點陣圖目錄專案的數目。 如果 NumberOfFats 欄位包含值1，則唯一有效的配置點陣圖目錄專案數目為1。 此外，只有在描述第一個配置點陣圖 (參閱 7.1.2.1) 一 [節](#7121-bitmapidentifier-field) 時，才會有一個配置點陣圖目錄專案是有效的。 如果 NumberOfFats 欄位包含值2，則唯一有效的配置點陣圖目錄專案數目是2。
此外，兩個配置點陣圖目錄專案只有在描述第一個配置點陣圖時才有效，另一個則描述第二個配置點陣圖。

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**表20配置點陣圖 DirectoryEntry 結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#711-entrytype-field">區段 7.1.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#712-bitmapflags-field">區段 7.1.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>保留</td>
<td>2</td>
<td>18</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#713-firstcluster-field">區段 7.1.3</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#714-datalength-field">區段 7.1.4</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 >entrytype 欄位

>entrytype 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1) [一節](#631-entrytype-field) 。

##### <a name="7111-typecode-field"></a>7.1.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.1) [一節](#6311-typecode-field) 。

對於配置點陣圖目錄專案，此欄位的有效值為1。

##### <a name="7112-typeimportance-field"></a>7.1.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.2) [一節](#6312-typeimportance-field) 。

對於配置點陣圖目錄專案，此欄位的有效值為0。

##### <a name="7113-typecategory-field"></a>7.1.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.3) [一節](#6313-typecategory-field) 。

##### <a name="7114-inuse-field"></a>7.1.1.4 InUse 欄位

InUse 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.4) [一節](#6314-inuse-field) 。

#### <a name="712-bitmapflags-field"></a>7.1.2 BitmapFlags 欄位

BitmapFlags 欄位包含旗標 (請參閱 [表 21](#table-21-bitmapflags-field-structure)) 。

<div id="table-21-bitmapflags-field-structure" />

**表 21 BitmapFlags 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#7121-bitmapidentifier-field">區段 7.1.2.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>保留</td>
<td>1</td>
<td>7</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 BitmapIdentifier 欄位

BitmapIdentifier 欄位應該會指出給定目錄專案所描述的配置點陣圖。 「執行」應該使用第一個配置點陣圖搭配第一個 FAT，而且應該使用第二個配置點陣圖搭配第二個 FAT。 ActiveFat 欄位說明哪些 FAT 和配置點陣圖為作用中。

此欄位的有效值應為：

- 0，表示指定的目錄專案會描述第一個配置點陣圖

- 1，表示指定的目錄專案會描述第二個配置點陣圖，而且只有在 NumberOfFats 包含值2時，才可能發生

#### <a name="713-firstcluster-field"></a>7.1.3 FirstCluster 欄位

FirstCluster 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.5) [一節](#635-firstcluster-field) 。

此欄位包含叢集鏈第一個叢集的索引，如同 FAT 所述，它會裝載配置點陣圖。

#### <a name="714-datalength-field"></a>7.1.4 DataLength 欄位

DataCluster 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.6) [一節](#636-datalength-field) 。

#### <a name="715-allocation-bitmap"></a>7.1.5 配置點陣圖

配置點陣圖會記錄叢集堆積中叢集的配置狀態。 配置點陣圖中的每個位都會指出其對應的叢集是否可供配置。

配置點陣圖代表從最低到最高索引的叢集 (請參閱 [表 22](#table-22-allocation-bitmap-structure)) 。 基於歷史原因，第一個叢集的索引為2。
注意：點陣圖中的第一個位是第一個位元組的最低順序位。

<div id="table-22-allocation-bitmap-structure" />

**表22配置點陣圖結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry [2]</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且區段 <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">區段 7.1.5.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry [ClusterCount + 1]</td>
<td>ClusterCount-1</td>
<td>1</td>
<td><p>此為必要欄位，而且 <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">區段 7.1.5.1</a> 會定義其內容。</p>
<p>注意：主要和備份開機磁區都包含 ClusterCount 欄位。</p></td>
</tr>
<tr class="even">
<td>保留</td>
<td>ClusterCount</td>
<td> (DataLength * 8) – ClusterCount</td>
<td><p>此為必要欄位，而且會保留其內容（如果有的話）。</p>
<p>注意：主要和備份開機磁區都包含 ClusterCount 欄位。</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] .。。BitmapEntry \[ ClusterCount + 1 個 \] 欄位

此陣列中的每個 BitmapEntry 欄位都代表叢集堆積中的叢集。 BitmapEntry \[ 2 \] 代表叢集堆積中的第一個叢集，而 BitmapEntry \[ ClusterCount + 1 代表叢集中的 \] 最後一個叢集。

這些欄位的有效值應為：

- 0，描述可供配置的對應叢集

- 1，將對應的叢集描述為無法配置 (叢集配置可能已經取用對應的叢集，或使用中的 FAT 可能會將對應的叢集描述為錯誤) 

### <a name="72-up-case-table-directory-entry"></a>7.2 向上案例資料表目錄專案

Up 案例資料表定義從小寫轉換為大寫字元的轉換。 這點很重要，因為檔案名目錄專案 (請參閱7.7 章節) 使用 Unicode 字元和 exFAT 檔案系統不區分大小寫，並保留大小寫。 此案例資料表存在於叢集堆積 (請參閱 7.2.5) [一節](#725-up-case-table) 中，並在根目錄中有對應的重要主要目錄專案 (請參閱 [表格 23](#table-23-up-case-table-directoryentry-structure)) 。 有效的 Up 案例資料表目錄專案數目為1。

由於 Up 案例資料表和檔案名之間的關聯性，因此，除了格式作業的結果之外，實作為結果不應修改向上案例資料表。

<div id="table-23-up-case-table-directoryentry-structure" />

**資料表23向上-案例資料表 DirectoryEntry 結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#721-entrytype-field">區段 7.2.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#722-tablechecksum-field">區段 7.2.2</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#723-firstcluster-field">區段 7.2.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#724-datalength-field">區段 7.2.4</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 >entrytype 欄位

>entrytype 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1) [一節](#631-entrytype-field) 。

##### <a name="7211-typecode-field"></a>7.2.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.1) [一節](#6311-typecode-field) 。

若為上案例資料表目錄專案，此欄位的有效值為
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.2) [一節](#6312-typeimportance-field) 。

若為上案例資料表目錄專案，此欄位的有效值為
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.3) [一節](#6313-typecategory-field) 。

##### <a name="7214-inuse-field"></a>7.2.1.4 InUse 欄位

InUse 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.4) [一節](#6314-inuse-field) 。

#### <a name="722-tablechecksum-field"></a>7.2.2 TableChecksum 欄位

[TableChecksum] 欄位包含 [FirstCluster] 和 [DataLength] 欄位描述) 的向上案例資料表 (總和檢查碼。 在使用向上案例資料表之前，必須先驗證此欄位的內容是否有效。

<div id="figure-3-tablechecksum-computation" />

**圖 3 TableChecksum 計算**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 FirstCluster 欄位

FirstCluster 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.5) [一節](#635-firstcluster-field) 。

此欄位包含叢集鏈第一個叢集的索引，如同 FAT 所述，它會裝載高案例資料表。

#### <a name="724-datalength-field"></a>7.2.4 DataLength 欄位

DataCluster 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.6) [一節](#636-datalength-field) 。

#### <a name="725-up-case-table"></a>7.2.5 Up-案例資料表

高案例資料表是一系列的 Unicode 字元對應。 字元對應是由2個位元組的欄位所組成，其中的 up 案例資料表中的欄位索引代表要加上大寫的 Unicode 字元，而2個位元組的欄位則代表大寫的 Unicode 字元。

前128個 Unicode 字元具有強制對應 (請參閱 [表格 24](#table-24-mandatory-first-128-up-case-table-entries)) 。
針對前128個 Unicode 字元，具有任何其他字元對應的 up 案例資料表無效。

僅支援強制對應範圍中之字元的實作為，可能會忽略下一個案例資料表其餘部分的對應。 在透過檔案名目錄專案建立或重新命名 (檔案時，這類的執行應該只會使用強制對應範圍中的字元，請參閱 [7.7) 一節](#77-file-name-directory-entry) 。 當您的現有檔案名出現上限時，這類的執行不應該是從非強制對應範圍中的大寫字元，但應該在產生的大寫檔案名中保持不變， (這是部分的大小寫) 。 比較檔案名時，這類的執行應該會將與名稱不同的檔案名從非強制對應範圍中的 Unicode 字元視為相等。 雖然這類檔案名只是可能對等的，但這類的執行無法確保完整大小寫的檔案名不會與下一個比較的名稱相衝突。

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Table 24 強制的第一個 128 up-案例資料表專案**

| 資料表索引 | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(附注：具有非身分識別的案例對應的專案會以粗體顯示)**

格式化磁片區時，可能會使用身分識別對應壓縮來產生壓縮格式的高案例資料表，因為 Unicode 字元空間的其中一大部分並沒有案例的概念 (這表示「小寫」和「大寫」字元等同于) 。
實值會藉由代表一系列的識別對應，並以 FFFFh 後面加上識別對應的數目，來壓縮高案例資料表。

例如，可能會使用下列八個壓縮的案例資料表專案，來表示 64h) 字元對應的前一個 100 (：

> FFFFh, 0061h, 0041h, 0042h, 0043h

前兩個專案表示前 97 (61h) 字元 (從0000h 到 0060h) 具有身分識別對應。 後續的字元（0061h 至0063h）會分別對應至0041h 至0043h 的字元。

將磁片區格式化時提供壓縮的案例資料表的功能是選擇性的。 不過，您可以同時解讀未壓縮和壓縮的案例資料表。 [TableChecksum] 欄位的值一律符合在磁片區上存在的案例資料表，可能是壓縮或未壓縮的格式。

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 建議的 Up 案例資料表

格式化磁片區時，執行應以壓縮格式記錄建議的案例資料表 (請參閱 [ [表 25](#table-25-recommended-up-case-table-in-compressed-format) ]) ，其中 TableChecksum 欄位的值為 E619D30Dh。

如果實作為定義自己的案例資料表（壓縮或未壓縮），則該資料表應涵蓋完整的 Unicode 字元範圍 (從字元碼0000h 到 FFFFh 內含) 。

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**資料表25建議的高壓縮格式案例資料表**

| 原始位移 | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02BBh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFh   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10BBh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7.3 磁片區標籤目錄專案

磁片區標籤是 Unicode 字串，可讓使用者區別其存放磁片區。 在 exFAT 檔案系統中，磁片區標籤會以根目錄中的主要目錄專案形式存在， (請參閱 [表格 26](#table-26-volume-label-directoryentry-structure)) 。 有效的磁片區標籤目錄專案數目範圍從0到1。

<div id="table-26-volume-label-directoryentry-structure" />

**資料表26磁片區標籤 DirectoryEntry 結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#731-entrytype-field">區段 7.3.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#732-charactercount-field">區段 7.3.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>此為必要欄位，而且 <a href="#733-volumelabel-field">區段 7.3.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>保留</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 >entrytype 欄位

>entrytype 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1) [一節](#631-entrytype-field) 。

##### <a name="7311-typecode-field"></a>7.3.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.1) [一節](#6311-typecode-field) 。

針對磁片區標籤目錄專案，此欄位的有效值為
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.2) [一節](#6312-typeimportance-field) 。

針對磁片區標籤目錄專案，此欄位的有效值為
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.3) [一節](#6313-typecategory-field) 。

##### <a name="7314-inuse-field"></a>7.3.1.4 InUse 欄位

InUse 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.4) [一節](#6314-inuse-field) 。

#### <a name="732-charactercount-field"></a>7.3.2 CharacterCount 欄位

CharacterCount 欄位必須包含 VolumeLabel 欄位包含的 Unicode 字串長度。

此欄位的有效值範圍應為：

- 至少為0，這表示 Unicode 字串的長度為0個字元， (相當於無磁片區標籤) 

- 最多11個，這表示 Unicode 字串長度為11個字元

#### <a name="733-volumelabel-field"></a>7.3.3 VolumeLabel 欄位

VolumeLabel 欄位必須包含 Unicode 字串，也就是磁片區的使用者易記名稱。 VolumeLabel 欄位與檔案名目錄專案的 FileName 欄位有相同的無效字元組 (請參閱 [7.7.3) 一節](#773-filename-field) 。

### <a name="74-file-directory-entry"></a>7.4 檔案目錄專案

檔案目錄專案會描述檔案和目錄。 它們是重要的主要目錄專案，任何目錄可能包含零或多個檔案目錄專案 (請參閱 [表格 27](#table-27-file-directoryentry)) 。 若要讓檔案目錄專案有效，只有一個資料流程延伸目錄專案，而且至少一個檔案名目錄專案必須緊接在檔案目錄專案後面 (請分別參閱 [第7.6 節](#76-stream-extension-directory-entry) 和 [第7.7 節](#77-file-name-directory-entry)) 。

<div id="table-27-file-directoryentry" />

**表27檔案 DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#741-entrytype-field">區段7.4.1 版</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#742-secondarycount-field">區段 7.4.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#743-setchecksum-field">區段 7.4.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#744-fileattributes-field">區段 7.4.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> 區段7.4.5 會 </
a> 定義其內容。</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">區段 7.4.6</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">區段 7.4.7</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> 區段7.4.5 會 </
a> 定義其內容。</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">區段 7.4.6</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> 區段7.4.5 會 </
a> 定義其內容。</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">區段 7.4.6</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">區段 7.4.7</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 版 >entrytype 欄位

>entrytype 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1) [一節](#631-entrytype-field) 。

##### <a name="7411-typecode-field"></a>7.4.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.1) [一節](#6311-typecode-field) 。

若為檔案目錄專案，此欄位的有效值為5。

##### <a name="7412-typeimportance-field"></a>7.4.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.2) [一節](#6312-typeimportance-field) 。

若為檔案目錄專案，此欄位的有效值為0。

##### <a name="7413-typecategory-field"></a>7.4.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.3) [一節](#6313-typecategory-field) 。

##### <a name="7414-inuse-field"></a>7.4.1.4 InUse 欄位

InUse 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.4) [一節](#6314-inuse-field) 。

#### <a name="742-secondarycount-field"></a>7.4.2 SecondaryCount 欄位

SecondaryCount 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.2) [一節](#632-secondarycount-field) 。

#### <a name="743-setchecksum-field"></a>7.4.3 SetChecksum 欄位

SetChecksum 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.3) [一節](#633-setchecksum-field) 。

#### <a name="744-fileattributes-field"></a>7.4.4 FileAttributes 欄位

FileAttributes 欄位包含旗標 (請參閱 [表格 28](#table-28-fileattributes-field-structure)) 。

<div id="table-28-fileattributes-field-structure" />

**表 28 FileAttributes 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，並符合 MS-DOS 定義。</td>
</tr>
<tr class="even">
<td>Hidden</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，並符合 MS-DOS 定義。</td>
</tr>
<tr class="odd">
<td>系統</td>
<td>2</td>
<td>1</td>
<td>此為必要欄位，並符合 MS-DOS 定義。</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="odd">
<td>目錄</td>
<td>4</td>
<td>1</td>
<td>此為必要欄位，並符合 MS-DOS 定義。</td>
</tr>
<tr class="even">
<td>封存</td>
<td>5</td>
<td>1</td>
<td>此為必要欄位，並符合 MS-DOS 定義。</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>7.4.5 CreateTimestamp、Create10msIncrement 和 CreateUtcOffset 欄位

CreateTimestamp 和 CreateTime10msIncrement 欄位組合時，會描述指定的檔案/目錄建立的本機日期和時間。 CreateUtcOffset 欄位描述當地日期和時間與 UTC 之間的時差。 建立指定的目錄專案集時，應設定這些欄位。

這些欄位必須符合 Timestamp、10msIncrement 和 UtcOffset 欄位的定義 (請分別參閱7.4.8、[區段 7.4.9](#749-10msincrement-fields)和[區段 7.4.10](#7410-utcoffset-fields)[一節](#748-timestamp-fields)) 。

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>7.4.6 LastModifiedTimestamp、LastModified10msIncrement 和 LastModifiedUtcOffset 欄位

LastModifiedTimestamp 和 LastModifiedTime10msIncrement 欄位組合時，會描述與指定的資料流程延伸目錄專案相關聯之任何叢集的內容上次修改的本地日期和時間。 LastModifiedUtcOffset 欄位描述當地日期和時間與 UTC 之間的時差。 實作為應更新這些欄位：

1. 在修改任何與指定的資料流程延伸目錄專案相關聯之叢集的內容之後 (除了 ValidDataLength 欄位所描述的內容之外的內容之外) 

2. 變更 ValidDataLength 或 DataLength 欄位的值時

這些欄位必須符合 Timestamp、10msIncrement 和 UtcOffset 欄位的定義 (請分別參閱7.4.8、[區段 7.4.9](#749-10msincrement-fields)和[區段 7.4.10](#7410-utcoffset-fields)[一節](#748-timestamp-fields)) 。

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 LastAccessedTimestamp 和 LastAccessedUtcOffset 欄位

LastAccessedTimestamp 欄位應描述上次存取指定的資料流程延伸目錄專案之任何叢集內容的本地日期和時間。 LastAccessedUtcOffset 欄位描述當地日期和時間與 UTC 之間的時差。
實作為應更新這些欄位：

1. 在修改任何與指定的資料流程延伸目錄專案相關聯之叢集的內容之後 (除了 ValidDataLength 以外的內容之外) 

2. 變更 ValidDataLength 或 DataLength 欄位的值時

在讀取任何與指定的資料流程延伸目錄專案相關聯的叢集內容之後，必須更新這些欄位。

這些欄位必須符合時間戳記和 UtcOffset 欄位的定義 (請) 分別參閱7.4.8 和[區段 7.4.10](#7410-utcoffset-fields)[一節](#748-timestamp-fields)。

#### <a name="748-timestamp-fields"></a>7.4.8 時間戳記欄位

時間戳記欄位會以兩秒的解析度描述本機日期和時間 (請參閱 [資料表 29](#table-29-timestamp-field-structure)) 。

<div id="table-29-timestamp-field-structure" />

**資料表29時間戳記欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>此為必要欄位，而且 <a href="#7481-doubleseconds-field">區段 7.4.8.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Minute</td>
<td>5</td>
<td>6</td>
<td>此為必要欄位，而且 <a href="#7482-minute-field">區段 7.4.8.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>小時</td>
<td>11</td>
<td>5</td>
<td>此為必要欄位，而且 <a href="#7483-hour-field">區段 7.4.8.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>天</td>
<td>16</td>
<td>5</td>
<td>此為必要欄位，而且 <a href="#7484-day-field">區段 7.4.8.4</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>Month</td>
<td>21</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#7485-month-field">區段 7.4.8.5</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>此為必要欄位，而且 <a href="#7486-year-field">區段 7.4.8.6</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>7.4.8.1 DoubleSeconds 欄位

DoubleSeconds 欄位應該會以兩秒的倍數描述時間戳記欄位的秒數部分。

此欄位的有效值範圍應為：

- 0，代表0秒

- 29，代表58秒

##### <a name="7482-minute-field"></a>7.4.8.2 分鐘欄位

[分鐘] 欄位應描述時間戳記欄位的分鐘部分。

此欄位的有效值範圍應為：

- 0，代表0分鐘

- 59，代表59分鐘

##### <a name="7483-hour-field"></a>7.4.8.3 Hour 欄位

[小時] 欄位應描述 [時間戳記] 欄位的小時部分。

此欄位的有效值範圍應為：

- 0，表示00:00 小時

- 23，代表23:00 小時

##### <a name="7484-day-field"></a>7.4.8.4 Day 欄位

Day 欄位必須描述時間戳記欄位的日部分。

此欄位的有效值範圍應為：

- 1，這是指定月份的第一天

- 給定月份的最後一天 (指定的月份會定義有效的天數) 

##### <a name="7485-month-field"></a>7.4.8.5 月份欄位

[月份] 欄位應描述 [時間戳記] 欄位的月份部分。

此欄位的有效值範圍應為：

- 至少1，代表1月

- 最多12個，表示12月

##### <a name="7486-year-field"></a>7.4.8.6 Year 欄位

[年份] 欄位應描述時間戳記欄位的年份部分，相對於1980年。 此欄位代表值為0且年份2107值為127的年份1980。

此欄位的所有可能值都是有效的。

#### <a name="749-10msincrement-fields"></a>7.4.9 10msIncrement 欄位

10msIncrement 欄位應該為其對應的時間戳記欄位提供10毫秒倍數的額外時間解析。

這些欄位之值的有效範圍應為：

- 至少為0，表示0毫秒

- 最多199，代表1990毫秒

#### <a name="7410-utcoffset-fields"></a>7.4.10 UtcOffset 欄位

UtcOffset 欄位 (請參閱 [表 30](#table-30-utcoffset-field-structure)) 描述從 UTC 到相對應的時間戳記和10msIncrement 欄位所述的當地日期和時間的位移。 UTC 與當地日期和時間之間的時差，包括時區和其他日期時間調整的效果，例如日光節約和區域夏季時間變更。

<div id="table-30-utcoffset-field-structure" />

**表 30 UtcOffset 欄位結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>此為必要欄位，而且 <a href="#74101-offsetfromutc-field">區段 7.4.10.1</a>會定義其內容。</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#74102-offsetvalid-field">區段 7.4.10.2</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>7.4.10.1 OffsetFromUtc 欄位

[OffsetFromUtc] 欄位描述的是與當地日期和時間相關的時間戳記與10msIncrement 欄位包含的 UTC 時差。
此欄位會以15分鐘的間隔描述 UTC 的位移 (請參閱表 31) 。

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**表 31 OffsetFromUtc 欄位值的意義**

<table>
<thead>
<tr class="header">
<th><strong>值</strong></th>
<th><strong>帶正負號的十進位相等</strong></th>
<th><strong>說明</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>當地日期和時間是 UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>當地日期和時間是 UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>當地日期和時間是 UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00h</td>
<td>0</td>
<td>當地日期和時間是 UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>當地日期和時間是 UTC –00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41h</td>
<td>-63</td>
<td>當地日期和時間是 UTC –15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>當地日期和時間是 UTC –16:00</td>
</tr>
</tbody>
</table>

如上表所示，此欄位的所有可能值都是有效的。 不過，在下列情況下，執行應該只記錄這個欄位的00h 值：

1. 本機日期和時間實際上與 UTC 相同，在此情況下，OffsetValid 欄位的值應該是1

2. 本機日期和時間是未知的，在此情況下，OffsetValid 欄位的值應該是1，而實值應將 UTC 視為當地日期和時間

3. UTC 是未知的，在此情況下，OffsetValid 欄位的值應為0

如果當地日期和時間與 UTC 之間的時差不是15分鐘間隔的倍數，則在 OffsetFromUtc 欄位中的實作為「00h」就會記錄00h，並且應將 UTC 視為當地日期和時間。

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 OffsetValid 欄位

OffsetValid 欄位應描述 OffsetFromUtc 欄位的內容是否有效，如下所示：

- 0，表示 OffsetFromUtc 欄位的內容無效
    > 和都必須是00h

- 1，表示 OffsetFromUtc 欄位的內容有效

只有當 UTC 無法用於計算 OffsetFromUtc 欄位的值時，才應該將此欄位設定為值0。 如果此欄位包含0這個值，則「實值」會將 Timestamp 和10msIncrement 欄位視為與目前本機日期和時間相同的 UTC 時差。

### <a name="75-volume-guid-directory-entry"></a>7.5 磁片區 GUID 目錄專案

磁片區 GUID 目錄專案包含 GUID，可讓您以獨特的方式和程式設計方式區分磁片區。
磁片區 GUID 以良性的主要目錄專案的形式存在於根目錄中 (請參閱 [資料表 32](#table-32-volume-guid-directoryentry)) 。 有效的磁片區 GUID 目錄專案數目範圍從0到1。

<div id="table-32-volume-guid-directoryentry" />

**資料表32磁片區 GUID DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#751-entrytype-field">區段7.5.1 版</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#752-secondarycount-field">區段7.5.2 版</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#753-setchecksum-field">區段7.5.3 版</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#754-generalprimaryflags-field">區段7.5.4 版</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#755-volumeguid-field">區段 7.5.5</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>保留</td>
<td>22</td>
<td>10</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 版 >entrytype 欄位

>entrytype 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1) [一節](#631-entrytype-field) 。

##### <a name="7511-typecode-field"></a>7.5.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.1) [一節](#6311-typecode-field) 。

針對磁片區 GUID 目錄專案，此欄位的有效值為
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.2) [一節](#6312-typeimportance-field) 。

針對磁片區 GUID 目錄專案，此欄位的有效值為
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.3) [一節](#6313-typecategory-field) 。

##### <a name="7514-inuse-field"></a>7.5.1.4 InUse 欄位

InUse 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.1.4) [一節](#6314-inuse-field) 。

#### <a name="752-secondarycount-field"></a>7.5.2 版 SecondaryCount 欄位

SecondaryCount 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.2) [一節](#632-secondarycount-field) 。

針對磁片區 GUID 目錄專案，此欄位的有效值為
0.

#### <a name="753-setchecksum-field"></a>7.5.3 版 SetChecksum 欄位

SetChecksum 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.3) [一節](#633-setchecksum-field) 。

#### <a name="754-generalprimaryflags-field"></a>7.5.4 版 GeneralPrimaryFlags 欄位

GeneralPrimaryFlags 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱) [6.3.4 一節](#634-generalprimaryflags-field) ，並定義要保留之 CustomDefined 欄位的內容。

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 AllocationPossible 欄位

AllocationPossible 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.4.1) [一節](#6341-allocationpossible-field) 。

針對磁片區 GUID 目錄專案，此欄位的有效值為
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 NoFatChain 欄位

NoFatChain 欄位必須符合一般主要 DirectoryEntry 範本中提供的定義 (請參閱 6.3.4.2) [一節](#6342-nofatchain-field) 。

#### <a name="755-volumeguid-field"></a>7.5.5 VolumeGuid 欄位

VolumeGuid 欄位必須包含可唯一識別指定磁片區的 GUID。

這個欄位的所有可能值都是有效的，但 null GUID 除外，也就是 {00000000-0000-0000-0000-000000000000} 。

### <a name="76-stream-extension-directory-entry"></a>7.6 資料流程延伸模組目錄專案

資料流程延伸目錄專案是檔案目錄專案集中的重要次要目錄專案 (請參閱 [資料表 33](#table-33-stream-extension-directoryentry)) 。 檔案目錄專案集中的資料流程延伸目錄專案有效位數為1。
此外，這個目錄專案只有在緊接在檔案目錄專案之後，才會是有效的。

<div id="table-33-stream-extension-directoryentry" />

**資料表33資料流程延伸模組 DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#761-entrytype-field">區段7.6.1 版</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#762-generalsecondaryflags-field">區段 7.6.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#763-namelength-field">區段 7.6.3</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>此為必要欄位，而且 <a href="#764-namehash-field">區段 7.6.4</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#765-validdatalength-field">區段 7.6.5</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Reserved3</td>
<td>16</td>
<td>4</td>
<td>此為必要欄位，而且其內容為保留。</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#766-firstcluster-field">區段 7.6.6</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#767-datalength-field">區段 7.6.7</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 版 >entrytype 欄位

>entrytype 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1) [一節](#641-entrytype-field) 。

##### <a name="7611-typecode-field"></a>7.6.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.1) [一節](#6411-typecode-field) 。

若為數據流延伸的目錄專案，此欄位的有效值為0。

##### <a name="7612-typeimportance-field"></a>7.6.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.2) [一節](#6412-typeimportance-field) 。

若為數據流延伸的目錄專案，此欄位的有效值為0。

##### <a name="7613-typecategory-field"></a>7.6.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.3) [一節](#6413-typecategory-field) 。

##### <a name="7614-inuse-field"></a>7.6.1.4 InUse 欄位

InUse 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.4) [一節](#6414-inuse-field) 。

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 GeneralSecondaryFlags 欄位

GeneralSecondaryFlags 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱) [6.4.2 一節](#642-generalsecondaryflags-field) ，並定義要保留之 CustomDefined 欄位的內容。

##### <a name="7621-allocationpossible-field"></a>7.6.2.1 AllocationPossible 欄位

AllocationPossible 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.1) [一節](#6421-allocationpossible-field) 。

若為數據流延伸目錄專案，此欄位的有效值為1。

##### <a name="7622-nofatchain-field"></a>7.6.2.2 NoFatChain 欄位

NoFatChain 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.2) [一節](#6422-nofatchain-field) 。

#### <a name="763-namelength-field"></a>7.6.3 NameLength 欄位

NameLength 欄位必須包含 Unicode 字串的長度，而後續的檔案名目錄專案 (請參閱) 統稱的 [第7.7 節](#77-file-name-directory-entry) 。

此欄位的有效值範圍應為：

- 至少1，這是最短的可能檔案名

- 最長255，這是可能的最長檔名

[NameLength] 欄位的值也會影響檔案名稱目錄專案 (請參閱 [7.7) 一節](#77-file-name-directory-entry) 。

#### <a name="764-namehash-field"></a>7.6.4 NameHash 欄位

NameHash 欄位必須包含2個位元組的雜湊 (請參閱 [ [圖 4](#figure-4-namehash-computation) ] 中的大寫檔案名的) 。 這可讓執行程式在依名稱搜尋檔案時執行快速比較。 重要的是，NameHash 會提供不相符的確認驗證。 執行程式應使用最新的大小寫檔案名來確認所有 NameHash 相符專案。

<div id="figure-4-namehash-computation" />

**圖 4 NameHash 計算**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>7.6.5 ValidDataLength 欄位

ValidDataLength 欄位應描述資料串流使用者資料的寫入時間。 當您將資料寫入資料流程時，必須更新此欄位。 在儲存體媒體上，資料資料流程的有效資料長度與資料長度之間的資料是未定義的。 如果讀取作業的有效資料長度超過有效的長度，則實作為讀取作業的實作為。

如果對應的檔案目錄專案描述目錄，則此欄位唯一有效的值會等於 DataLength 欄位的值。 否則，此欄位的有效值範圍應為：

- 至少為0，表示未將任何使用者資料寫入資料流程

- 最多 DataLength，這表示已將使用者資料寫出至整個資料流程長度

#### <a name="766-firstcluster-field"></a>7.6.6 FirstCluster 欄位

FirstCluster 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.3) [一節](#643-firstcluster-field) 。

此欄位應該包含資料串流的第一個叢集的索引，其裝載使用者資料。

#### <a name="767-datalength-field"></a>7.6.7 DataLength 欄位

DataLength 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.4) [一節](#644-datalength-field) 。

如果對應的檔案目錄專案描述目錄，則此欄位的有效值為相關聯配置的整個大小（以位元組為單位），這可能是0。 此外，對於目錄而言，這個欄位的最大值是 256 MB。

### <a name="77-file-name-directory-entry"></a>7.7 檔案名目錄專案

檔案名目錄專案是檔案目錄專案集中重要的次要目錄專案 (請參閱 [資料表 34](#table-34-file-name-directoryentry)) 。 檔案目錄專案集中檔案名目錄專案的有效數目為 NameLength/15，四捨五入到最接近的整數。 此外，只有在緊接以資料流程延伸目錄專案做為連續的系列時，才會將檔案名目錄專案視為有效。 [檔案名] 目錄專案會合並以形成檔案目錄專案集的檔案名。

給定目錄專案的所有子系都必須有唯一的檔案名目錄專案集。 也就是說，在任何一個目錄內的大小寫之後，都不能有重複的檔案或目錄名稱。

<div id="table-34-file-name-directoryentry" />

**資料表34檔案名 DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#771-entrytype-field">區段 7.7.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#772-generalsecondaryflags-field">區段 7.7.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>此為必要欄位，而且 <a href="#773-filename-field">區段 7.7.3</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 >entrytype 欄位

>entrytype 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1) [一節](#641-entrytype-field) 。

##### <a name="7711-typecode-field"></a>7.7.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.1) [一節](#6411-typecode-field) 。

若為數據流延伸目錄專案，此欄位的有效值為1。

##### <a name="7712-typeimportance-field"></a>7.7.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.2) [一節](#6412-typeimportance-field) 。

若為數據流延伸的目錄專案，此欄位的有效值為0。

##### <a name="7713-typecategory-field"></a>7.7.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.3) [一節](#6413-typecategory-field) 。

##### <a name="7714-inuse-field"></a>7.7.1.4 InUse 欄位

InUse 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.4) [一節](#6414-inuse-field) 。

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 GeneralSecondaryFlags 欄位

GeneralSecondaryFlags 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱) [6.4.2 一節](#642-generalsecondaryflags-field) ，並定義要保留之 CustomDefined 欄位的內容。

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 AllocationPossible 欄位

AllocationPossible 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.1) [一節](#6421-allocationpossible-field) 。

若為數據流延伸的目錄專案，此欄位的有效值為0。

##### <a name="7722-nofatchain-field"></a>7.7.2.2 NoFatChain 欄位

NoFatChain 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.2) [一節](#6422-nofatchain-field) 。

#### <a name="773-filename-field"></a>7.7.3 FileName 欄位

FileName 欄位必須包含 Unicode 字串，這是檔案名的一部分。 在檔案目錄專案集的訂購檔案名目錄專案中，FileName 欄位會串連以形成檔案目錄專案集的檔案名。 如果檔案名欄位的長度超過15個字元，且檔案名目錄專案的最大數目為17，則最後一個串連檔案名的長度上限為
255.

串連的檔案名與其他 FAT 型檔案系統有同一組不合法的字元 (請參閱 [資料表 35](#table-35-invalid-filename-characters)) 。 實值應該將檔案名欄位的未使用字元設定為0000h 值。

<div id="table-35-invalid-filename-characters" />

**資料表35不正確檔案名字元**

| **字元碼** | **說明** | **字元碼** | **說明**   | **字元碼** | **說明** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | 控制程式代碼    | 0001h              | 控制程式代碼      | 0002h              | 控制程式代碼    |
| 0003h              | 控制程式代碼    | 0004h              | 控制程式代碼      | 0005h              | 控制程式代碼    |
| 0006h              | 控制程式代碼    | 0007h              | 控制程式代碼      | 0008h              | 控制程式代碼    |
| 0009h              | 控制程式代碼    | 000Ah              | 控制程式代碼      | 000Bh              | 控制程式代碼    |
| 000Ch              | 控制程式代碼    | 000Dh              | 控制程式代碼      | 000Eh              | 控制程式代碼    |
| 000Fh              | 控制程式代碼    | 0010h              | 控制程式代碼      | 0011h              | 控制程式代碼    |
| 0012h              | 控制程式代碼    | 0013h              | 控制程式代碼      | 0014h              | 控制程式代碼    |
| 0015h              | 控制程式代碼    | 0016h              | 控制程式代碼      | 0017h              | 控制程式代碼    |
| 0018h              | 控制程式代碼    | 0019h              | 控制程式代碼      | 001Ah              | 控制程式代碼    |
| 001Bh              | 控制程式代碼    | 001Ch              | 控制程式代碼      | 001Dh              | 控制程式代碼    |
| 001Eh              | 控制程式代碼    | 001Fh              | 控制程式代碼      | 0022h              | 引號  |
| 002Ah              | Asterisk        | 002Fh              | 斜線     | 003Ah              | 冒號           |
| 003Ch              | 小於符號  | 003Eh              | 大於符號 | 003Fh              | 問號   |
| 005Ch              | 反斜線      | 007Ch              | 直槓      |                    |                 |

檔案名 "." 和 "..." 分別具有「這個目錄」和「包含目錄」的特殊意義。 在 [檔案名] 欄位中，「不應該」記錄這些保留的檔案名。
但是，執行可能會在目錄清單中產生這兩個檔案名，以參考所列出的目錄和包含的目錄。

執行可能會想要將檔案和目錄名稱限制為只有 ASCII 字元集。 如果有的話，它們應該將字元使用的字元限制為前128個 Unicode 專案中有效字元的範圍。 它們仍然必須在磁片區上將檔案和目錄名稱儲存為 Unicode，並在與使用者互動時轉譯成 ASCII/Unicode。

### <a name="78-vendor-extension-directory-entry"></a>7.8 廠商延伸模組目錄專案

廠商擴充功能目錄專案是檔案目錄專案集中的良性次要目錄專案 (請參閱 [資料表 36](#table-36-vendor-extension-directoryentry)) 。 檔案目錄專案集可包含任意數目的廠商擴充功能目錄專案，最多可達次要目錄專案的限制，而不是其他次要目錄專案的數目。 此外，廠商延伸的目錄專案只有在不在必要的資料流程延伸模組和檔案名目錄專案之前，才有效。

廠商延伸目錄專案可讓廠商透過 VendorGuid 欄位，在個別的檔案目錄專案集中擁有唯一的廠商專屬目錄專案 (請參閱 [資料表 36](#table-36-vendor-extension-directoryentry)) 。 唯一的目錄專案可以有效地讓供應商擴充 exFAT 檔案系統。 廠商可以定義 Vendordefined 向欄位的內容 (請參閱 [資料表 36](#table-36-vendor-extension-directoryentry)) 。 廠商的實施可能會維護 Vendordefined 向欄位的內容，並可提供廠商特有的功能。

無法辨識廠商延伸模組目錄專案的 GUID 的執行，應將目錄專案視為與任何其他無法辨識的良性次要目錄專案相同 (請參閱 [第8.2 節](#82-implications-of-unrecognized-directory-entries)) 。

<div id="table-36-vendor-extension-directoryentry" />

**表36廠商延伸模組 DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#781-entrytype-field">區段 7.8.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#782-generalsecondaryflags-field">區段 7.8.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#783-vendorguid-field">區段 7.8.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Vendordefined 向</td>
<td>18</td>
<td>14</td>
<td>此為必要欄位，而且廠商可以定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 >entrytype 欄位

>entrytype 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1) [一節](#641-entrytype-field) 。

##### <a name="7811-typecode-field"></a>7.8.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.1) [一節](#6411-typecode-field) 。

針對廠商擴充功能目錄專案，此欄位的有效值為0。

##### <a name="7812-typeimportance-field"></a>7.8.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.2) [一節](#6412-typeimportance-field) 。

針對廠商擴充功能目錄專案，此欄位的有效值為1。

##### <a name="7813-typecategory-field"></a>7.8.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.3) [一節](#6413-typecategory-field) 。

##### <a name="7814-inuse-field"></a>7.8.1.4 版 InUse 欄位

InUse 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.4) [一節](#6414-inuse-field) 。

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 GeneralSecondaryFlags 欄位

GeneralSecondaryFlags 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱) [6.4.2 一節](#642-generalsecondaryflags-field) ，並定義要保留之 CustomDefined 欄位的內容。

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 版 AllocationPossible 欄位

AllocationPossible 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.1) [一節](#6421-allocationpossible-field) 。

針對廠商擴充功能目錄專案，此欄位的有效值為0。

##### <a name="7822-nofatchain-field"></a>7.8.2.2 NoFatChain 欄位

NoFatChain 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.2) [一節](#6422-nofatchain-field) 。

#### <a name="783-vendorguid-field"></a>7.8.3 VendorGuid 欄位

VendorGuid 欄位必須包含可唯一識別指定廠商延伸模組的 GUID。

這個欄位的所有可能值都是有效的，但 null GUID 除外，也就是 {00000000-0000-0000-0000-000000000000} 。 不過，廠商應該使用 GUID 產生工具（例如 GuidGen.exe），在定義擴充功能時選取 GUID。

此欄位的值會決定 Vendordefined 向欄位的供應商特定結構。

### <a name="79-vendor-allocation-directory-entry"></a>7.9 廠商配置目錄專案

廠商配置目錄專案是檔案目錄專案集中的良性次要目錄專案 (請參閱 [資料表 37](#table-37-vendor-allocation-directoryentry)) 。 檔案目錄專案集可包含任意數目的廠商配置目錄專案，最多可達次要目錄專案的限制，而不是其他次要目錄專案的數目。 此外，只有在所需的資料流程延伸模組和檔案名目錄專案之前，廠商配置目錄專案才會有效。

廠商配置目錄專案可讓廠商透過 VendorGuid 欄位，在個別的檔案目錄專案集中擁有唯一的廠商專屬目錄專案 (請參閱 [資料表 37](#table-37-vendor-allocation-directoryentry)) 。 唯一的目錄專案可以有效地讓供應商擴充 exFAT 檔案系統。 廠商可以定義相關聯叢集的內容（如果有的話）。 廠商的實施可能會維護相關聯叢集的內容（如果有的話），並可提供廠商特有的功能。

無法辨識供應商配置目錄專案之 GUID 的執行作業，應該將目錄專案視為與任何其他無法辨識的良性次要目錄專案相同 (請參閱 [8.2 節](#82-implications-of-unrecognized-directory-entries)) 。

<div id="table-37-vendor-allocation-directoryentry" />

**表37廠商配置 DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>entrytype</td>
<td>0</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#791-entrytype-field">區段 7.9.1</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>此為必要欄位，而且 <a href="#792-generalsecondaryflags-field">區段 7.9.2</a> 會定義其內容。</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>此為必要欄位，而且 <a href="#793-vendorguid-field">區段 7.9.3</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>Vendordefined 向</td>
<td>18</td>
<td>2</td>
<td>此為必要欄位，而且廠商可以定義其內容。</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>此為必要欄位，而且 <a href="#794-firstcluster-field">區段 7.9.4</a> 會定義其內容。</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>此為必要欄位，而且 <a href="#795-datalength-field">區段 7.9.5</a> 會定義其內容。</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 >entrytype 欄位

>entrytype 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1) [一節](#641-entrytype-field) 。

##### <a name="7911-typecode-field"></a>7.9.1.1 TypeCode 欄位

TypeCode 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.1) [一節](#6411-typecode-field) 。

針對廠商配置目錄專案，此欄位的有效值為1。

##### <a name="7912-typeimportance-field"></a>7.9.1.2 TypeImportance 欄位

TypeImportance 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.2) [一節](#6412-typeimportance-field) 。

針對廠商配置目錄專案，此欄位的有效值為1。

##### <a name="7913-typecategory-field"></a>7.9.1.3 TypeCategory 欄位

TypeCategory 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.3) [一節](#6413-typecategory-field) 。

##### <a name="7914-inuse-field"></a>7.9.1.4 InUse 欄位

InUse 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.1.4) [一節](#6414-inuse-field) 。

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 GeneralSecondaryFlags 欄位

GeneralSecondaryFlags 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱) [6.4.2 一節](#642-generalsecondaryflags-field) ，並定義要保留之 CustomDefined 欄位的內容。

##### <a name="7921-allocationpossible-field"></a>7.9.2.1 AllocationPossible 欄位

AllocationPossible 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.1) [一節](#6421-allocationpossible-field) 。

針對廠商配置目錄專案，此欄位的有效值為1。

##### <a name="7922-nofatchain-field"></a>7.9.2.2 NoFatChain 欄位

NoFatChain 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.2.2) [一節](#6422-nofatchain-field) 。

#### <a name="793-vendorguid-field"></a>7.9.3 VendorGuid 欄位

VendorGuid 欄位必須包含可唯一識別指定供應商配置的 GUID。

這個欄位的所有可能值都是有效的，但 null GUID 除外，也就是 {00000000-0000-0000-0000-000000000000} 。 不過，廠商應該使用 GUID 產生工具（例如 GuidGen.exe），在定義擴充功能時選取 GUID。

此欄位的值會決定相關聯之叢集內容的廠商特定結構（如果有的話）。

#### <a name="794-firstcluster-field"></a>7.9.4 FirstCluster 欄位

FirstCluster 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.3) [一節](#643-firstcluster-field) 。

#### <a name="795-datalength-field"></a>7.9.5 DataLength 欄位

DataLength 欄位必須符合一般次要 DirectoryEntry 範本中提供的定義 (請參閱 6.4.4) [一節](#644-datalength-field) 。

### <a name="710-texfat-padding-directory-entry"></a>7.10 TexFAT 填補目錄專案

此規格（exFAT 修訂1.00 檔案系統基本規格）不會定義 TexFAT 填補目錄專案。 不過，其類型代碼是1，而其類型重要性為1。 此規格的執行應該會將 TexFAT 填補目錄專案視為與任何其他無法辨識的良性主要目錄專案相同，因此，不應移動 TexFAT 填補目錄專案。

## <a name="8-implementation-notes"></a>8個執行注意事項

### <a name="81-recommended-write-ordering"></a>8.1 建議的寫入順序

實作為可確保磁片區盡可能具有復原能力，以及其他無法避免的錯誤。 建立新的目錄專案或修改叢集配置時，通常應遵循下列撰寫順序：

1. 將 VolumeDirty 欄位的值設定為1

2. 視需要更新作用中的 FAT

3. 更新使用中配置點陣圖

4. 視需要建立或更新目錄專案

5. 如果第一個步驟之前的值為0，請清除 [VolumeDirty] 欄位的值為0

刪除目錄專案或釋放叢集配置時，執行應遵循下列撰寫順序：

1. 將 VolumeDirty 欄位的值設定為1

2. 如有必要，請刪除或更新目錄專案

3. 視需要更新作用中的 FAT

4. 更新使用中配置點陣圖

5. 如果第一個步驟之前的值為0，請清除 [VolumeDirty] 欄位的值為0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8.2 無法辨識之目錄專案的含意

相同主要修訂編號、1和次要修訂編號（大於0）的未來 exFAT 規格，可能會定義新的良性主要、重大次要和良性次要目錄專案。 只有較高主要修訂編號的 exFAT 規格可以定義新的重要主要目錄專案。 此規格的實作為 exFAT 修訂1.00 檔案系統基本規格，應該能夠掛接和存取任何主要修訂編號1和任何次要修訂編號的 exFAT 磁片區。 這會呈現可能會遇到無法辨識之目錄專案的情況。 以下說明這些案例的含意：

1. 根目錄中有無法辨識的重要主要目錄專案會呈現不正確磁片區。 在任何非根目錄中，除了檔案目錄專案以外，任何重要的主要目錄專案都會呈現不正確裝載目錄。

2. 執行不應修改無法辨識的良性主要目錄專案或其相關聯的叢集配置。 不過，刪除目錄時，以及只有在刪除目錄時，執行應刪除無法辨識的良性主要目錄專案，並釋放所有相關聯的叢集配置（如果有的話）。

3. 執行不應修改無法辨認的重要次要目錄專案或其相關聯的叢集配置。 目錄專案集中有一或多個無法辨識的重要次要目錄專案，會轉譯整個目錄專案集無法辨識。 當您刪除包含一或多個無法辨識的重要次要目錄專案的目錄專案集時，必須釋放與無法辨識的重要次要目錄專案相關聯的所有叢集配置（如果有的話）。
   此外，如果目錄專案集描述目錄，則可能會執行下列動作：

   - 跨越目錄

   - 列舉其包含的目錄專案

   - 刪除包含的目錄專案

   - 將包含的目錄專案移至不同的目錄

   但是，執行不應：

   - 修改內含的目錄專案（刪除除外），如所述

   - 建立新的包含目錄專案

   - 開啟包含的目錄專案（依所述的往返和列舉除外）

4. 執行不應修改無法辨識的良性次要目錄專案或其相關聯的叢集配置。
   實作為應忽略無法辨識的良性次要目錄專案。 刪除目錄專案集時，必須釋放與無法辨識的良性次要目錄專案相關聯的所有叢集配置（如果有的話）。

## <a name="9-file-system-limits"></a>9檔案系統限制

### <a name="91-sector-size-limits"></a>9.1 磁區大小限制

BytesPerSectorShift 欄位會定義最低和最大磁區大小的限制 (評估為 **下限：512個位元組; 上限：4096個位元組**) 。

### <a name="92-cluster-size-limits"></a>9.2 叢集大小限制

SectorsPerClusterShift 欄位會定義 (**下限：1個磁區; 上限： 25--BytesPerSectorShift 個磁區** 的下限和上限叢集大小限制，其會評估為 32mb) 。

### <a name="93-cluster-heap-size-limits"></a>9.3 叢集堆積大小限制

叢集堆積至少應包含足夠的空間來裝載下列基本檔案系統結構：根目錄、所有配置點陣圖和向上案例資料表。

較低的叢集堆積大小限制是位於叢集堆積中每個基本檔案系統結構的大小下限的函數。 即使有最小的可能叢集 (512 個位元組) ，每個基本檔案系統結構都不需要一個以上的叢集。 因此， **下限為： 2 + NumberOfFats** 叢集，根據 [NumberOfFats] 欄位的值，評估為3或4個群集。

叢集堆積大小上限是最大可能的群集數目的簡單函式，ClusterCount 欄位會定義 (**上限： 2 <sup>32</sup>-11** 叢集) 。 無論叢集大小為何，這類叢集堆積都有足夠的空間可至少裝載基本檔案系統結構。

### <a name="94-volume-size-limits"></a>9.4 磁片區大小限制

VolumeLength 欄位會定義 (下限： **2 <sup>20</sup>/2 <sup>BytesPerSectorShift</sup>磁區**（評估為 1 mb）的下限和上限磁片區大小限制： **上限： 2 <sup>64</sup>-1 個磁區**，根據最大的磁區大小，評估為大約 64ZB) 。 不過，此規格建議在叢集堆積中不超過2個<sup>24</sup>-2 的叢集 (請參閱 [3.1.9) 一節](#319-clustercount-field) 。 因此，磁片區的建議上限是： ClusterHeapOffset + (2<sup>24</sup>-2) \* 2<sup>SectorsPerClusterShift</sup>。 假設有最大的叢集大小、32MB 和假設 ClusterHeapOffset 是 96MB (足夠的空間供主要和備份開機區域使用，而且只有第一個 FAT) ，建議的磁片區上限會評估為大約512TB。

### <a name="95-directory-size-limits"></a>9.5 目錄大小限制

資料流程延伸目錄專案的 DataLength 欄位會定義 (**下限：0位元組、上限： 256mb**) 的下限和上限目錄大小限制。 這表示目錄最多可裝載8388608個目錄專案 (每個目錄專案都會耗用32個位元組) 。 假設有最小的檔案目錄專案集（三個目錄專案），目錄最多可裝載2796202個檔案。

## <a name="10-appendix"></a>10附錄

### <a name="101-globally-unique-identifiers-guids"></a>10.1 (Guid) 全域唯一識別碼

GUID 是全域唯一識別碼的 Microsoft 實作為。 GUID 是128位值，其中包含8個十六進位數位的一個群組，後面接著三個4個十六進位數位的群組，後面接著一個12個十六進位數位（例如 {6B29FC40-CA47-1067-B31D-00DD010662DA}）， (參閱 [表 38](#table-38-guid-structure)) 。

<div id="table-38-guid-structure" />

**資料表 38 GUID 結構**

<table>
<thead>
<tr class="header">
<th><strong>功能變數名稱</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><p><strong>大小</strong></p>
<p><strong> (位元組) </strong></p></th>
<th><strong>註解</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>此為必要欄位，而且包含從範例)  (6B29FC40h 的第一個 GUID 群組中的四個位元組。</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>此為必要欄位，而且包含從範例)  (CA47h 的第二個 GUID 群組中的兩個位元組。</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>此為必要欄位，而且包含從範例)  (1067h 的第三個 GUID 群組中的兩個位元組。</td>
</tr>
<tr class="even">
<td>Data4 [0]</td>
<td>8</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (B3h 的第四個 GUID 群組中最重要的位元組。</td>
</tr>
<tr class="odd">
<td>Data4 [1]</td>
<td>9</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (1Dh 的第四個 GUID 群組中最重要的位元組。</td>
</tr>
<tr class="even">
<td>Data4 [2]</td>
<td>10</td>
<td>1</td>
<td>此為必要欄位，包含範例) 的第五組 GUID (00h 的第一個位元組。</td>
</tr>
<tr class="odd">
<td>Data4 [3]</td>
<td>11</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (DDh 的第五個 GUID 群組中的第二個位元組。</td>
</tr>
<tr class="even">
<td>Data4 [4]</td>
<td>12</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (01h 的第五個 GUID 群組中的第三個位元組。</td>
</tr>
<tr class="odd">
<td>Data4 [5]</td>
<td>13</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (06h 的第五個 GUID 群組中的第四個位元組。</td>
</tr>
<tr class="even">
<td>Data4 [6]</td>
<td>14</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (62h 的第五個 GUID 群組中的第五個位元組。</td>
</tr>
<tr class="odd">
<td>Data4 [7]</td>
<td>15</td>
<td>1</td>
<td>此為必要欄位，而且包含從範例)  (DAh 的第五個 GUID 群組中的第六個位元組。</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10.2 資料分割資料表

為了確保 exFAT 磁片區在一組廣泛使用案例中的互通性，執行程式應針對 MBR 分割區儲存體使用分割類型07h，並針對 GPT 分割儲存體使用分割 GUID {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7}。

## <a name="11-documentation-change-history"></a>11檔變更歷程記錄

表格39描述此檔的版本、更正、新增專案、移除及說明的歷程記錄。

<div id="table-39-documentation-change-history" />

**表39檔變更歷程記錄**

<table>
<thead>
<tr class="header">
<th><strong>日期</strong></th>
<th><strong>變更的描述</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-01-2008</td>
<td><p>基本規格的第一版，包括：</p>
<blockquote>
<p>第1節，簡介</p>
<p>第2節：<br />
磁片區結構</p>
<p>第3節，主要和備份開機區域</p>
<p>第4節，檔案配置資料表區域</p>
<p>第5節，資料區域</p>
<p>第6節，目錄結構</p>
<p>第7節，目錄專案定義</p>
<p>第8節，執行附注</p>
<p>第9節，檔案系統限制</p>
<p>第10節，附錄</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-6 月-2008</td>
<td><p>基本規格的第二個版本，其中包括下列變更：</p>
<blockquote>
<p>第11節的加法<br />
檔變更歷程記錄</p>
<p>在7.8 和7.9 區段中新增廠商擴充功能和廠商配置目錄專案</p>
<p>在區段7.2.5 和7.2.5.1 中新增建議的案例資料表</p>
<p>新增第7.4 節中的 UtcOffset 欄位，並新增第1.3 節中的 UTC 縮寫</p>
<p>資料表19中 CustomDefined 欄位大小的更正</p>
<p>區段7.6.3 中 NameLength 值的有效範圍修正</p>
<p>第7.4 節中的時間戳記和10msIncrement 欄位的更正和澄清</p>
<p>第3.3 節中的 Null 參數結構澄清</p>
<p>說明區段6.3.4.2 中 NoFatChain 欄位的值意義</p>
<p>說明區段上面6.2.3 中 DataLength 欄位的值意義</p>
<p>說明區段3.1.13.2 中的 VolumeDirty 欄位，以及第8.1 節的建議寫入順序</p>
<p>3.1.13.3 區段中的 MediaFailure 欄位澄清</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-10 月-2008</td>
<td><p>基本規格的第三個版本，其中包括下列變更：</p>
<blockquote>
<p>加法應為，而且可能是現場說明</p>
<p>在表2區段1.3 中新增 UTC 定義</p>
<p>修改了章節1.5，以確保與 TexFAT 規格檔一致。</p>
<p>明確說明只有 Microsoft 可能會在6.2 節中定義目錄專案版面配置的限制</p>
<p>已新增澄清 FirstCluster 欄位應為零（如果 DataLength 為零且 NoFatChain 設定為區段6.3.5 和區段6.4.3）</p>
<p>闡明瞭第7.4 節中有效檔案目錄專案的需求</p>
<p>已將唯一檔案和目錄名稱的需求新增至區段7。7</p>
<p>已將 ASCII 的執行附注新增至區段結尾7.7。3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-1 月-2009</td>
<td><p>基本規格的第四個版本，其中包括下列變更：</p>
<blockquote>
<p>已移除 Windows CE 存取控制專案的參考</p>
<p>已新增澄清區段7.2.5.1 以明確要求完整的案例資料表</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-09-2009</td>
<td><p>第五版的基本規格，其中包括下列變更：</p>
<blockquote>
<p>檔案格式變更以允許更好的 PDF 轉換</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24-2 月-2010</td>
<td><p>基本規格的第六個版本，其中包括下列變更：</p>
<blockquote>
<p>修改了不正確的語句：「如果 DataLength 為零，並將 NoFatChain 設定為」區段6.3.5 中的「FirstCluster 欄位應為零，而設定為」。如果6.4.3 位為1，則 NoFatChain 必須指向叢集堆積中的有效叢集」，以說明如果已設定 FirstCluster 位，則必須有有效的配置。</p>
<p>已新增 "如果 NoFatChain 位為1，則 DataLength 不得為零。 如果 FirstCluster 欄位為零，則 DataLength 也必須是零 "到區段6.3.6 和區段6.4.4，以說明如果設定 NoFatChain 位，必須有有效的配置。</p>
<p>已將著作權聲明更新為2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26-08-2019</td>
<td><p>基本規格的第七個版本，其中包括下列變更：</p>
<blockquote>
<p>更新與規格相關的法律條款，包括：</p>
<p>移除 Microsoft 機密通知</p>
<p>移除 Microsoft Corporation 技術檔授權合約區段</p>
<p>已將著作權聲明更新為2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
