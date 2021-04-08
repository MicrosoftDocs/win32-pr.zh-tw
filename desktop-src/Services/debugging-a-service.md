---
description: 您可以使用下列任何一種方法來對服務進行 debug。
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: 對服務進行偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690076"
---
# <a name="debugging-a-service"></a>對服務進行偵錯

您可以使用下列任何一種方法來對服務進行 debug。

-   使用您的偵錯工具，在服務執行時進行偵錯工具。 首先，取得服務進程 (PID) 的處理序識別碼。 取得 PID 之後，請附加至正在執行的進程。 如需語法資訊，請參閱偵錯工具隨附的檔。
-   呼叫 [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) 函式來叫用偵錯工具，以進行即時的偵錯工具。
-   指定啟動程式時要使用的偵錯工具。 若要這樣做，請在下列登錄位置中建立名為 **影像檔執行選項** 的金鑰：

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion**

    使用與服務相同的名稱建立子機碼 (例如 MYSERV.EXE) 。 若要使用這個子機碼，請新增名為 **[偵錯工具**] 的 **REG \_ SZ** 類型值。 使用偵錯工具的完整路徑做為字串值。 在 [服務控制台] 小程式中，選取您的服務，按一下 [ **啟動** ]，然後核取 [ **允許服務與桌面互動]**。 服務必須是互動式服務，否則偵錯工具無法在預設桌面上執行。 請注意，Windows Vista 不再支援這項技術，因為所有服務都是在專為服務保留的會話中執行，而且不支援顯示使用者介面。

-   使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 來記錄資訊。

若要將自動啟動服務的初始化程式碼進行偵錯工具，您必須以隨選啟動服務的方式暫時安裝和執行服務。

有時候，可能需要以主控台應用程式的形式執行服務，以進行偵測。 在此案例中， [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 函式會傳回 **錯誤的 \_ \_ SERVICE \_ CONTROLLER \_ CONNECT**。 因此，請務必將您的程式碼結構，使其不會在傳回此錯誤時呼叫服務特定程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將服務應用程式偵錯工具](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Windows 的偵錯工具](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
