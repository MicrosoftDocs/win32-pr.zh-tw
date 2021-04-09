---
description: 深入瞭解：資料庫參數
title: 資料庫參數
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114084"
---
# <a name="database-parameters"></a>資料庫參數


_**適用于：** Windows |Windows Server_

## <a name="database-parameters"></a>資料庫參數

本主題包含用於資料庫的參數。

*JET_paramCheckFormatWhenOpenFail*  
44  

設定時，此參數會在開啟資料庫引擎的資料庫或交易記錄檔時，導致 [JetInit](./jetinit-function.md) 傳回特殊錯誤。 這些錯誤包括：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>錯誤</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>資料庫和/或交易記錄檔是使用 database engine 在 Windows NT 3.51 中建立的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>資料庫和/或交易記錄檔是使用 database engine 在 Windows NT Server 4.0 之前的測試版本中建立的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>資料庫和/或交易記錄檔是使用 Windows NT Server 4.0 中的 database engine 所建立。</p></td>
</tr>
</tbody>
</table>


**Windows Vista：**  若為 Windows Vista 和更新版本，此參數已過時，而且不會影響資料庫引擎的操作。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>對</p></td>
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


*JET_paramDatabasePageSize*  
64  

此參數會設定資料庫的頁面大小。 頁面大小是資料庫檔案可能的最小空間配置單位。 資料庫頁面大小也非常重要，因為它會在資料庫中設定個別記錄大小的上限。

**注意** 目前每個進程只支援一個資料庫頁面大小。 這表示，如果您在包含使用資料庫引擎之不同應用程式的單一進程中，則它們都必須同意資料庫頁面大小。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>2048、4096、8192</p></td>
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
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramDbExtensionSize*  
18  

此參數會控制每次需要成長以容納更多資料時，資料庫檔案所新增的空間量。 大小是在資料庫頁面中。

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
<td><p>1–2147483647</p></td>
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
<td><p>No</p>
<p><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</p></td>
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


*JET_paramEnableIndexChecking*  
45  

當此參數為 true 時，系統會在 [JetAttachDatabase](./jetattachdatabase-function.md) 階段檢查每個資料庫，以取得在作業系統中使用舊版 NLS 程式庫建立的 Unicode 索引鍵資料行的索引。 這必須完成，因為資料庫引擎會保存 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 所產生的排序索引鍵，而這些排序索引鍵的值會從 release 變更為 release。

如果偵測到主要索引處於此狀態，則 [JetAttachDatabase](./jetattachdatabase-function.md) 一律會失敗，並 JET_errPrimaryIndexCorrupted。

如果偵測到任何次要索引處於此狀態，則有兩個可能的結果。 如果 JET_bitDbDeleteCorruptIndexes 已傳遞至 [JetAttachDatabase](./jetattachdatabase-function.md) ，則這些索引將會刪除，而且 JET_wrnCorruptIndexDeleted 將會從 [JetAttachDatabase](./jetattachdatabase-function.md)傳回。 您的應用程式將需要重新建立這些索引。 如果 JET_bitDbDeleteCorruptIndexes 未傳遞至 [JetAttachDatabase](./jetattachdatabase-function.md) ，則呼叫會失敗併發生 JET_errSecondaryIndexCorrupted。

**注意** 強烈建議您的應用程式將此參數設定為 True。

**注意** 強烈建議應用程式避免在 (叢集) 索引的主鍵中使用 Unicode 索引鍵資料行。

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
<td><p>全球</p>
<p><strong>Windows Vista：</strong>  Windows Vista 和更新版本：實例</p></td>
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


*JET_paramEnableIndexCleanup*  
54  

當這個參數設定為 true 時，資料庫引擎會視需要在 [JetInit](./jetinit-function.md) 時自動清除 Unicode 索引鍵資料行上的索引，以避免變更 WINDOWS 中 NLS 程式庫所造成的資料庫格式變更。 NLS 程式庫會定期進行這類變更，以新增對新語言的支援、將遺漏的字元新增至語言、將定序順序加入至語言，或是以語言的定序順序修正 bug。 這些變更會影響由資料庫引擎以索引鍵的元件的形式保存的 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 所產生的排序關鍵字。

