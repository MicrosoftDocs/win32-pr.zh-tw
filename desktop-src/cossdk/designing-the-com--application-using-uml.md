---
description: 開發成功的 COM + 應用程式需要預先設計的應用程式架構。
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: 使用 UML 設計 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385919"
---
# <a name="designing-the-com-application-using-uml"></a>使用 UML 設計 COM + 應用程式

開發成功的 COM + 應用程式需要預先設計的應用程式架構。 整合模組化語言 (UML) 是此設計開發的關鍵。 UML 是一種模型化標記法，適用于結合軟體產業最佳作法的應用程式資料和流程。 由於 UML 會將應用程式分成三個可反映應用程式的視圖，以及它的封裝和執行，因此模型化標記法可妥善擴充以支援企業模型化。

UML 會解決應用程式的三個觀點，如下所示：

-   靜態視圖，以使用者案例和類別圖所採用的資訊來建立模型。
-   動態視圖，使用順序、共同作業和狀態轉換圖表進行模型化。
-   功能視圖，這是使用虛擬程式碼和規格的較傳統描述性敘述。

這些視圖的資訊可透過下列三個可搭配 UML 運作的設計步驟來收集。 撰寫一行程式碼之前，您必須先建立下列模型：

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>概念模型
</dt> <dd>

決定需要哪些元件和服務。

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>邏輯模型
</dt> <dd>

判斷它們所屬的邏輯設計層。

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>實體模型
</dt> <dd>

判斷元件的實際位置，以及它們的編碼方式。

</dd> </dl>

然後，這些模型可以搭配以 UML 為基礎的案例工具使用。 如需這三種設計模型的詳細資訊，請參閱本節中的下列主題：

-   [概念模型：應用程式需求](the-conceptual-model--application-requirements.md)
-   [邏輯模型：應用程式定義和規劃](the-logical-model--application-definition-and-planning.md)
-   [實體模型：應用程式架構](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 設計假設和原則](com--design-assumptions-and-principles.md)
</dt> <dt>

[使用 COM + 的一般設計秘訣](general-design-tips-for-using-com-.md)
</dt> <dt>

[優化與 COM + 商務邏輯層的互動](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[用來建立分散式應用程式的其他 Microsoft 工具](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



