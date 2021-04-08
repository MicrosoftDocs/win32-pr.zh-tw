---
title: 屬性和方法
description: 就像任何 OLE 物件一樣，控制項可透過一組包含屬性和方法的傳入介面，提供大部分的功能。
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021115"
---
# <a name="properties-and-methods"></a>屬性和方法

就像任何 OLE 物件一樣，控制項可透過一組包含屬性和方法的傳入介面，提供大部分的功能。

控制項會透過 OLE automation 來公開屬性和方法，讓容器能夠在容器提供的程式設計語言的控制下存取這些屬性和方法。

為了支援透過使用者介面存取屬性，控制項提供屬性頁、OLEIVERB 屬性的支援 \_ 、每個屬性流覽，以及透過屬性變更通知的資料系結。

-   透過屬性頁，控制項可以顯示其屬性，並視需要顯示其容器。
-   藉由支援 OLEIVERB \_ 屬性，屬性專案就會顯示在容器的功能表上。 然後，終端使用者可以選取 [ **屬性** ] 專案來查看控制項的屬性頁，以及修改屬性。
-   每個屬性流覽支援的容器，可以將控制項的屬性顯示為較大屬性工作表的一部分，其中可能包含來自容器中數個控制項的屬性。
-   透過屬性變更通知，控制項可以通知用戶端其屬性已變更，讓用戶端可以執行任何必要的動作。

如需詳細資訊，請參閱下列主題：

-   [控制項屬性](control-properties.md)
-   [控制項方法](control-methods.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX 控制項](activex-controls.md)
</dt> <dt>

[屬性頁和屬性工作表](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




