---
title: 建立 Proxy 物件
description: 除了設計可執行 IAccessible 屬性和方法的類別之外，伺服器開發人員也可能需要設計 proxy 物件來監視可存取物件的存留期。
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671903"
---
# <a name="creating-proxy-objects"></a>建立 Proxy 物件

除了設計可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的類別之外，伺服器開發人員也可能需要設計 *proxy* 物件來監視可存取物件的存留期。 如果應用程式中的可存取物件可在應用程式執行時使用，則您不需要建立 proxy 物件。 如果可以在應用程式執行時終結可存取的物件，則您必須建立 proxy 物件。

## <a name="in-this-section"></a>本節內容

-   [什麼是 Proxy 物件？](what-are-proxy-objects.md)
-   [為何需要 Proxy 物件](why-proxy-objects-are-needed.md)
-   [Proxy 物件的設計考慮](design-considerations-for-proxy-objects.md)

 

 




