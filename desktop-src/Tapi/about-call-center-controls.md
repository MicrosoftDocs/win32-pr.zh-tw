---
description: TAPI 3 定義了五個主要 ACD 物件，代理程式會將 ACD 的佇列分組代理程式和代理程式會話。 它也會使用額外的介面 ITTAPICallCenter 來延伸 TAPI 物件。
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: 關於撥置中心控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115529"
---
# <a name="about-call-center-controls"></a>關於撥置中心控制項

TAPI 3 定義五個主要 ACD 物件：代理程式處理常式、佇列、ACD 群組、代理程式和代理程式會話。 它也會以額外的介面（ [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)）擴充 TAPI 物件。

## <a name="agent-object"></a>Agent 物件

Agent 物件代表能夠處理呼叫的代理程式。 這通常是一個人，但可能是 IVR 或其他軟體和硬體的組合。 代理程式是電話中心的關鍵;它們負責接收和處理來電，有時也會對客戶或潛在客戶發出傳出的呼叫。

在 TAPI 中，代理程式物件與使用者帳戶直接相關，以提供與現有舊版切換系統的相容性。 此外，為了提供與現有舊版切換系統的相容性，代理程式可能也會與交換器代理程式識別碼相關聯。

代理程式物件會公開 [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) 介面。 這個介面會執行可建立代理程式會話的方法，並取得統計資料，例如已處理的總呼叫。 應用程式可以使用代理程式物件來操作代理程式狀態，並判斷全域代理程式統計資料。

## <a name="agent-handler-object"></a>代理程式處理常式物件

代理程式處理常式代表能夠將呼叫傳遞給代理程式群組的軟體或硬體。 一般來說，這是一種將外部線路連接到代理程式工作站電話的專屬交換器。 大部分的 ACD 系統只有一個這類交換器，但是大型作業可能會有更多。 如果代理程式在一個以上的 ACD 系統上有裝置，則代理程式會看到對應的代理程式處理常式物件數目。 此外，也會有代理程式物件的實例，其與代理程式在每個 ACD 系統上的外觀有關。

代理程式處理常式物件會公開 [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) 介面。 這個介面會執行方法，以提供與代理程式處理常式相關聯之 [ACD 群組](#acd-group-object) 的相關資訊，以及可使用的位址。

## <a name="agent-session-object"></a>代理程式會話物件

代理程式會話代表已登入且有資格處理特定 [ACD 群組](#acd-group-object)之呼叫的代理程式。 代理程式會話是動態建立的物件，它會將代理程式與 ACD 群組產生關聯，而這些物件會提供服務，同時也會在位址接收呼叫， (刀架、站、電話等 ) 。 應用程式可以使用代理程式會話物件來追蹤特定 ACD 群組內的代理程式活動。

代理程式會話物件會公開 [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) 介面。 這個介面會實作為通話的平均交談時間等資訊的方法。

## <a name="acd-group-object"></a>ACD 群組物件

ACD 群組代表需要特定類型處理的呼叫類別。 例如，銀行撥接中心的部分來電可能會考慮現有的帳戶，其他則可能與新帳戶相關。 有些代理程式在這兩個領域中可能都有專業知識，但大多都是特製化。 將會建立 ACD 群組來處理每種類型的呼叫。 ACD 群組服務一或多個佇列。 進行分類時，系統會將這些呼叫傳遞給與相關 ACD 群組相關聯的佇列。 離開佇列的呼叫會傳遞給已建立 [代理程式會話物件](#agent-session-object) 的代理程式，指出它們能夠處理來自該 ACD 群組的呼叫。

ACD 群組物件會公開 [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) 介面。 這個介面會執行方法，以提供與目前 ACD 群組相關聯之佇列的存取權。

## <a name="queue-object"></a>Queue 物件

Queue 物件代表 ACD 系統內的某個點，其中的呼叫會暫時保留暫止的動作。 Queue 物件會公開 [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) 介面。 此介面會執行收集佇列統計資料的方法，例如目前已排入佇列的呼叫數目。 [ACD Proxy](acd-proxy.md)會使用此資訊將呼叫散發給代理程式，並產生系統管理報告。

佇列物件的存取權可讓應用程式讀取與佇列使用相關的各種標準統計資料，但不會讓它能夠控制佇列上的呼叫。 只有具有相關聯位址和行存取權的應用程式 (通常是 ACD proxy 應用程式) 能夠控制佇列上的呼叫。

大部分的佇列會直接與 [ACD 群組物件](#acd-group-object)相關聯，而且會保留呼叫，直到代理程式可以處理它為止。 可能存在其他佇列，以允許複雜的呼叫指南 (所定義的路徑，未接聽的呼叫將會透過切換) 來執行。 例如，呼叫可能會被放入佇列中，然後才會路由傳送至 ACD 群組所服務的佇列。

 

 
