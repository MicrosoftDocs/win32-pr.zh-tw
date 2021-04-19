---
title: 簡單元素
description: 簡單元素是與其他元素共用 IAccessible 物件的 UI 元素，而且會依賴該 IAccessible 物件 (通常是其父) 來公開其屬性。
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969483"
---
# <a name="simple-elements"></a>簡單元素

*簡單元素* 是與其他元素共用 [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 UI 元素，而且會依賴該 **IAccessible** 物件 (通常是其父) 來公開其屬性。 為了區分共用 **IAccessible** 物件的元素，伺服器會為每個簡單專案指派一個唯一的正數子識別碼。 這項指派是依每個實例的介面來完成，因此識別碼在該內容中必須是唯一的。 許多實作為順序指派這些識別碼，從1開始。 此配置不允許簡單的元素擁有自己的子系。 簡單元素也稱為 *子* 系。

若要唯一識別和公開，簡單元素需要 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件和子系識別碼。 因此，當與 **IAccessible** 物件通訊時，用戶端必須提供適當的子系識別碼。 特殊的識別碼（ **CHILDID \_ SELF**）可以用來參考可存取的物件本身，而不是它的其中一個子系。

在簡單元素之間共用的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件通常會對應至使用者介面中的一般父物件。 例如，系統清單方塊會針對整體清單方塊和每個清單方塊專案的簡單元素公開可存取物件。 在此情況下，清單方塊的 **IAccessible** 物件也是清單專案的父代或容器。

如需可存取物件的詳細資訊，請參閱 [可存取的物件](accessible-objects.md)。

 

 




