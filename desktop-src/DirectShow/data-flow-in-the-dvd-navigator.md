---
description: DVD 導覽器中的資料流程
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: DVD 導覽器中的資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688391"
---
# <a name="data-flow-in-the-dvd-navigator"></a>DVD 導覽器中的資料流程

DVD 導覽器有停止和暫停播放的方法。 這些方法與 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)中的 **Stop** 和 **Pause** 方法類似（但不完全相同）。 兩者之間的差異如下：

-   **IDvdControl2** 方法會變更 DVD 導覽器從磁片讀取的內容。 它們不會變更圖形的狀態。
-   **IMediaControl** 方法會變更圖形的狀態。 它們不會變更 DVD 導覽器從磁片讀取的內容。  (下一節中說明的一個重要例外狀況，與 **Stop** 方法相關。 ) 

例如， [**IDvdControl2：:P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) 方法會發出附錄 J "Pause \_ On" 命令，但不會暫停篩選圖形。 另一方面， [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) 方法會暫停圖形，但不會發出任何 DVD 命令。

一般情況下，請使用 **IMediaControl：:P ause** 和 **Stop** 方法，而不是對應的 **IDvdControl2** 方法。 **IMediaControl** 方法有極小的延遲，而 **IDvdControl2** 方法的延遲最多可達二秒。

停止播放

[**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)的行為取決於您可以使用 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)方法設定的旗標。

-   如果 DVD \_ ResetOnStop 旗標為 **FALSE**， **IMediaControl：： Stop** 會停止圖形，但不會變更 DVD Navigator 的網域。 當您再次呼叫 [執行] 時，會從目前的位置繼續播放。
-   如果 DVD \_ ResetOnStop 為 **TRUE**， **IMediaControl：： Stop** 會導致 dvd Navigator 重設。 當您再次呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 時，Dvd 導覽器會從第一個 Play 網域播放，如同您第一次插入 dvd 一樣。

DVD \_ ResetOnStop 旗標預設為 **TRUE** ，以與繼承應用程式相容。 不過，一般而言，您應該覆寫預設值，並將旗標設為 **FALSE**。 原因是某些事件可能會導致圖形在播放期間停止。 例如，如果顯示解析度變更，則篩選圖形會停止，重新連接影片轉譯器並重新啟動。 如果 DVD \_ ResetOnStop 為 **TRUE**，播放將會從光碟的開頭重新開機。這可能不是使用者預期的。

因此，在您的應用程式開始時，將 DVD ResetOnStop 的 **SetOption** 呼叫 \_ 設為 **FALSE**。 如果您想要停止播放，並讓它從相同的位置繼續，請呼叫 **IMediaControl：： stop** 或 **IMediaControl：:P ause**。 如果您想要停止播放和重設磁片，請呼叫具有等於 TRUE 之 DVD ResetOnStop 的 **setoption** \_ ; 然後呼叫 **IMediaControl：： stop**; 最後，再次呼叫 **setoption** ，然後將 DVD ResetOnStop 重設 \_ 為 **FALSE**。

暫停播放

如果您在圖形暫停時提供 DVD 導覽器命令，則在圖形再次執行之前，命令可能無法完成。 在某些情況下，這可能會在您的應用程式中造成鎖死。 您應該遵循兩個規則來避免鎖死：

-   暫停時，請勿發出一個以上的非同步 DVD 命令。
-   暫停時，不會封鎖應用程式的 UI 執行緒或變更圖形狀態的執行緒。

第二個規則值得詳細檢查。 以下是一些可能會造成鎖死的特定案例：

-   **案例**：在暫停的情況下，應用程式會發出具有封鎖旗標的 DVD 命令。 如果發出 DVD 命令的執行緒是發出執行命令的相同執行緒，這可能會導致鎖死。 DVD 命令會封鎖，直到圖形執行為止，但在命令完成之前，圖形無法執行。

    **建議**：在個別的背景工作執行緒上發出 DVD 命令，或不要使用封鎖旗標。

-   **案例**：在暫停的情況下，應用程式會發出 DVD 命令，然後在命令物件上呼叫 [**IDvdCmd：： WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) 。 這種情況相當於先前的範例。 如果您從 UI 執行緒呼叫 **wait** ，ui 執行緒將無法執行圖形，直到 **等候** 方法解除封鎖為止，但 **等候** 方法將不會解除封鎖，直到圖形執行為止。

    **建議**：在背景工作執行緒上呼叫 **Wait** 。

-   **案例**：當圖形正在執行時，應用程式會以封鎖旗標發出 DVD 命令，然後呼叫另一個執行緒的暫停。 這是可能的競爭情形，因為圖形可能會在發出命令之前暫停。 如果這兩個執行緒中的一個執行緒是 UI 執行緒，您可能會造成類似先前兩個範例的鎖死。 此範例說明如果您的應用程式使用多個執行緒，撰寫安全線程程式碼的重要性。

    **建議**：如果您使用背景工作執行緒，請確定您的程式碼為安全線程。

-   **案例**：在暫停的情況下，應用程式會停用 UI 中的 run 命令，然後發出非同步 DVD 命令。 由於應用程式執行緒仍在執行中，因此這種情況並不會嚴格地產生鎖死。 不過，使用者現在無法執行圖形，因此命令將永遠不會完成。

    **建議**：暫停時，一律讓 run 命令保持啟用狀態。

將 DVD 搜尋到指定的時間

若要精確地搜尋光碟上的指定時間，請呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)。 然後呼叫 [**IDvdControl2：:P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)，指定時間，並將 *DWFLAGS* 設定為 DVD CMD 旗標排清 \_ \_ \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



