---
title: 同步處理點
description: 在 IStorage 相同的物件上支援屬性集時，請務必留意基底儲存體和屬性儲存體之間的同步處理點。
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034878"
---
# <a name="synchronization-points"></a>同步處理點

在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)相同的物件上支援屬性集時，請務必留意基底儲存體和屬性儲存體之間的同步處理點。

屬性集儲存區會將屬性集資料流程保存在內部緩衝區中，直到該緩衝區透過 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 方法認可為止。 無論 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 是在交易模式或直接模式中開啟，都是如此。

 

 




