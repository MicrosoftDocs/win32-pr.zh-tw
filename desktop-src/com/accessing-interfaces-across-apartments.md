---
title: 跨單元存取介面
description: 跨單元存取介面
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89e82fa29e768328e6c110349627d32e92ab010ce61fdf64141ad3ca7fe9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048916"
---
# <a name="accessing-interfaces-across-apartments"></a>跨單元存取介面

COM 提供一種方法，讓進程中的任何一個單元都能存取在進程中任何其他單元之物件上所執行的介面。 這是透過 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面完成的。 這個介面有三個方法，可讓您執行下列作業：

-   將介面註冊為 *全域* (processwide) 介面。
-   透過 cookie 從任何其他的單元取得該介面的指標。
-   撤銷介面的全域註冊。

[**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)介面是一個有效率的方法，可讓您將介面指標儲存在記憶體位置，以便從進程內的多個單元存取，例如整個進程的變數和 *agile* 物件 (自由執行緒、封送處理的物件) 包含指向其他物件的介面指標。

Agile 物件不知道其執行所在的基礎 COM 基礎結構;換句話說，它正在執行的是哪一個單元、內容和執行緒。 物件可能會保存在某個單元或內容特定的介面上。 基於這個理由，從 agile 元件執行的任何位置呼叫這些介面，可能不一定會正常運作。 全域介面表會根據 agile 物件執行所在的位置，確保使用有效的 proxy (或指向物件的直接指標) ，藉以避免這個問題。

> [!Note]  
> 全域介面資料表無法跨進程或電腦界限進行移植，因此不能用來取代正常的參數傳遞機制。

 

如需有關建立和使用全域介面表的詳細資訊，請參閱下列主題：

-   [建立全域介面資料表](creating-the-global-interface-table.md)
-   [使用全域介面資料表的時機](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[選擇執行緒模型](choosing-the-threading-model.md)
</dt> <dt>

[多執行緒單元](multithreaded-apartments.md)
</dt> <dt>

[同進程伺服器執行緒問題](in-process-server-threading-issues.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒和多執行緒通訊](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[單一執行緒單元](single-threaded-apartments.md)
</dt> </dl>

 

 




