---
title: 建立 Proxy 物件
description: 除了設計可執行 IAccessible 屬性和方法的類別之外，伺服器開發人員也可能需要設計 proxy 物件來監視可存取物件的存留期。
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133891"
---
# <a name="creating-proxy-objects"></a>建立 Proxy 物件

除了設計可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的類別之外，伺服器開發人員也可能需要設計 *proxy* 物件來監視可存取物件的存留期。 如果應用程式中的可存取物件可在應用程式執行時使用，則您不需要建立 proxy 物件。 如果可以在應用程式執行時終結可存取的物件，則您必須建立 proxy 物件。

## <a name="in-this-section"></a>本節內容

-   [什麼是 Proxy 物件？](what-are-proxy-objects.md)
-   [為何需要 Proxy 物件](why-proxy-objects-are-needed.md)
-   [Proxy 物件的設計考慮](design-considerations-for-proxy-objects.md)

 

 




