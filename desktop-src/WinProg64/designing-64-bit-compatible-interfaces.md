---
title: 設計64位相容介面
description: 當您將新的資料類型或方法加入至介面、變更舊的資料類型，或不適當地使用資料類型時，就會發生回溯相容性問題。
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- 回溯相容性64位 Windows 程式設計
- 64位相容介面64位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，相容性
- 相容性64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300784"
---
# <a name="designing-64-bit-compatible-interfaces"></a>設計64位相容介面

從32位 Windows 移植到64位 Windows 本身，不應該為分散式應用程式建立任何問題，不論它們是使用遠端程序呼叫， (RPC) 直接還是透過 DCOM。 RPC 程式設計模型會指定在連接的每一端都有相同大小的妥善定義資料大小和整數類型。 此外，在針對64位 Windows 開發的 LLP64 抽象資料模型中，只有指標會展開至64位—所有其他整數資料類型仍維持32位。 由於指標是用戶端/伺服器連接的每一端的本機指標，通常會以 **null** 或非 **null** 標記的形式傳送，因此封送處理引擎可以明確地在連接的任一端處理不同的指標大小。

但是，當您將新的資料類型或方法加入至介面、變更舊的資料類型，或不適當地使用資料類型時，就會發生回溯相容性問題。 下列主題討論如何避免這些情況 (可能的) ，以及如何在無法避免的情況下，設計健全的因應措施。

## <a name="in-this-section"></a>本章節內容

-   [變更現有介面](changing-an-existing-interface.md)
-   [避免資訊隱藏](avoiding-information-hiding.md)
-   [避免多型](avoiding-polymorphism.md)
-   [在 IDL 檔案中使用新的資料類型](using-new-data-types-in-your-idl-file.md)
-   [為64位 Windows 準備您的應用程式](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>相關章節

如果您還不熟悉64位 Windows 的新資料類型、工作環境和 API 變更，請參閱準備使用64位 [windows](getting-ready-for-64-bit-windows.md)。

 

 




