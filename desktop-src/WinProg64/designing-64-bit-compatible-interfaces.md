---
title: 設計64位相容介面
description: 當您將新的資料類型或方法加入至介面、變更舊的資料類型，或不適當地使用資料類型時，就會發生回溯相容性問題。
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- 回溯相容性 64-位 Windows 程式設計
- 64位相容介面64位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，相容性
- 相容性 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc4647899f66463835fe03ddfdc9e0651fa2caf50d8eabe18471060a42e902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928005"
---
# <a name="designing-64-bit-compatible-interfaces"></a>設計64位相容介面

從32位 Windows 移植至64位 Windows 不應該自行針對分散式應用程式建立任何問題，不論它們是使用遠端程序呼叫， (RPC) 直接或透過 DCOM。 RPC 程式設計模型會指定在連接的每一端都有相同大小的妥善定義資料大小和整數類型。 此外，在針對64位 Windows 開發的 LLP64 抽象資料模型中，只會將指標展開至64位，所有其他整數資料類型仍維持32位。 由於指標是用戶端/伺服器連接的每一端的本機指標，通常會以 **null** 或非 **null** 標記的形式傳送，因此封送處理引擎可以明確地在連接的任一端處理不同的指標大小。

但是，當您將新的資料類型或方法加入至介面、變更舊的資料類型，或不適當地使用資料類型時，就會發生回溯相容性問題。 下列主題討論如何避免這些情況 (可能的) ，以及如何在無法避免的情況下，設計健全的因應措施。

## <a name="in-this-section"></a>本章節內容

-   [變更現有介面](changing-an-existing-interface.md)
-   [避免資訊隱藏](avoiding-information-hiding.md)
-   [避免多型](avoiding-polymorphism.md)
-   [在 IDL 檔案中使用新的資料類型](using-new-data-types-in-your-idl-file.md)
-   [準備您的應用程式以進行64位 Windows](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>相關章節

如果您還不熟悉適用于64位 Windows 的新資料類型、工作環境和 API 變更，請參閱[準備取得64位 Windows](getting-ready-for-64-bit-windows.md)。

 

 




