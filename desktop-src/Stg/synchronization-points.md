---
title: 同步處理點
description: 在 IStorage 相同的物件上支援屬性集時，請務必留意基底儲存體和屬性儲存體之間的同步處理點。
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675911"
---
# <a name="synchronization-points"></a>同步處理點

在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)相同的物件上支援屬性集時，請務必留意基底儲存體和屬性儲存體之間的同步處理點。

屬性集儲存區會將屬性集資料流程保存在內部緩衝區中，直到該緩衝區透過 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 方法認可為止。 無論 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 是在交易模式或直接模式中開啟，都是如此。

 

 




