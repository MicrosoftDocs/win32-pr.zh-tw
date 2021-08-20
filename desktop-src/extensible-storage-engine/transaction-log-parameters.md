---
description: 深入瞭解：交易記錄參數
title: 交易記錄檔參數
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: d7e8b3e206c4d13cfe4b4170298327a03ac8be5038873f6d2f6c1c79827923a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117702030"
---
# <a name="transaction-log-parameters"></a>交易記錄檔參數


_**適用于：** Windows |Windows伺服器_

**本文內容**  
交易記錄檔參數  
需求  
另請參閱  

## <a name="transaction-log-parameters"></a>交易記錄檔參數

本主題包含用於交易記錄的參數。

*JET_paramBaseName*  
3  

此參數會設定用於資料庫引擎所使用之許多檔案的三個字母前置詞。 例如，檢查點檔案稱為「EDB」。因為 EDB 是預設的基底名稱，所以預設為使用 .CHK。 基底名稱可以用來輕鬆區分屬於不同實例或不同應用程式的檔案集合。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;edb.log&quot;</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>3個字元</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramCircularLog*  
17  

此參數會設定資料庫引擎管理交易記錄檔的方式。

當迴圈記錄關閉時，所產生的所有交易記錄檔都會保留在磁片上，直到不再需要該檔案，因為已執行資料庫的完整備份。 在此模式中，您可以從較舊的備份進行還原，並在所有保留的交易記錄檔中向前播放，如此一來，萬一發生強制還原的損毀，就不會遺失任何資料。 需要定期完整備份，以防止磁片填滿交易記錄檔。

當迴圈記錄開啟時，只有小於目前檢查點的交易記錄檔會保留在磁片上。 這種模式的好處是，備份不需要淘汰舊的交易記錄檔。 缺點是已不再有零的資料遺失還原。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramCommitDefault*  
16  

此參數會控制在會話上認可最外層交易時所採取的預設動作。 任何可以傳遞給 [JetCommitTransaction](./jetcommittransaction-function.md) 的有效選項，也可以做為實例中所有會話的預設值和/或特定會話的預設值。 如需這些選項的詳細資訊，請參閱 [JetCommitTransaction](./jetcommittransaction-function.md) 。

此參數會影響交易的可靠性和效能。 如需詳細資訊，請參閱 [JetCommitTransaction](./jetcommittransaction-function.md) 。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>JET_GRBIT (整數) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>適用于 JetCommitTransaction 的有效選項</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>實例或會話</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOldLogs*  
48  

當此參數為 true，且記錄檔路徑所指向的交易記錄檔 (**JET_paramLogFilePath**) 都是過時的版本，則這些交易記錄檔將會自動刪除。

**Windows 2000：** 從 Windows NT 將資料庫升級至 Windows 2000 時，必須小心使用此參數。 如果資料庫不是處於一致的狀態，而且舊的記錄檔遭到刪除，則資料庫的內容將會遺失。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000：</strong> 假</p>
<p><strong>Windows XP：</strong> 真</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramIgnoreLogVersion*  
47  

如果此參數為 true，則資料庫引擎將不會在 [JetInit](./jetinit-function.md)期間驗證交易記錄檔的版本號碼。

**Windows XP：** 從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

此參數提供舊版資料庫引擎的檔案命名慣例回溯相容性。

目前支援下列選項：

JET_bitESE98FileNames

當這個選項存在時，database engine 會針對其檔案使用下列命名慣例：

  - 交易記錄檔將會使用。記錄檔的副檔名

  - 檢查點檔案將會使用。副檔名的 .CHK

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>JET_GRBIT (整數) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0、JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>WindowsVista 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramLogBuffers*  
12  

此參數會設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。 此參數的單位是保存交易記錄檔之磁片區的磁區大小。 磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。

此參數會對效能造成影響。 當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。 交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。 在此情況下，已知的預設值太小。

