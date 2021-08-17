---
title: 系統管理應用程式案例
description: 系統管理應用程式會呼叫 MGM 函式的子集，這些函式與列舉多播轉送專案 (MFEs) 和 MFE 統計資料相關。
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791913"
---
# <a name="administrative-application-scenario"></a>系統管理應用程式案例

系統管理應用程式會呼叫 MGM 函式的子集，這些函式與列舉多播轉送專案 (MFEs) 和 MFE 統計資料相關。 應用程式不需要向多播群組管理員註冊，就能使用這些函式 (也就是應用程式不需要控制碼) 。

## <a name="enumerating-mfes"></a>列舉 MFEs

下表摘要說明系統管理應用程式與多播群組管理員之間互動的一連串步驟。 第一個資料行描述系統管理應用程式執行的動作，以及管理應用程式對多播群組管理員的回應。 第二個數據行描述多播群組管理員對系統管理應用程式的回應。 第三個數據行顯示任何其他資訊。

資料表的每個資料列都代表一個步驟。



| 系統管理應用程式動作                                                                                                                                                                                      | 多播群組管理員動作                                                                                                                                                                                                                                                              | 備註                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 使用 [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) 函數取得一或多個 MFEs。                                                                                                                                   | 傳回用戶端所提供的緩衝區所能容納的 MFEs 數目。 如果提供的緩衝區中沒有可傳回的 MFEs，則傳回錯誤的 \_ \_ 緩衝區和傳回一個 MFE 所需的緩衝區大小。<br/>                                                              | 用戶端也可以使用對應的統計資料函式（ [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) 和 [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)）來取出 MFE 統計資料。 |
| 如果 \_ \_ 接收到緩衝區不足的錯誤，請使用指定大小的緩衝區再次呼叫 [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) 函數。                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| 繼續呼叫 [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) 函式，並將上一個呼叫所傳回的其中一個參數提供給 [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) 函式的最後一個 MFE。 | 傳回用戶端所提供的緩衝區所能容納的 MFEs 數目。 如果提供的緩衝區中沒有可傳回的 MFEs，則會傳回錯誤的 \_ \_ 緩衝區，以及一個 MFE 所需的緩衝區大小。<br/> \_ \_ \_ 當沒有其他 MFEs 時，會傳回錯誤的專案。<br/> |                                                                                                                                                                                                 |
| 繼續列舉，直到錯誤 \_ 不再 \_ \_ 收到任何專案為止。                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> 您可以使用 [**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) 和 [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) 函數來取出特定 MFE 或特定的 MFE 統計資料集。

 

 

 





