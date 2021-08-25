---
title: 非同步名字
description: 非同步名字
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9e9b5e427df882b7e0be84507b79c9113a46e44dad614e571a831fedecedff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859648"
---
# <a name="asynchronous-monikers"></a>非同步名字

OLE 標記架構提供一致且可延伸的程式設計模型，可使用網際網路物件、提供剖析名稱的方法， (Url) 為可列印的名稱，以及尋找並系結至 URL 字串所表示的物件。  (也會看到 [URL](url-monikers.md)標記) 項。 ) 標準 OLE 標記 (值得注意的是，因為它們是同步的，所以不適合網際網路，因為它們是同步的，因此只有在有所有資料可供使用時，才會傳回物件或其儲存區的指標。 視所要下載的資料量而定，同步系結可讓用戶端的使用者介面長時間進行系結。

網際網路需要新的應用程式設計方法。 應用程式應該能夠以非同步方式執行所有昂貴的網路作業，以避免拖延使用者介面。 應用程式應該能夠觸發作業，並在完整或部分完成時收到通知。 屆時，應用程式應該可以選擇繼續進行作業的下一個步驟，或視需要提供其他資訊。 當您進行下載時，應用程式應該也可以為使用者提供進度資訊，以及隨時取消作業的機會。

非同步標記可提供這些功能以及各種層級的非同步系結行為，同時為不知道或不需要非同步行為的應用程式提供回溯相容性。 另一項 OLE 技術（非同步儲存）可與非同步名字區搭配使用，以提供非同步下載網際網路物件的持續性狀態。 非同步標記會觸發系結作業，並設定必要的元件，包括儲存和資料流程物件、位元組陣列物件和通知接收。 一旦連接元件之後，就會出現此標記，且系結的其餘部分主要是在執行非同步儲存元件和物件的元件之間執行。

如需詳細資訊，請參閱下列主題：

-   [非同步和同步的名字標記](./asynchronous-vs.-synchronous-monikers.md)
-   [非同步和同步系結](./asynchronous-vs.-synchronous-binding.md)
-   [非同步和同步儲存體](./asynchronous-vs.-synchronous-storage.md)
-   [資料提取模型和 Data-Push 模型](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[URL 的名字](url-monikers.md)
</dt> </dl>

 

 