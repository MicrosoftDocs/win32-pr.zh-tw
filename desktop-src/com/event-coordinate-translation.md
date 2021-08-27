---
title: 事件座標轉譯
description: 事件座標轉譯
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843c2e5a3f978f405a3c126ef6a246024b55ccd2f73fbf86a8eed285b6181169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993138"
---
# <a name="event-coordinate-translation"></a>事件座標轉譯

控制項的96規格需要針對控制項所引發的事件傳遞的座標，使其不會被 HIMETRIC 為以點為基礎。 這項變更會讓事件以屬性和方法來進行協調，因此座標轉譯不再是容器的責任。 這會引發特定的相容性問題，其中控制項會使用非預期的座標基底引發事件，這應該只是96控制項容器裝載舊版96前控制項的問題，如下所示：

-   當舊版的96前容器裝載96控制項時，控制項會將事件座標呈現為點，這應該不會造成容器任何問題，因為容器應辨識參數類型。
-   當96容器裝載96前控制項時，控制項將會顯示具有座標的容器，並預期容器會有任何需要的轉譯。 不過，96容器會預期控制項必須符合96控制項規格，並將其座標呈現為點。 控制項在容器所提供的 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)介面上使用 [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords)方法的方式，與用來達成此目標的屬性和方法相同。

因此，裝載96前控制項的96容器使用者必須注意，當引發事件時，可能需要進一步轉譯座標。

 

 




