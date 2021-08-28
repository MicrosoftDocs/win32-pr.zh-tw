---
title: 慣性
description: 本節說明 Windows Touch 的慣性。
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows觸控、慣性
- 慣性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ff1fd58d52ba73d758254c1dac1e8952df30b836b68ef12b022a29ceafc694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709808"
---
# <a name="inertia"></a>慣性

本節說明 Windows Touch 的慣性。

包含在 Windows 7 中的慣性 API，藉由提供簡單的物理模型，在 Windows Touch 應用程式中啟用一致的物件行為。 您可以使用慣性處理器（封裝功能的類別）來啟用慣性。 慣性處理器的運作方式，是在物件操作完成時處理傳遞給它的事件，並以與其他應用程式一致的方式處理物件軌跡。 請注意，慣性處理器與操作處理器緊密結合，以簡化對使用操作的應用程式加入慣性支援。 事實上，慣性處理器會引發操作處理器所執行的相同事件。 下一節將說明如何開始使用慣性。



| 區段                                                                      | 描述                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [慣性機制](inertia-mechanics.md)                                   | 說明慣性計算的基本概念。                                                                             |
| [處理非受控碼中的慣性](handling-inertia-in-unmanaged-code.md) | 說明如何使用 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面處理非受控碼中的慣性。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作和慣性](manipulation-and-inertia.md)
</dt> </dl>

 

 




