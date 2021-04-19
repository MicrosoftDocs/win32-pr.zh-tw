---
description: 在呼叫端內容中強制啟用
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: 在呼叫端內容中強制啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991797"
---
# <a name="enforcing-activation-in-the-callers-context"></a>在呼叫端的內容中強制啟用

您可以控制物件是否會在其本身的內容中啟用。 當您使用 [元件服務] 系統管理工具要求在呼叫端的內容中啟用元件時，當 COM + 在內容中啟動元件的實例時，會發生下列情況：

-   如果可能的話，會在建立者的內容中啟用物件。
-   如果物件需要自己的內容，則物件啟用會失敗;\_ \_ \_ \_ \_ \_ 會傳回建立外部用戶端 \_ 內容的共同電子嘗試。

物件是否需要自己的內容，取決於其設定是否相對於呼叫端內容屬性的目前狀態。 如需詳細資訊，請參閱 [Com +](com--contexts.md)內容。

如果物件有自己的內容，您會想要在該層級上控制啟用的程度。 例如，如果元件不支援封送處理，而它有自己的內容，則對其進行的任何呼叫都將會失敗，因為跨內容呼叫會被攔截並執行輕量封送處理。

**若要在呼叫端的內容中強制啟用**

1.  在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠右鍵按一下元件 (位於任何選取的 COM + 應用) 程式的 [ **元件** ] 資料夾中（您要在其中設定啟用屬性），然後按一下 [ **屬性**]。

2.  在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。

3.  選取 [ **必須在呼叫端內容中啟用** ] 核取方塊。

4.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用概念](com--just-in-time-activation-concepts.md)
</dt> <dt>

[在預設內容中強制啟用](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



