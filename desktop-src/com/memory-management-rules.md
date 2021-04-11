---
title: 記憶體管理規則
description: 記憶體管理規則
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093399"
---
# <a name="memory-management-rules"></a>記憶體管理規則

介面指標的存留期一律是透過每個 COM 介面上的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來管理。 如需詳細資訊，請參閱 [管理參考計數的規則](rules-for-managing-reference-counts.md)。

針對所有其他參數，請務必遵守管理記憶體的特定規則。 下列規則適用于介面 methodsâ中的所有參數（包括不以傳值方式傳遞的 return valueâ€）：

-   參數必須由呼叫端配置及釋放。
-   Out 參數必須由被呼叫的參數進行配置;呼叫端會使用標準 COM 工作記憶體配置器來釋放它們。 如需詳細資訊，請參閱 [OLE 記憶體](the-ole-memory-allocator.md) 配置器。
-   In/out-參數一開始是由呼叫端配置，然後在必要時由呼叫的參數釋放和重新配置。 如果是 out 參數，呼叫端會負責釋出最後傳回的值。 必須使用標準 COM 記憶體配置器。

在後兩個案例中，其中一段程式碼會配置記憶體，而另一段程式碼會釋出記憶體，使用 COM 配置器可確保兩段程式碼使用相同的配置方法。

另一個需要特別注意的地方，就是在失敗狀況中處理 out 和 out 參數。 如果函式傳回失敗碼，呼叫端通常無法清除 out 或 out 參數。 這會導致下列其他規則：

-   如果發生錯誤情況，參數必須一律可靠地設定為將會清除的值，而不會由呼叫端執行任何動作。
-   所有 out 指標參數都必須明確設定為 **Null**。 這些通常會以指標對指標參數的形式傳遞，但也可以做為呼叫端所配置之結構的成員，以及呼叫的程式碼填滿。 確保這一點的最直接方式 (是在部分) 中，將這些值設定為函式專案的 **Null** 。 這項規則很重要，因為它可提升更健全的應用程式互通性。
-   在錯誤情況下，所有的 out 參數都必須由稱為 (的程式碼保持不變，因此會在呼叫端初始化它們) 或明確設定的值（如同 out 參數錯誤傳回案例中）。

請記住，這些適用于 COM 應用程式的記憶體管理慣例只適用于公用介面，而 APIsâ則是「COM 應用程式必須嚴格地內部進行記憶體配置，因此必須使用這些機制來完成。

COM 會在內部使用遠端程序呼叫， (RPC) 在用戶端與伺服器之間進行通訊。 如需在 RPC 伺服器 stub 中管理記憶體的詳細資訊，請參閱 [伺服器 Stub 記憶體管理](../rpc/server-stub-memory-management.md) 主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理記憶體配置](managing-memory-allocation.md)
</dt> </dl>

 

 