很重要的一點是，索引的變更可能很有可能無法進行累加式清除。 在此情況下，會依 **JET_paramEnableIndexChecking** 的規定來處理索引。

**注意** 強烈建議您的應用程式將此參數和 **JET_paramEnableIndexChecking** 設定為 **True** 。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>對</p></td>
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
<td><p>No</p>
<p><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows Server 2003 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

當此參數為 true 時，指定會話一次只允許一個資料庫使用 [JetOpenDatabase](./jetopendatabase-function.md) 來開啟。 這項限制會排除暫存資料庫。

**WINDOWS XP 和 Windows Server 2003：**  此參數只會在 Windows XP 和 Windows Server 2003 上寫入。

**Windows Vista：**  此參數的行為通常是 Windows Vista。

**注意**  此參數只是寫入。

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
<td><p>No</p>
<p><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableOnlineDefrag*  
35  

此參數會控制使用 [JetDefragment](./jetdefragment-function.md)起始時的線上磁碟重組行為。 如需詳細資訊，請參閱 [JetDefragment](./jetdefragment-function.md) 。

Windows 2000：在 Windows 2000 上，此參數是簡單的布林值，會在 [JetDefragment](./jetdefragment-function.md)啟動時閘道進行線上磁碟重組。 當設為 **TRUE** 時，會對資料庫中每個資料表的記錄執行線上磁碟重組。

**WINDOWS XP：**  在 Windows XP 和更新版本中，這個參數可以設定為下列其中一個或多個選項：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>選項</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>請勿執行線上磁碟重組。 這是與此參數的 Windows 2000 設定為 False 相等的二進位檔。</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>執行完整的線上磁碟重組。 這是對此參數而言，與 Windows 2000 設定為 True 的二進位檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>針對資料庫中每個資料表的記錄執行線上磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>針對資料庫中每個資料表的空間樹狀目錄執行線上磁碟重組。</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>這個參數是用來支援 Microsoft Exchange 基礎結構，而且不適合在您的應用程式中使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>執行完整的線上磁碟重組。 這個參數的概念相當於 Windows 2000 設定 True。</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p><strong>Windows 2000：</strong>  真</p>
<p><strong>WINDOWS xp：適用于 WINDOWS xp 和更新版本：</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p><strong>Windows 2000：</strong>  布林</p>
<p><strong>WINDOWS XP 和更新版本：</strong>  JET_GRBIT (整數) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000：</strong>  False、True</p>
<p><strong>WINDOWS XP 及更新版本：</strong>  0 – JET_OnlineDefragAll</p></td>
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


*JET_paramPageFragment*  
20  

此參數是資料庫引擎用來控制可用空間片段的臨界值。 大小是在資料庫頁面中。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>8</p></td>
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
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramRecordUpgradeDirtyLevel*  
78

此參數會控制資料庫頁面快取管理員撰寫資料庫頁面，而該頁面已經歷就地格式轉換的程度。 這些格式轉換會在頁面從使用 Windows 2000 資料庫引擎建立的資料庫載入，但是由 Windows XP 或更新版本的 database engine 所使用，而立即進行。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-3</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

) 記錄中的延遲 (于提示/最高認可記錄檔後方，以延遲資料庫頁面排清。 啟用此延遲可能會在最新的記錄檔發生嚴重遺失時，允許資料庫復原。 請參閱 JET_bitReplayIgnoreLostLogs。

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
<td><p>0-1023</p></td>
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
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

開啟/關閉自動連續的 B 型樹狀目錄磁碟重組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-1</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

決定選取 B 型樹狀結構密度的頻率。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-最大整數</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

I/o 節流機制提供工作執行的最長時間（以毫秒為單位），以視為「已完成」。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-10000</p></td>
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
<td><p>Windows 7</p></td>
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

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
