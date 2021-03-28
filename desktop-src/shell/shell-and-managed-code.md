---
description: 內含式擴充功能會載入至任何觸發它們的進程。
title: 執行擴充功能的指引 In-Process
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945357"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>執行擴充功能的指引 In-Process

內含式擴充功能會載入至任何觸發它們的進程。 例如，Shell 命名空間延伸模組可以載入至任何進程，以直接或間接方式存取 Shell 命名空間。 Shell 的命名空間是由許多 Shell 作業所使用，例如顯示一般檔案對話方塊、透過其相關聯的應用程式開機檔案，或取得用來表示檔案的圖示。 因為同進程擴充功能可以載入至任意進程，所以必須小心，因為它們不會對主應用程式或其他內含式擴充造成負面影響。

其中一個特定的執行時間是 *common language runtime (CLR)*，也稱為 *managed 程式碼* 或 *.NET Framework*。 **Microsoft 建議您不要將 managed 內含式擴充功能寫入 Windows 檔案總管或 Windows Internet Explorer，也不會將它們視為支援的案例。**

本主題討論當您判斷 CLR 以外的任何執行時間是否適合用於同進程延伸模組時，所要考慮的因素。 其他執行時間的範例包括 JAVA、Visual Basic、JavaScript/ECMAScript、Delphi 和 C/c + + 執行時間程式庫。 本主題也提供一些原因，也就是 managed 程式碼在同進程延伸中不受支援。

## <a name="version-conflicts"></a>版本衝突

當執行時間不支援在單一進程中載入多個執行階段版本時，可能會發生版本衝突。 4.0 版之前的 CLR 版本屬於這個類別。 如果載入某個執行時間版本時，無法載入該相同執行時間的其他版本，這可能會在主應用程式或其他內含式擴充功能使用衝突的版本時產生衝突。 如果版本與另一個同進程延伸模組發生衝突，衝突可能很難重現，因為失敗需要正確的衝突擴充功能，而失敗模式則取決於載入衝突擴充功能的順序。

請考慮使用4.0 版之前的 CLR 版本所撰寫的同進程擴充功能。 電腦上使用 [ **開啟** 檔案] 對話方塊的每個應用程式，都可能會將對話的 managed 程式碼和其在應用程式中載入的「應用程式」相依性載入至應用程式的進程。 第一次將 CLR 的4.0 版載入至應用程式進程的應用程式或擴充功能，會限制該程式之後可以使用的 CLR 版本。 如果具有 **開啟** 對話方塊的 managed 應用程式是以衝突的 CLR 版本為基礎，則擴充功能可能無法正確執行，而且可能會導致應用程式失敗。 相反地，如果延伸模組是在進程中載入的第一個，而且 managed 程式碼的衝突版本會在該 (可能是 managed 應用程式或執行中的應用程式在需要時載入 CLR) ，則作業會失敗。 對使用者而言，應用程式的某些功能會隨機停止運作，或應用程式莫名其妙損毀。

請注意，等於或晚于4.0 版的 CLR 版本，通常不容易受到版本控制問題的影響，因為它們是設計成與彼此並存，並且具有大部分的 CLR 1.0 (的最高4.0 版，但不能與其他版本) 並存。 不過，可能會發生版本衝突以外的問題，如本主題的其餘部分所述。

## <a name="performance-issues"></a>效能問題

當執行時間將效能問題載入處理常式時，可能會對效能產生重大影響。 效能下降的形式可能是記憶體使用量、CPU 使用量、經過時間，甚至是位址空間耗用量。 CLR、JavaScript/ECMAScript 和 JAVA 已知為高度影響執行時間。 由於同進程擴充功能可以載入至許多進程，而且通常會在效能緊迫的時刻進行 (例如，當您準備要顯示使用者) 的功能表時，強烈影響的執行時間可能會對整體回應性造成負面影響。

