---
title: " (RRAS) 列舉群組"
description: 下表摘要說明路由通訊協定與多播群組管理員之間互動的一連串步驟。
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101838"
---
# <a name="enumerating-groups"></a>列舉群組

下表摘要說明路由通訊協定與多播群組管理員之間互動的一連串步驟。 第一個資料行描述路由通訊協定執行的動作，以及路由通訊協定對多播群組管理員的回應。 第二個數據行描述多播群組管理員對路由通訊協定的回應。 第三個數據行顯示任何其他資訊。

資料表的每個資料列都代表一個步驟。



| 路由通訊協定動作                                                                                                                                                    | 多播群組管理員動作                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 使用 [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) 函數取得列舉的控制碼。                                                         | 傳回控制碼。                                                                                                                                                                                                                                                                                             |
| 使用 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函數取得一或多個群組。                                                             | 傳回用戶端所提供之緩衝區中的任意數量群組。 如果在提供的緩衝區中無法傳回任何群組，則會傳回錯誤的 \_ \_ 緩衝區和傳回一個群組所需的緩衝區大小。<br/> 如果沒有 \_ 其他 \_ 群組，就會傳回錯誤 \_ 的專案。<br/> |
| 如果 \_ \_ 接收到緩衝區不足的錯誤，請使用指定大小的緩衝區再次呼叫 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函數。 |                                                                                                                                                                                                                                                                                                              |
| 繼續呼叫 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函式，直到錯誤 \_ 不再 \_ 收到任何專案為止 \_ 。                                   |                                                                                                                                                                                                                                                                                                              |
| 使用 [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) 函數結束列舉程式。                                                                   | 終結控制碼。                                                                                                                                                                                                                                                                                          |



 

 

 





