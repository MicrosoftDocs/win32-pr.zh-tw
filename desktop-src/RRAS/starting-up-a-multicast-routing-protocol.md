---
title: 啟動多播路由通訊協定
description: 下表摘要說明路由通訊協定與多播群組管理員之間啟動互動的一連串步驟。
ms.assetid: 14524745-5cf9-442c-a5b4-b1ef313151cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898a7e1357264a0f7330abb11a6de5f216bafbf3e2535a572a1e956bae151f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035518"
---
# <a name="starting-up-a-multicast-routing-protocol"></a>啟動多播路由通訊協定

下表摘要說明路由通訊協定與多播群組管理員之間啟動互動的一連串步驟。 第一個資料行描述路由通訊協定執行的動作，以及路由通訊協定對多播群組管理員的回應。 第二個數據行描述多播群組管理員對路由通訊協定的回應，以及多播群組管理員執行的任何動作，例如回呼。 第三個數據行顯示任何其他資訊。

資料表的每個資料列都代表一個步驟。



| 路由通訊協定動作                                                                                                                                                                                                                                                                                                                 | 多播群組管理員動作                                                                                                                                                                                                                                                                                                                                                                                                                                            | 備註                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 使用 [**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol) 函數向多播群組管理員註冊。                                                                                                                                                                                                                      | 返回路由通訊協定，在後續的 MGM API 呼叫中，通訊協定必須用來識別其本身的控制碼。                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                         |
| 判斷介面是否已擁有，以及使用 [**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface) 函式所擁有的路由通訊協定。                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | IGMP 可以使用此函式來判斷介面的擁有者，並使用這個函式所傳回的資訊執行特定通訊協定的處理。                                                                             |
| 使用 [**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership) 函式取得已啟用通訊協定之所有介面的擁有權。                                                                                                                                                                                | 如果 IGMP 已取得介面的擁有權，而且收到相同介面的 [**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership) 函式呼叫，請使用 [**PMGM \_ 停用 \_ IGMP \_ 回呼**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) 回呼來聯繫 IGMP。 一旦完成所有關于介面擁有權的多播資料變更，請使用 [**PMGM \_ 啟用 \_ igmp \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)，再次聯繫 igmp。<br/> | 除了 IGMP 之外，只有一個通訊協定可以擁有指定時間的介面。                                                                                                                                                            |
| 判斷路由器上群組成員資格的目前狀態。 這個動作是使用群組成員資格列舉函數來執行： [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)、 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)和 [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)。 | 傳回群組的清單。                                                                                                                                                                                                                                                                                                                                                                                                                                                | 路由通訊協定可以使用結果，根據已經加入的群組來決定要採取的動作。 如需使用這些函數的完整範例，請參閱 [列舉群組](enumerating-groups.md) 。<br/> |



 

 

