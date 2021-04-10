---
title: 定義元件類別
description: 定義元件類別
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184184"
---
# <a name="defining-component-categories"></a>定義元件類別

元件類別定義的作者會建立唯一的 GUID (與定義一起發行的 CATID) 。 其他合作物件知道此類型的定義，而且可以據此使用其支援的類別。 如同介面的方法簽章，在安裝之後，不應該修改分類的語法。 藉由引進具有修訂之語義的新分類識別碼，最好是維持類別的回溯相容性。

因為介面識別碼 (IID) 和元件類別識別碼 (CATID) 存在於不同的命名空間中，所以看起來像是可以針對 IID 和 CATID 使用相同的 GUID。 不過，由於 Iid 通常用於介面之 proxy/stub 伺服器的 CLSID，因此可能會發生衝突。 因此，請不要對 IID 和 CATID 使用相同的 GUID。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將圖示與類別產生關聯](associating-icons-with-a-category.md)
</dt> <dt>

[依元件功能分類](categorizing-by-component-capabilities.md)
</dt> <dt>

[依容器功能分類](categorizing-by-container-capabilities.md)
</dt> <dt>

[預設類別和關聯](default-classes-and-associations.md)
</dt> <dt>

[元件類別管理員](the-component-categories-manager.md)
</dt> </dl>

 

 




