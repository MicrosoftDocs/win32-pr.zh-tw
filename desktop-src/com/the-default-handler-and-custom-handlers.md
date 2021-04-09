---
title: 預設處理常式和自訂處理常式
description: 預設處理常式和自訂處理常式
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932037"
---
# <a name="the-default-handler-and-custom-handlers"></a>預設處理常式和自訂處理常式

大部分的應用程式會使用預設處理常式（OLE 提供的實值）做為處理常式。 當預設處理常式的功能不足時，應用程式會執行自訂處理常式。 自訂處理常式可以完全取代預設處理常式，或使用它在適當情況下提供的部分功能。 在後者的情況下，應用程式處理常式會實作為由新控制項物件和預設處理常式組成的匯總物件。 組合應用程式/預設處理常式也稱為同 *進程處理* 程式。 *遠端處理處理常式* 用於未在系統登錄中指派 CLSID 或沒有指定處理常式的物件。 這些物件類型的處理常式所需的全部都是在整個進程界限之間傳遞資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件處理常式](object-handlers.md)
</dt> </dl>

 

 




