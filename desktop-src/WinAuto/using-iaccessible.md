---
title: 使用 IAccessible 介面
description: IAccessible 介面是一組方法的集合，這些方法會公開範圍廣泛的 UI 元素最常見的屬性和行為。
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c683e83928db53894c7c2c22976a5cf58c402c241e698dca5248230b1b24177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744893"
---
# <a name="using-the-iaccessible-interface"></a>使用 IAccessible 介面

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面是一組方法的集合，這些方法會公開範圍廣泛的 UI 元素最常見的屬性和行為。 UI 元素是使用者介面一部分的控制項，例如功能表或按鈕。 可存取的物件是具有有意義 **IAccessible** 介面的 UI 元素。

某些 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性不適用於每種使用者介面元素。 此外， **IAccessible** 的執行會因應用程式而異。

雖然已完整指定 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的參數和傳回值，但用戶端應該如何使用屬性或伺服器應該如何執行屬性，有時可能會受到解讀。

本節提供協助用戶端應用程式取得 UI 元素相關資訊，以及協助伺服器應用程式提供適當資訊的建議、指導方針和範例。

## <a name="in-this-section"></a>本節內容

-   [描述性屬性的內容](content-of-descriptive-properties.md)
-   [選取範圍和焦點屬性和方法](selection-and-focus-properties-and-methods.md)
-   [物件導覽屬性和方法](object-navigation-properties-and-methods.md)

 

 




