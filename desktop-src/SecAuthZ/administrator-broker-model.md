---
description: 應用程式分成兩個程式。 其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: 系統管理員訊息代理程式模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849883"
---
# <a name="administrator-broker-model"></a>系統管理員訊息代理程式模型

在系統管理員訊息代理程式模型中，應用程式分成兩個程式。 其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。

使用應用程式資訊清單，將標準使用者程式標示為 **asInvoker** 的 **並無 requestedexecutionlevel** ，並將系統管理程式標示為並無 requestedexecutionlevel **requireAdministrator**。 使用者會先啟動標準使用者程式。 當使用者嘗試執行需要完整系統管理員存取權杖的作業時，標準使用者程式會呼叫 [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) 函數來啟動系統管理程式。 **ShellExecute** 函式會在使用使用者的完整系統管理員存取權杖執行應用程式之前，提示使用者進行核准。 然後，系統管理程式可以執行需要系統管理員許可權的工作。

系統管理程式未完全與標準使用者程式隔離。 系統管理程式可以啟用與標準使用者程式之間的處理序間通訊。 不過，這類通訊會受限於預設的強制完整性原則。 如需強制完整性考慮的詳細資訊，請參閱將 [應用程式設計成以低完整性層級執行](/previous-versions/dotnet/articles/bb625960(v=msdn.10))。

以下是系統管理員 broker 模型的可能用途：

-   開發嚮導。 當硬體 wizard 判定電腦上未安裝必要的驅動程式，或位於企業的核准位置時，它會呼叫提高許可權的應用程式，並將驅動程式移至電腦存放區。
-   Autorun.exe 呼叫 Setup.exe。 當使用者從 CD 執行軟體時，Autorun.exe 是以標準使用者身分執行，則會啟動以系統管理員身分執行的 Setup.exe，以將軟體安裝在電腦上。

以下是使用系統管理員訊息代理程式模型的缺點：

-   從應用程式到應用程式的轉換可能會對使用者造成混淆。 將新應用程式顯示在監視器上的原因可能很難通知使用者。
-   可能很難在兩個應用程式之間傳遞狀態資訊。 例如，您不會使用此模型在標準使用者控制台之間傳遞狀態資訊 (CPL) 與其系統管理員對應，只是讓相同的 CPL 具有系統管理和標準使用者功能。 標準使用者 CPL 必須將其狀態儲存在某個位置。
-   分割兩個程式之間的功能時，可能會有許多已複寫的程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發需要系統管理員許可權的應用程式](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[系統管理員 COM 物件模型](administrator-com-object-model.md)
</dt> <dt>

[作業系統服務模型](operating-system-service-model.md)
</dt> <dt>

[提高許可權的工作模型](elevated-task-model.md)
</dt> </dl>

 

 
