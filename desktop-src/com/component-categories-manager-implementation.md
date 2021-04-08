---
title: 元件類別管理員執行
description: 當可用的元件數目增加時，管理這些元件會變得越來越困難。 就它們公開的介面以及它們所執行的工作而言，許多元件都提供類似的功能。
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932566"
---
# <a name="component-categories-manager-implementation"></a>元件類別管理員執行

當可用的元件數目增加時，管理這些元件會變得越來越困難。 就它們公開的介面以及它們所執行的工作而言，許多元件都提供類似的功能。

通常必須列舉可在特定內容中使用的元件。 例如，OLE 複合檔案中使用的 [ **插入物件** ] 對話方塊，以及用於 ole 控制項的 [ **插入控制項** ] 對話方塊。 這些對話方塊會列出所有符合 (或宣告來滿足複合檔案或控制項之介面合約) 的所有元件。 這些現有的類別 (OLE 檔，OLE 控制項) 不代表確切的介面簽章。 OLE 檔必須公開一組特定的核心介面 (例如 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) 或 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)) 但也可以公開其他介面，例如 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)。

在過去，已標記元件，方法是新增人類可讀取的名稱 ( 「可插入」、「控制項」等等) 作為 **HKEY \_ 類別 \_ 根目錄 \\ CLSID \\ {...}** 的子機碼 對應至元件的登錄機碼。 這適用于類別的集中定義，但在許多獨立的合作物件定義新類別時，會產生風險名稱衝突。 在 COM 的其他區域中，提供可延伸命名空間的解決方案是使用全域唯一識別碼 (Guid) 。 與其使用人類看得懂的名稱， (CATID) 的唯一數目會指派給每個類別。

現有分類的另一項限制是僅限於表示元件本身的功能。 許多元件需要容器的特定功能。 將這類元件插入容器時，插入可能會失敗或非預期的行為，即使元件符合其中一個類別所隱含的合約也一樣。 若要列舉在某些情況下可以成功使用的元件，必須考慮元件和容器的功能。

基於這些考慮，已對現有的分類進行下列變更：

-   類別是使用全域唯一識別碼的 Catid 來表示。
-   在 **HKEY \_ 類別 \_ 根 \\ CLSID** 登錄機碼的 **元件** 子機碼底下，已開發兩個不同的子機碼：「實作為類別」和「必要類別」。 這些子機碼包含元件所提供的 Catid 清單，或元件的容器必須提供的清單。

為了簡化元件類別的管理，類別會列在登錄： **HKEY \_ 類別的 \_ 根 \\ 元件類別** 的集中位置。 此索引鍵會列出已安裝的類別及其 CATID 以及當地語系化、人們看得懂的名稱。

如需詳細資訊，請參閱下列主題：

-   [依元件功能分類](categorizing-by-component-capabilities.md)
-   [依容器功能分類](categorizing-by-container-capabilities.md)
-   [元件類別管理員](the-component-categories-manager.md)
-   [預設類別和關聯](default-classes-and-associations.md)
-   [定義元件類別](defining-component-categories.md)
-   [將圖示與類別產生關聯](associating-icons-with-a-category.md)

 

 




