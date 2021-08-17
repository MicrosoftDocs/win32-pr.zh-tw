---
description: 排程器會為每個優先權層級維護可執行執行緒的佇列。
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: 環境切換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c15f5d762525fd4a80030ea10e128e2c30a1ab914e9f17d0f954d80ecfd2e204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143131"
---
# <a name="context-switches"></a>環境切換

排程器會為每個優先權層級維護可執行執行緒的佇列。 這些稱為就緒的 *執行緒*。 當處理器變成可用時，系統會執行 *內容切換*。 內容切換中的步驟如下：

1.  儲存剛剛完成執行之執行緒的內容。
2.  將剛剛完成執行的執行緒放在佇列的結尾，以瞭解其優先順序。
3.  尋找包含就緒執行緒的最高優先順序佇列。
4.  移除佇列開頭的執行緒、載入其內容，然後執行它。

下列執行緒類別並非就緒的執行緒。

-   使用 CREATE 擱置旗標建立的執行緒 \_
-   使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 或 [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) 函式執行期間停止的執行緒
-   等候同步處理物件或輸入的執行緒。

在暫停或封鎖的執行緒準備好執行之前，排程器不會將任何處理器時間配置給它們，無論其優先順序為何。

內容切換的最常見原因如下：

-   時間配量已過。
-   具有較高優先順序的執行緒已準備好執行。
-   執行中的執行緒需要等候。

當執行中的執行緒需要等候時，它會會讓出其時間配量的其餘部分。

 

 
