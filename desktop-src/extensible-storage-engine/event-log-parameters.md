---
description: 深入瞭解：事件記錄檔參數
title: 事件記錄檔參數
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026931"
---
# <a name="event-log-parameters"></a>事件記錄檔參數


_**適用于：** Windows |Windows Server_

## <a name="event-log-parameters"></a>事件記錄檔參數

本主題包含事件記錄檔所使用的參數。

JET_paramEventLogCache  
此參數會控制記錄檔訊息快取的大小 () （以位元組為單位），此訊息會保存資料庫引擎在 eventlog 服務停止時發出的 eventlog 訊息。 當服務變成可運作時，這些快取的訊息將會清除到 eventlog。 將會捨棄任何溢位的快取訊息。

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


*JET_paramEventLoggingLevel*  
  
此參數會設定資料庫引擎發出給 eventlog 的 eventlog 訊息詳細層級。 較高的數位將會產生更詳細的事件記錄檔訊息。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>JET_EventLoggingLevelMax</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p></td>
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
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramEventSource*  
4  

此參數會提供應用程式特定的字串，該字串將會新增至 database engine 發出的任何事件記錄檔訊息。 這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。 如果指定了空字串 (預設) 則會使用主應用程式的可執行檔名稱。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;&quot;</p></td>
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


*JET_paramEventSourceKey*  
49  

這個參數可以用來控制 database engine 針對其事件記錄檔訊息所使用的事件記錄檔。 依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。 如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;&quot;</p></td>
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


*JET_paramNoInformationEvent*  
50  

當此參數為 true 時，將會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。

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
