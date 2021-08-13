---
description: 服務通常會撰寫為主控台應用程式。
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: 服務進入點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8f44322048351161bb8f3b8afdd619129d18b5effb5dc850d8909afbb3673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888970"
---
# <a name="service-entry-point"></a>服務進入點

服務通常會撰寫為主控台應用程式。 主控台應用程式的進入點是它的 **主要** 功能。 **Main** 函數會從服務的登錄機碼接收 **ImagePath** 值的引數。 如需詳細資訊，請參閱 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數的「備註」一節。

當 SCM 啟動服務程式時，它會等候它呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 函數。 使用下列指導方針。

-   服務 \_ WIN32 專屬進程的服務 \_ \_ 應該立即從其主執行緒呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 。 您可以在服務啟動後執行任何初始化，如 [服務 ServiceMain](service-servicemain-function.md)函式中所述。
-   如果服務類型是服務 \_ WIN32 \_ 共用進程， \_ 而且程式中的所有服務都有一般的初始化，您可以在呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)之前，在主執行緒中執行初始化，只要它花費的時間不超過30秒。 否則，您必須建立另一個執行緒來進行一般初始化，而主執行緒會呼叫 **StartServiceCtrlDispatcher**。 在服務啟動之後，您仍然應該執行任何服務特定的初始化。

[**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)函式會針對進程中包含的每個服務，使用 [**服務 \_ 資料表 \_ 專案**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya)結構。 每個結構會指定服務的服務名稱和進入點。 如需範例，請參閱 [撰寫服務程式的主要功能](writing-a-service-program-s-main-function.md)。

如果 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 成功，則在進程中的所有執行中服務都進入服務停止狀態之前，呼叫的執行緒不會傳回 \_ 。 SCM 會透過具名管道將控制項要求傳送至此執行緒。 執行緒會作為控制項發送器，執行下列工作：

-   建立新的執行緒，以在新服務啟動時呼叫適當的進入點。
-   呼叫適當的 [處理常式](service-control-handler-function.md) 函式來處理服務控制要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫服務程式的 main 函數](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



