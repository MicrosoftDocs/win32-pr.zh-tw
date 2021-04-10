---
title: RPC 和 COM 的版本控制理論
description: 遠端程序呼叫的版本設定理論 (RPC) 和 COM。
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- 遠端程序呼叫 RPC、最佳作法、版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093076"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>RPC 和 COM 的版本控制理論

只有兩個完全萬無一失的方法支援新功能，而不會有網路相容性問題的風險：

-   根據規則變更介面版本;這可防止新的用戶端與舊的伺服器通訊，而且可能會防止舊的用戶端與新的伺服器通訊。 本節稍後會說明這一點。
-   引進處理新功能的不同介面。

標準 RPC 介面可透過 GUID 和版本號碼組合來識別;COM 介面是由其 GUID 識別。 版本包含主要和次要部分。 如果是具有相同 GUID 和不同版本號碼的標準介面，則只有在主要版本相同，而且用戶端不是高於伺服器的次要版本時，才有可能連接。

結果是變更 RPC 介面的 GUID 中斷連線相容性，而變更介面名稱則否。

在標準 RPC 中，已妥善定義升級和延伸模組的路徑，而且基本上需要在介面結尾新增新的方法，而新的類型只能在新的方法中使用。 如果需要這類新增專案，則必須增加次要版本。 任何其他變更都需要主要版本的變更，因為用戶端和伺服器軟體在網路上會不相容。 遵循這些規則可確保新用戶端與舊伺服器之間有連接，反之亦然，雙方都完全相容。

如果是 COM 介面，則無法使用 version 屬性。 建立新的介面並繼承自舊介面，相當於在 RPC 中操作版本。 一般而言，COM 的最佳方法是為擴充的功能建立新的介面。 次要版本相當於繼承自舊版本的新介面。 變更舊的方法或舊的資料類型需要全新的 COM 介面，此介面不會繼承自舊的介面。

針對 COM， [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 函式是一種已建立的方法，可檢查伺服器是否支援介面;因此，可以輕鬆地解析用戶端可以與舊版本或新版介面互動的情況。

 

 