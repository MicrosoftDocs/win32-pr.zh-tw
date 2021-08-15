---
description: 執行緒已排程為根據其排程優先權執行。
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: 排程優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793310"
---
# <a name="scheduling-priorities"></a>排程優先順序

執行緒已排程為根據其 *排程優先權* 執行。 每個執行緒都會指派排程優先權。 優先權層級的範圍從零 (最低優先順序) 到 31 (最高優先順序) 。 只有零頁執行緒的優先順序可以是零。  (零頁執行緒是系統執行緒，負責在沒有其他需要執行的執行緒時，將任何可用的頁面清空。 ) 

系統會將具有相同優先權的所有線程視為相等。 系統會以迴圈配置資源的方式，將時間配量指派給優先順序最高的所有線程。 如果這些執行緒都未準備好執行，系統會以迴圈配置資源的方式，將時間配量指派給下一個最高優先順序的所有線程。 如果有較高優先順序的執行緒可供執行，系統就會停止執行較低優先順序的執行緒 (而不允許它使用時間配量) 完成，並將完整的時間配量指派給較高優先順序的執行緒。 如需詳細資訊，請參閱 [內容切換](context-switches.md)。

每個執行緒的優先順序取決於下列準則：

-   其進程的 priority 類別
-   執行緒在其進程的 priority 類別中的優先權層級

優先順序類別和優先權層級會合並以形成執行緒的 *基本優先權* 。 如需執行緒動態優先權的詳細資訊，請參閱 [優先權提升](priority-boosts.md)。

## <a name="priority-class"></a>Priority 類別

每個進程都屬於下列其中一個優先順序類別：<dl> 閒置 \_ 優先權 \_ 類別  
低於 \_ 一般 \_ 優先順序 \_ 類別  
一般 \_ 優先順序 \_ 類別  
高於 \_ 一般 \_ 優先順序 \_ 類別  
高 \_ 優先順序 \_ 類別  
即時 \_ 優先權 \_ 類別  
</dl>

依預設，進程的 priority 類別為一般 \_ 優先順序 \_ 類別。 當您建立子進程時，請使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數來指定子進程的優先權類別。 如果呼叫進程是閒置 \_ 優先權 \_ 類別或低於 \_ 一般 \_ 優先順序 \_ 類別，則新的進程會繼承這個類別。 您可以使用 [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) 函數來判斷進程的目前優先權類別，並使用 [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) 函數來變更進程的 priority 類別。

監視系統的進程（例如，會定期更新顯示器的螢幕保護裝置或應用程式）應該使用「閒置 \_ 優先順序」 \_ 類別。 這可防止此進程的執行緒（沒有高優先順序）干擾較高優先順序的執行緒。

請小心使用高 \_ 優先順序 \_ 類別。 如果執行緒在較高的優先權層級執行了較長的時間，則系統中的其他執行緒將不會取得處理器時間。 如果有多個執行緒同時設定為高優先順序，執行緒就會失去其有效性。 高優先順序的類別應該保留給必須回應時間關鍵事件的執行緒。 如果您的應用程式執行一個需要高優先順序類別的工作，而其餘的工作都是一般優先順序，請使用 [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) 來暫時引發應用程式的 priority 類別;然後在時間關鍵工作完成後將它減少。 另一種策略是建立高優先順序的程式，讓它的所有線程都封鎖大部分的時間，只有在需要重要工作時才喚醒執行緒。 很重要的一點是，高優先順序的執行緒應該執行一小段時間，而且只有在具有要執行的時間緊迫工作時。

您幾乎不應使用即時 \_ 優先權 \_ 類別，因為這會中斷管理滑鼠輸入、鍵盤輸入和背景磁片排清的系統執行緒。 此類別適用于與硬體直接進行「交談」的應用程式，或執行應該受限中斷的簡單工作。

## <a name="priority-level"></a>優先權層級

以下是每個優先權類別內的優先權層級：<dl> 執行緒 \_ 優先順序 \_ 閒置  
執行緒 \_ 優先順序 \_ 最低  
一般的執行緒 \_ 優先順序 \_ \_  
執行緒 \_ 優先順序 \_ 正常  
\_ \_ 高於 \_ 一般的執行緒優先順序  
執行緒 \_ 優先順序 \_ 最高  
執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足  
</dl>

所有線程都是使用執行緒 \_ 優先權 \_ NORMAL 來建立。 這表示執行緒優先順序與進程優先權類別相同。 在您建立執行緒之後，請使用 [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) 函數來調整其相對於進程中其他執行緒的優先權。

典型的策略是使用 \_ \_ \_ 處理常式輸入執行緒的一般一般或執行緒優先順序最高的執行緒優先順序 \_ \_ ，以確保應用程式能回應使用者。 背景執行緒（特別是處理器密集的執行緒）可以設定為 \_ \_ 低於 \_ 正常或執行緒優先順序的執行緒 \_ 優先順序 \_ ，以確保它們可以在必要時被佔用。 但是，如果您的執行緒等候另一個具有較低優先順序的執行緒完成一些工作，請務必封鎖等候高優先順序執行緒的執行。 若要這樣做，請使用 [wait](../sync/wait-functions.md)函式、 [重要區段](../sync/critical-section-objects.md)或 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) 函數、 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)或 [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) 函數。 最好是讓執行緒執行迴圈。 否則，進程可能會變成鎖死，因為不會排定優先順序較低的執行緒。

若要判斷線程的目前優先權層級，請使用 [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) 函數。

## <a name="base-priority"></a>基本優先順序

系統會合並進程優先權類別和執行緒優先順序層級，以構成每個執行緒的基本優先權。

下表顯示處理優先權類別和執行緒優先順序值組合的基本優先權。


<table>
<tr>
<th colspan="2">進程優先順序類別</th>
<th>執行緒優先順序層級</th>
<th>基本優先順序</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
