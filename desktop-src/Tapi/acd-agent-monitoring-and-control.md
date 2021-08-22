---
description: 您可以透過這些功能來監視和控制 ACD 代理程式的狀態 lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState 和 lineSetAgentActivity。
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: ACD 代理程式監視和控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8986fc31e8b30e8b32c4b347a26abfa46adbd426c20c506553ae2f41ea879a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872655"
---
# <a name="acd-agent-monitoring-and-control"></a>ACD 代理程式監視和控制

您可以透過下列函式來監視和控制工作站上的 ACD 代理程式狀態： [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)、 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)、 [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)、 [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)、 [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)、 [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)和 [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)。

[**行 \_ AGENTSTATUS**](line-agentstatus.md)訊息是用來指出代理程式資訊變更的時間。

這些控制項與位址（而不是線條）相關聯，因為許多 ACD 系統都是以與電話終端機上的按鈕相關聯的不同 ACD 佇列來執行， (並) 個別的呼叫外觀。 此外，ACD 代理程式電話通常可以有個別通話的個別通話外觀。

在架構上，ACD 功能應該在以伺服器為基礎的應用程式中執行。 上述用戶端函式（而不是對應至電話語音服務提供者）會傳達給已註冊 (的伺服器應用程式，並使用 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) 的選項作為這類函數的處理常式。 [**\_ PROXYREQUEST**](line-proxyrequest.md)訊息是用來在提出要求時，對處理常式應用程式發出信號，它會呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)函式來傳回結果和資料。 處理常式應用程式也可以在必要時呼叫 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 來產生行 \_ AGENTSTATUS 訊息。 如果是採用 ACD 功能本身的傳統 PBX 或獨立 ACD，則交換器的電話語音服務提供者必須包含可接受要求的 proxy 伺服器應用程式，並將其路由 (可能使用 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) 函式或) 給服務提供者的私用介面，以將它們路由傳送至交換器。

 

 



