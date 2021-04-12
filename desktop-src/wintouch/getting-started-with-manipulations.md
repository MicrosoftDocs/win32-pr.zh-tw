---
title: 操作
description: 本節說明 Windows Touch 的物件操作。
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch，操作
- 操作，關於
- 操作，手勢差異
- 手勢、操作差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300187"
---
# <a name="manipulations"></a>操作

本節說明 Windows Touch 的物件操作。

## <a name="manipulation-overview"></a>操作總覽

要考慮操作的一個便利方式，就是將它們視為手勢的超集合。 您可以使用筆勢進行哪些動作，您可以利用更多的彈性，並使用操作來提供更精細的精確度。 操作和手勢之間的差異最好以簡單的範例來示範。 您可以展開物件，並使用操作將它轉譯;使用手勢時，您一次只能進行一個動作。 這項功能可以即時操作物件，藉由啟用更真實的體驗，讓應用程式更直覺化。

操作 Api 是用來針對已啟用觸控功能的應用程式，簡化對物件的轉換作業。 操作是在 Windows 7 中透過操作 COM 物件來執行。 藉由使用操作，開發人員可以更輕鬆地支援慣性 (物件物理) ，而且可以在與其他應用程式一致的方式中，輕鬆地執行物件的轉換。 下列各節說明您可以執行操作的各種方式。



| 區段                                                                                            | 描述                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [將操作支援新增至非受控碼](adding-manipulation-support-in-unmanaged-code.md) | 說明如何執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收，以及將事件處理常式新增至您的程式碼。 |
| [Advanced 操作](advanced-manipulations.md)                                               | 說明如何執行複雜的操作。                                                                                                       |
| [單一手指旋轉](single-finger-rotation.md)                                               | 說明如何使用資料透視點和操作處理器來旋轉物件。                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作和慣性](manipulation-and-inertia.md)
</dt> </dl>

 

 