耗用大量資源的高影響執行時間可能會導致主機進程或另一個同進程延伸模組失敗。 例如，對其堆積取用數百 mb 位址空間的高度影響執行時間，可能會導致主機應用程式無法載入大型資料集。 此外，因為同進程擴充功能可以載入至多個進程，所以單一延伸模組中的高資源耗用量，可以快速地在整個系統中使用高資源耗用量。

如果執行時間仍處於載入狀態，或即使在使用該執行時間的延伸模組已卸載時仍繼續取用資源，則該執行時間不適合在擴充功能中使用。

## <a name="issues-specific-to-the-net-framework"></a>.NET Framework 的特定問題

下列各節將討論使用 managed 程式碼延伸模組時發現的問題範例。 它們並不是您可能會遇到的所有可能問題的完整清單。 此處所討論的問題都是延伸模組中不支援 managed 程式碼的原因，以及當您評估其他執行時間的使用時，要考慮的重點。

### <a name="re-entrancy"></a>重新進入

當 CLR 封鎖單一執行緒的單元 (STA) 執行緒時（例如，由於監視器）。 Enter、WaitHandle. WaitOne 或爭用 [**lock**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) 語句，CLR 在其標準設定中，會在等候時進入嵌套的訊息迴圈。 有許多擴充方法都禁止處理訊息，而這種無法預期且未預期的重新進入，可能會造成異常行為，而難以重現和診斷。

### <a name="the-multithreaded-apartment"></a>多執行緒單元

CLR 會為元件物件模型 (COM) 物件建立執行時間可呼叫的 *包裝* 函式。 這些相同的執行時間可呼叫包裝函式稍後會由 CLR 的完成項（屬於多執行緒單元 (MTA) 的一部分）終結。 將 proxy 從 STA 移至 MTA 需要封送處理，但不會封送處理擴充功能使用的所有介面。

### <a name="non-deterministic-object-lifetimes"></a>不具決定性的物件存留期

CLR 比原生程式碼的物件存留期保證更弱。 許多延伸模組都有物件和介面的參考計數需求，而 CLR 所採用的垃圾收集模型無法滿足這些需求。

-   如果 CLR 物件取得 COM 物件的參考，就不會釋放執行時間可呼叫包裝函式所持有的 COM 物件參考，直到執行時間可呼叫包裝函式進行垃圾收集為止。 非決定性的發行行為可能會與某些介面合約發生衝突。 例如， [**IPersistPropertyBag：： Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) 方法要求當 **Load** 方法傳回時，物件不會保留屬性包的參考。
-   如果 CLR 物件參考傳回機器碼，則執行時間可呼叫包裝函式會在呼叫運行 [**時間可呼叫**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 包裝函式的最後呼叫時，會讓出其 clr 物件的參考，但基礎 CLR 物件在進行垃圾收集之前不會完成。 不具決定性的最終可能會與某些介面合約發生衝突。 例如，縮圖處理常式必須在其參考計數降至零時立即釋出所有資源。

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>受控碼和其他執行時間的可接受用法

使用 managed 程式碼和其他執行時間來執行跨進程擴充是可接受的。 跨進程 Shell 延伸模組的範例包括下列各項：

-   預覽處理常式
-   命令列型動作，例如在 **shell** \\ *動詞* \\ **命令** 子機碼下註冊的動作。
-   在本機伺服器中執行的 COM 物件，適用于允許跨進程啟用的 Shell 擴充點。

有些擴充功能可以實作為同進程或跨進程的延伸模組。 如果這些擴充功能不符合這些內含式擴充功能的需求，您可以將這些擴充功能實作為跨進程擴充。 下列清單顯示可實作為同進程或跨進程擴充的延伸模組範例：

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand)與在 **shell**  \\ *動詞* \\ **命令** 子機碼下註冊的 DelegateExecute 專案相關聯。
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)與在 **shell** \\ *動詞* \\ **DropTarget** 子機碼下註冊的 CLSID 相關聯。
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate)與在 **shell** 動詞子機碼下註冊的 **CommandStateHandler** 專案相關聯 \\  。

 

 
