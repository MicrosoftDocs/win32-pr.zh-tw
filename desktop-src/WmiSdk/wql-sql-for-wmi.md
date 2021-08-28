---
description: WMI 查詢語言 (WQL) 是美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) &郵件的子集， \# 但不含次要語義變更。 下表列出 WQL 關鍵字。
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL for WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e2c80473874390851e81a5f2acebcd6d7e1497
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626754"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL for WMI)

WMI 查詢語言 (WQL) 是美國國家標準局的子集，結構化查詢語言 (SQL) 具有次要語義變更的 (SQL ANSI) 。 下表列出 WQL 關鍵字。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>WQL 關鍵字</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>結合兩個布林運算式，並在兩個運算式都<strong>為 true</strong>時傳回<strong>true</strong> 。<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIATORS OF</a></td>
<td>抓取與來源實例相關聯的所有實例。<br/> 將此語句與架構查詢和資料查詢搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>參考查詢中物件的類別。<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>指定包含 SELECT 語句中所列屬性的類別。 WindowsManagement Instrumentation (WMI) 一次只支援一個類別的資料查詢。<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">GROUP 子句</a></td>
<td>讓 WMI 產生一個通知來表示事件群組。<br/> 使用這個子句搭配事件查詢。<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>篩選在 in <a href="within-clause.md">子句</a>中指定的分組間隔期間所收到的事件。<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>搭配 NOT 和 <strong>Null</strong>使用的比較運算子。 此語句的語法如下：<br/> 是 [NOT] <strong>Null</strong><br/>  (，其中不是選擇性的) <br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>將查詢套用至指定類別之子類別的運算子。 如需詳細資訊，請參閱 <a href="isa-operator-for-event-queries.md">適用于事件查詢的 Isa 操作員</a>、 <a href="isa-operator-for-data-queries.md">資料查詢的 isa 運算子</a>，以及 <a href="isa-operator-for-schema-queries.md">用於架構查詢的 isa 運算子</a>。<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>用於查詢 <a href="references-of-statement.md">的參考</a> 和 <a href="associators-of-statement.md">associators of</a> ，以確保產生的實例只會填入實例的索引鍵，進而減少呼叫的額外負荷。<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>判斷指定的字元字串是否符合指定之模式的運算子。<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>在 WQL SELECT 查詢中使用的比較運算子，例如：<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>指出物件沒有明確指派的值。 <strong>Null</strong> 不等於零 (0) 或空白。<br/></td>
</tr>
<tr class="odd">
<td>OR<br/></td>
<td>結合兩個條件。<br/> 當在語句中使用一個以上的邏輯運算子時，OR 運算子會在 AND 運算子之後評估。<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">的參考</a></td>
<td>抓取參考特定來源實例的所有關聯實例。 將此語句與架構和資料查詢搭配使用。 語句的 <a href="references-of-statement.md">參考</a> 類似于語句的 <a href="associators-of-statement.md">associators of</a> 。 但是，它不會取出端點實例;它會捕獲關聯實例。<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>指定用於查詢的屬性。<br/> 如需詳細資訊，請參閱 <a href="select-statement-for-data-queries.md">資料查詢的 Select 語句</a>、 <a href="select-statement-for-event-queries.md">事件查詢的 select 語句</a>，或 <a href="select-statement-for-schema-queries.md">架構查詢的 select 語句</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>評估為-1 (減一) 的布林運算子。<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>縮小資料、事件或架構查詢的範圍。<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>指定輪詢或分組間隔。<br/> 使用這個子句搭配事件查詢。<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>判斷值為 0 (零) 的布林運算子。</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 使用 WQL 關鍵字字作為物件名稱，可能會導致無法剖析查詢，即使查詢未發生錯誤，也是如此。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WQL 運算子](wql-operators.md)
</dt> <dt>

[WQL-支援的日期格式](wql-supported-date-formats.md)
</dt> <dt>

[WQL-支援的時間格式](wql-supported-time-formats.md)
</dt> </dl>

 

 