**Windows XP 和 Windows 2000：** 在 Windows XP 和舊版中，不建議將此參數設定為大於交易記錄檔大小一半的緩衝區數目（以位元組為單位) ） (。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 80</p>
<p><strong>Windows Vista：</strong> 126</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 80 –2147483647</p>
<p><strong>Windows Vista：</strong> 1-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLogCheckpointPeriod*  
14  

此參數會設定資料庫引擎在產生指定的記錄檔磁區數目時，採取檢查點。

**Windows XP：** 從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileCreateAsynch*  
69  

當這個參數設定為 true 時，資料庫引擎會建立下一個交易記錄檔，因為目前的交易記錄檔已被取用。 其目的是要將從一個交易記錄檔切換至下一個交易記錄檔所花費的時間降至最低，以大幅更新負載。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>是</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>WindowsXP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFilePath*  
2 

此參數表示將包含實例之交易記錄之資料夾的相對或絕對檔案系統路徑。 路徑必須以反斜線字元結束，表示目標路徑是資料夾。 交易記錄檔包含在損毀之後將資料庫檔案帶入一致狀態所需的資訊。 它們通常名為 EDB \* 。日誌。 交易記錄檔的內容就和資料庫檔案本身一樣，)  (也一樣重要。 每個努力都應該進行保護。

此外也會有名為 RES1 的其他保留記錄檔。記錄檔和 RES2。連同一般記錄檔一起儲存的記錄檔。 這些檔案的內容並不重要，因為其唯一的目的是保留磁碟空間，以允許引擎在低磁片案例中正常關機。 這些也會是暫時的記錄檔，通常名為 EDBTMP。登入相同的資料夾。 這兩個檔案的內容並不重要。 這個檔案是準備好使用的新記錄檔。

交易記錄檔之主機磁片區的屬性及其相對於資料庫引擎所使用之其他檔案的位置，可能會大幅影響效能。

**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;.\&q</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>資料夾路徑 (字串) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0–246個字元</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileSize*  
11  

此參數會設定交易記錄檔的大小。 每個交易記錄檔都是固定的大小。 大小等於這個系統參數的設定（單位為1024個位元組）。

此參數會對可靠性造成影響。 如果設定太小，則會更快達到 (1048575) 的記錄檔數目上限。 發生這種情況時，必須完全關閉實例、必須刪除現有的記錄檔，而且必須重新開機實例。 此動作不僅會降低應用程式的可用性，也會使應用程式資料庫的任何先前備份失效。

此參數會對效能造成影響。 如果設定非常大，則 [JetInit](./jetinit-function.md) 會變慢，因為資料庫引擎在初始化時，至少必須讀取最年輕記錄檔 (的) 。 如果設定非常大，則在記錄檔之間切換時也需要較長的時間。 如果設定非常小，則需要為指定的更新數目建立更多記錄檔，這樣會增加額外負荷。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>5120</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 128 –32768</p>
<p><strong>Windows Vista：</strong> 64 –32768</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLogWaitingUserMax*  
15  

此參數會嘗試將長期認可所造成的記錄緩衝區排清優化，方法是在希望另一個交易共用排清的情況下，等候指定的會話數目等待永久性認可。

**Windows XP：** 從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramRecovery*  
34  

此參數是控制實例損毀復原的主切換。 如果此參數設定為 "On"，則會使用 >ARIES 樣式復原，在進程或電腦損毀時，將實例中的所有資料庫帶到一致的狀態。 如果此參數設定為 "Off"，則會管理實例中的所有資料庫，而不會有損毀復原的優點。 也就是說，如果實例未在進程結束或電腦關機之前使用 [JetTerm](./jetterm-function.md) 完全關閉，則該實例中所有資料庫的內容將會損毀。

在特殊情況下，停用復原會很有用，因為在這種情況下，資料庫的內容在發生損毀的情況下不會很有用。 所有其他情況都應啟用復原。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;開啟&quot;</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0–259個字元</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramSystemPath*  
0  

此參數表示將包含實例之檢查點檔案之資料夾的相對或絕對檔案系統路徑。 路徑必須以反斜線字元結束，表示目標路徑是資料夾。 檢查點檔案是每個實例維護的簡單檔案，可記住必須重新執行的最舊交易記錄檔，以便在損毀之後將該實例中的所有資料庫帶到一致的狀態。 檢查點檔案通常名為 EDB。.CHK.

**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;.\&q</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>資料夾路徑 (字串) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0–246個字元</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramWaitLogFlush*  
13 

此參數會嘗試將長期認可所造成之記錄緩衝區的排清優化，方法是在希望另一個交易共用排清之前等候一段指定的時間。

**Windows XP：** 從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>實例或會話</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

這個參數是用來指定要使用 Windows Server 2003 和先前的檔案命名配置來維護的檔案命名相容性功能。 如需有關不同檔案及其命名的詳細資訊，請參閱[可擴充的儲存體引擎](./extensible-storage-engine-files.md)檔案。

JET_bitESE98FileNames 可確保用於交易記錄檔和檢查點檔案的副檔名，與 Windows Server 2003 中使用的副檔名相同。 注意：如果從 Windows Server 2003 升級，則仍不需要指定此項，因為當 JET_paramCircularLog 設定為 **true** 時，引擎會自動升級副檔名，如果 JET_paramCircularLog 為 **false**，則保留較舊的記錄檔延伸模組。

**注意**  若要設定位，應先取出值，然後在所需的相容性位中取出 "or"。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>JET_GRBIT (整數) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>從 Windows Server 2008 和 Windows Vista 開始</p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
