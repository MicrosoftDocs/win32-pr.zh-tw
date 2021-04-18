---
title: 缺點
description: 缺點
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507393"
---
# <a name="disadvantages"></a>缺點

同進程伺服器使用本機伺服器的編輯功能，提供物件處理常式的速度和大小優勢。 那麼，為什麼您會選擇將您的 OLE 應用程式實作為本機伺服器，而不是同進程伺服器？ 有幾個原因：

-   安全性。 只有本機伺服器的位址空間與用戶端隔離。 同進程伺服器會共用用戶端的位址空間和處理內容，因此在發生錯誤或惡意程式設計時可能較不穩定。
-   粒 度。 本機伺服器可以在許多不同的用戶端上裝載其物件的多個實例，在多個用戶端中的物件之間共用伺服器狀態的方式，可能是實作為同進程伺服器，而這只是載入至每個用戶端的 DLL。
-   相容性。 如果您選擇執行同進程伺服器，就會放棄不支援這類伺服器的 OLE 1 相容性。 這並不是許多開發人員的考慮，但如果是，則是重要的考慮。
-   無法支援連結。 同進程伺服器不能作為連結來源。 因為 DLL 無法自行執行，所以無法建立要連結的檔案物件。

儘管有這些缺點，同進程伺服器可能是其速度和大小的絕佳選擇，如果符合您的所有其他需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[優點](advantages.md)
</dt> <dt>

[同進程伺服器](in-process-servers.md)
</dt> </dl>

 

 




