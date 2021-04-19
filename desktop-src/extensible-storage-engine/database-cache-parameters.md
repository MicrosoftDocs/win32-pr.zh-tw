---
description: 深入瞭解：資料庫快取參數
title: 資料庫快取參數
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974548"
---
# <a name="database-cache-parameters"></a>資料庫快取參數


_**適用于：** Windows |Windows Server_

## <a name="database-cache-parameters"></a>資料庫快取參數

本主題包含用於資料庫快取的參數。

*JET_paramBatchIOBufferMax*  
22  

此參數會控制資料庫頁面快取的輔助部分大小，該部分在其他情況下無法使用時，用來模擬散佈收集 i/o。 大小是在資料庫頁面中。

**WINDOWS XP 和更新版本：**  此參數已過時，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0、2-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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


*JET_paramCacheSize*  
41  

這個參數可以用來控制執行時間的資料庫頁面快取大小。 一般來說，快取會自動將其大小調整為資料庫和電腦活動層級的功能。 如果應用程式將此參數設定為零，則快取會以這種方式調整其本身的大小。 但是，如果應用程式將此參數設定為非零值，則快取會將其本身調整為資料庫頁面)  (的目標大小。 然後，快取會將其大小保留為該閾值，直到指定新的大小或釋放它以選擇其本身的大小為止。

**注意**  快取大小仍受限於 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所加諸的限制。

讀取此參數時，會傳回資料庫頁面中的實際快取大小。 應用程式可使用此大小做為輸入，以驅動其手動調整快取大小。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>特殊</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  1 –1048575</p>
<p><strong>WINDOWS XP：</strong>  1-4294967295</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
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
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMin*  
60  

此參數會設定資料庫頁面快取的大小下限。 大小是在資料庫頁面中。

根據預設，資料庫快取會在 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所設定的限制之間自動調整其大小。

**Windows 2000：**  在 Windows 2000 上，此參數的值應該設定為大約等於四倍的執行緒數目，這些執行緒會同時位於 ESE API 內。 這是為了避免資料庫頁面快取緩衝區數目不足所造成的鎖死，以執行像 B + 樹狀結構分割的複雜作業。

**WINDOWS XP 和更新版本：**  快取管理員會自動設定自己的最小快取大小，以避免鎖死。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000：</strong>  64</p>
<p><strong>WINDOWS XP：</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  1 –1048575</p>
<p><strong>WINDOWS XP：</strong>  1-4294967295</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p><strong>Windows 2000：</strong>  不</p>
<p><strong>WINDOWS XP：</strong>  是的</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p><strong>Windows 2000：</strong>  不</p>
<p><strong>WINDOWS XP：</strong>  是的</p></td>
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


*JET_paramCacheSizeMax*  
23  

此參數會設定資料庫頁面快取的大小上限。 大小是在資料庫頁面中。

根據預設，資料庫快取會在 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所設定的限制之間自動調整其大小。

**注意**   如果此參數保留為其預設值，則在呼叫 [JetInit](./jetinit-function.md) 時，會將快取的大小上限設定為實體記憶體的大小。

**Windows Vista：**  在 Windows Vista 中，此參數的預設值已變更，以闡明此行為。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  512</p>
<p><strong>Windows Vista：</strong>  2000000000</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  1 –1048575</p>
<p><strong>WINDOWS XP：</strong>  1-4294967295</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p><strong>Windows 2000：</strong>  不</p>
<p><strong>WINDOWS XP：</strong>  是的</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p><strong>WINDOWS XP 和 windows 2000：</strong>  不</p>
<p><strong>Windows Vista 和 Windows Server 2003：</strong>  是的</p></td>
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


*JET_paramCheckpointDepthMax*  
24 

此參數會控制從資料庫頁面快取清除資料庫頁面的方式，以將從損毀復原所需的時間降至最低。 參數是一種閾值，以位元組為單位，表示在損毀之後必須重新執行的交易記錄檔數目。

如果使用 [JET_paramCircularLog](./transaction-log-parameters.md) 啟用迴圈記錄，此參數也會控制要保留在磁片上的交易記錄檔大約數量。

此參數的設定必須太低。 因為這個參數的值接近零，所以快取在將資料庫頁面排清至磁片時，會變得越來越多。 這並不只會導致資料庫檔案的寫入數目增加，也會間接造成這些檔案的讀取次數增加。 在某些情況下，這可能會造成極大的效能問題。 可惜的是，為此參數設定最小的最佳值只能透過目標應用程式的實驗來完成。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  0 –2147483647</p>
<p><strong>Windows Vista：</strong>  所有值</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong> 此參數為 global。</p>
<p><strong>Windows Vista：</strong>  此參數為每個實例。</p></td>
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
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointIOMax*  
135  

此參數會控制資料庫引擎將用來排清修改過的資料庫頁面，以使檢查點前進的最大並行寫入數目。 此參數的值可用來平衡檢查點的速度，以及此進程對保存資料庫的磁片之其他 i/o 作業的回應時間所造成的負面影響。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>8–1024</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
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
<td><p>Windows Vista 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

當此參數為 **True** 時，資料庫引擎將直接從 Windows 檔案快取使用資料庫資料，而不是將快取的資料複製到它自己的私用記憶體中。 任何修改過的資料庫資料仍會快取在私用記憶體中。

這種模式的目的是要進一步減少 database engine 用來快取資料庫資料的私用記憶體量。

只有在使用 Windows 檔案快取時，您可以將 JET_paramEnableFileCache 設定為 **True**，才能使用 view cache。

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
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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
<td><p>Windows Vista 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

此參數會設定以微秒為單位的時間間隔，這會將兩個資料庫頁面存取視為相互關聯。 此相互關聯間隔可控制快取頁面取代演算法的敏感度， (LRU-K) 至後續的頁面存取。 接著，這會影響其選擇要保持快取的頁面。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>128000</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>    0 –2147483647</p>
<p><strong>Windows Vista：</strong>  所有值</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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


*JET_paramLRUKHistoryMax*  
26  

此參數會設定將保留資料庫頁面存取時間的非快取資料庫頁面數目上限。 這些記錄可讓快取的頁面取代演算法 (LRU-K) ，更精確地偵測錯誤地從資料庫頁面快取中收回的熱門頁面。

**WINDOWS XP 和 Windows Server 2003：**  Windows XP 和 Windows Server 2003 會忽略此參數，且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000：</strong>  1024</p>
<p><strong>Windows Vista：</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  0 –4194303</p>
<p><strong>Windows Vista：</strong>  所有值</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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


*JET_paramLRUKPolicy*  
27  

此參數會設定視為用來判斷頁面實用性的資料庫頁面存取數目。 此參數基本上是 LRU-K 中的 K，也就是資料庫頁面快取的頁面取代演算法。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>1 - 2</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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


*JET_paramLRUKTimeout*  
28

此參數表示以秒為單位的時間間隔，在這段時間之後，資料庫頁面快取中的頁面會被視為已遺失頁面存取權，目的是考慮頁面的實用性。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  1 –2147483647</p>
<p><strong>Windows Vista：</strong>   1-4294967295</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>No</p></td>
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


*JET_paramLRUKTrxCorrInterval*  
29  

此參數已過時，且不會影響資料庫引擎的操作。

*JET_paramStartFlushThreshold*  
31  

此參數會控制當資料庫頁面快取開始從快取收回頁面，以騰出空間給未快取的頁面時。 當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。 此臨界值一律相對於 **JET_paramCacheSizeMax** 所設定的最大快取大小。 此臨界值也必須小於 **JET_paramStopFlushThreshold** 所設定的停止閾值。

開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。 高啟動臨界值可讓背景進程更有時間回應。 不過，高啟動閾值表示較高的停止閾值，而且會減少修改過的頁面的資料庫頁面快取大小 (Windows 2000) 或 (Windows XP 及更新版本) 的所有頁面。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  5 (1% ) </p>
<p><strong>Windows Vista：</strong>  20000000 (1% ) </p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  1 –1048575</p>
<p><strong>WINDOWS XP：</strong>  1-4294967295</p>
<p><strong>Windows Vista：</strong>  所有值</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
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
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramStopFlushThreshold*  
32  

此參數會控制資料庫頁面快取何時結束從快取收回頁面，以騰出空間給未快取的頁面。 當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。 此臨界值一律相對於 **JET_paramCacheSizeMax** 所設定的最大快取大小。 此臨界值也必須大於 **JET_paramStartFlushThreshold** 所設定的 [開始] 閾值。

開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。 較大的間距將可讓您更有可能合併對相鄰頁面的寫入。 不過，高停止閾值會減少修改過的頁面的資料庫頁面快取大小 (Windows 2000) 或 (Windows XP 及更新版本) 的所有頁面。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  10 (2% ) </p>
<p><strong>Windows Vista：</strong>  40000000 (2% ) </p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  1 –1048575</p>
<p><strong>WINDOWS XP：</strong>  1-4294967295</p>
<p><strong>Windows Vista：</strong>  所有值</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
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
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>規格需求

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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
