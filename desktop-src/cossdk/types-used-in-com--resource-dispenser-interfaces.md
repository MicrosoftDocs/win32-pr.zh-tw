---
description: COM + 資源配置器介面中使用的類型
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: COM + 資源配置器介面中使用的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e98473ce108ea280532c2188e911b488e42669b98273b14fc229d003905b581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305228"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>COM + 資源配置器介面中使用的類型

以下是在資源配置器介面中使用的類型。



| 類型           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | **DWORD** ，識別資源的類型，而不是特定的資源。 **RESTYPID** 通常是在配置器記憶體中描述資源類型之結構的指標。 分配器管理員不了解 (，也不需要瞭解資源配置器記憶體中) 此結構。 分配器管理員只使用 **RESTYPID** 來參考資源配置器內的資源類型。                                                                                                                                   |
| **渣 油**      | 識別特定資源的 **DWORD** ，而不是資源的類型。 **RESID** 通常是 (**void \* *_) ，指向資源配置器記憶體中代表資源的結構。在資源配置器的記憶體中，分配者管理員不需要瞭解此結構。分配器管理員會使用 _* RESID** 來參考資源配置器內的特定資源。                                                                                                                                 |
| **SRESID**     | **RESID** 的 Unicode 字串版本，用於 [**IHolder：： TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources)和 [**IHolder：： UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources)方法。 當您只需要記錄資源的少量資訊，而且該資源的整個描述可以包含在 **SRESID** 中時，字串有時很有用。 尤其是，使用 **SRESID** 可能會在資源代表兩個 (或更多) 專案之間的關聯性時，消除資源配置器中的對應需求。 |
| **TRANSID**    | 識別交易。 此類型可以轉換成 **ITransaction** 介面。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | 表示資源在損毀之前可以處於非使用中狀態的時間長度。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM + 資源配置器介面](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



