---
title: 拖曳來源責任
description: 拖曳來源責任
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106978585"
---
# <a name="drag-source-responsibilities"></a>拖曳來源責任

拖曳來源負責下列工作：

-   針對公開 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 介面的放置目標提供資料傳輸物件。
-   正在產生指標和來源意見反應。
-   判斷何時取消拖曳作業或發生卸載作業。
-   針對卸載作業所造成的原始資料執行任何動作，例如刪除資料或建立其連結。

主要工作是建立可公開 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 介面的資料傳輸物件。 拖曳來源可能包含或可能不包含所選資料的複本。 包括它並非強制性的，但這麼做可協助防止意外的變更，並允許剪貼簿作業程式碼與拖放程式碼相同。

當拖曳作業正在進行時，拖曳來源會負責設定滑鼠指標，並在適當的情況下，為使用者提供其他來源意見反應。 拖曳來源無法提供任何追蹤滑鼠位置的意見反應，而不是實際設定實際指標 (查看 [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) 函數) 。 必須強制執行此規則，以避免與放置目標所提供的意見反應衝突。  (拖曳來源也可以是放置目標。 在卸載本身時，來源/目標當然可以提供目標意見反應來追蹤滑鼠的位置。 不過，在這種情況下，它是追蹤滑鼠，而不是來源的放置目標。 ) 根據放置目標所提供的意見反應，來源會設定適當的指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[拖放功能](drag-and-drop.md)
</dt> </dl>

 

 