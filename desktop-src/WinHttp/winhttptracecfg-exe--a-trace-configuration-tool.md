---
description: Microsoft Windows HTTP 服務 (WinHTTP) 追蹤設定工具 WinHttpTraceCfg.exe，可用來設定用於偵測和封包探查用途的追蹤功能。
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe，追蹤設定工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e292373c0da19be32f48d7f62f558953406e8d1b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622564"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe，追蹤設定工具

[Microsoft Windows HTTP 服務 (WinHTTP) ](about-winhttp.md)追蹤設定工具 WinHttpTraceCfg.exe，可用來設定用於偵測和封包探查用途的追蹤功能。 監視 WinHTTP 函式和其對應網路流量的能力很重要。 將使用加密網路通訊協定的應用程式（例如安全通訊端層 (SSL) ）偵測到網路傳輸層上的探查封包，並在用戶端與伺服器解密之後，需要能夠攔截流量。 Microsoft Windows HTTP Services (WinHTTP) 提供的追蹤設備，有一系列的功能可攔截用戶端與伺服器之間的流量串流。

此追蹤工具可以是很重要的偵錯工具。 例如，您可以使用它來查看傳遞給各種函式呼叫的參數，以及查看 WinHTTP 應用程式傳送和接收的實際資料。

-   [使用追蹤設備](#using-the-trace-facility)
-   [解讀追蹤資料](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>使用追蹤設備

WinHTTP 從登錄取得追蹤控制參數。 這些控制項參數會影響 WinHTTP 產生追蹤輸出的方式，以及該輸出的格式化方式。 使用 WinHTTP 的所有應用程式都會共用相同的設定。

WinHttpTraceCfg.exe 的追蹤設備設定工具，可從[Windows Server 2003 資源套件工具](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd)網站下載。 Configuration tool 會根據指定的命令列參數，設定或抓取追蹤設備登錄設定。

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

下表列出設定工具的可能參數。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>顯示語法資料。<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>指定是否啟用或停用追蹤工具。 <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>預設值， 停用追蹤。</td>
</tr>
<tr class="even">
<td>1</td>
<td>啟用追蹤。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>指定記錄檔的前置詞。 前置詞可以包含路徑。 記錄檔會寫入至目前的目錄或前置詞中指定的目錄，並具有下列格式。</p>
<p><<em>前置詞</em> > -<<em>應用程式名稱</em> > 。<<em>時間</em> > .log</p>
<p>如果未指定前置詞，則會使用空字串。 指定 &quot; * &quot; 以刪除現有的前置詞。</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>指定追蹤輸出是否顯示在偵錯工具中，或寫入檔案。</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>預設值， 寫入至記錄檔。</td>
</tr>
<tr class="even">
<td>1</td>
<td>在偵錯工具中顯示。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>指定如何) 顯示網路流量 (要求和回應。</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>只顯示 HTTP 標頭。</td>
</tr>
<tr class="even">
<td>1</td>
<td>預設值， 顯示美國國家標準局 (ANSI) 格式的網路流量。</td>
</tr>
<tr class="odd">
<td>2</td>
<td>以十六進位格式顯示網路流量。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-t</td>
<td><p>指定追蹤中是否記錄最上層函式呼叫。</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>預設值， 不會記錄函式呼叫。</td>
</tr>
<tr class="even">
<td>1</td>
<td>最上層函式呼叫會被記錄下來。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>指定追蹤設備所產生之記錄檔的大小上限（以位元組為單位）。 如果指定這個選項但未指定大小，則最小值為65535個位元組。 如果記錄檔達到大小上限，則會清除檔案的內容。 追蹤資料會繼續寫入至記錄檔。</p></td>
</tr>
</tbody>
</table>



 

執行追蹤設備設定工具並不指定參數，會抓取並顯示目前的登錄設定。

> [!Note]  
> 記錄檔會快速成長並降低應用程式效能。 啟用追蹤設備之前，請確定所需的硬碟空間可用。

 

## <a name="interpreting-trace-data"></a>解讀追蹤資料

追蹤設備資料流程會反映在應用程式中呼叫的 WinHTTP 函式，以及任何傳送或接收的 HTTP 資料。 在某些情況下，也會顯示 WinHTTP 內部呼叫的函式。

下圖顯示追蹤設備所產生的記錄檔部分。 已反白顯示並標示了數個專案。

![範例追蹤](images/ss-tracer-wco.png)

追蹤輸出的每一行都包含三個數據行中的資訊。 第一個資料行顯示記錄專案的日期和時間。 第二個數據行會顯示 (識別碼) 的要求識別碼，可以用來區別多個要求。 如果記錄專案未對應至特定的要求， \* \* 則會在此資料行中顯示「會話」。 根據此識別碼排序記錄檔，以只查看針對單一要求所發生的事件，可能會很有用。 下列範例顯示您可以用來排序記錄檔的命令。

**findstr 00000001 LogFile 記錄檔**

第三個數據行會顯示函式呼叫、HTTP 流量或包含的狀態訊息，以協助解讀追蹤。

當記錄專案對應至函式呼叫時，也會記錄函數的參數。 記憶體位址會以十六進位顯示，其他所有值則顯示為 ASCII 字串。 追蹤設備也會記錄每個函數的傳回時間和值。

HTTP 資料的格式取決於使用追蹤設備設定工具指定的登錄設定。 加密 HTTP 資料時，解密的資料也會顯示在追蹤輸出中。

 

 




