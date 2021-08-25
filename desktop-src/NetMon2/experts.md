---
description: 專家是 Microsoft Win32 動態連結程式庫 (DLL) ，可分析網路封包提供者 (NPP) 所收集的網路流量，並放入 capture 檔案中。
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: 專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f4c3e34a9f6b8b36fdc6aa4793acfa5b652b9fa2c2117afc62943c0947af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890911"
---
# <a name="expert"></a>專家

專家是 Microsoft Win32 動態連結程式庫 (DLL) ，可分析 [*網路封包提供者*](n.md) (NPP) 所收集的網路流量，並放入 capture 檔案中。 在資料被捕獲並儲存在 capture 檔案中之後，專家就可以使用剖析器（也稱為通訊協定剖析器）來分析檔案中的資料。 例如，您可以檢查 capture 檔案的框架，並使用剖析 [*器來辨識通訊協定，例如*](p.md) 伺服器訊息區 (SMB) ，或傳輸控制通訊協定/網際網路通訊協定 (tcp/ip) 。

您可以設計專家來處理所有的網路監視器剖析器，以及您自行建立的任何剖析器。

當要求的通訊協定相符識別特定的畫面格之後，專家會將資料從框架中解壓縮。 您可以設計專家來管理網路監視器事件檢視器所顯示之可用資料的資訊。

您可以在執行時間設定專家，然後使用網路監視器儲存使用者設定資料，以使用不同的 capture 檔。 您可以使用專家為使用者提供相互關聯資料和自訂解決方案。 如需有關建立 HTML 設定資訊的詳細資訊，請參閱 [事件參考頁面](event-reference-page.md)。

在網路監視器設定期間，會在專家子目錄中安裝下列專家 Dll：

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

當您開始網路監視器時， [**DllMain**](dllmain-expert.md) 函式會建立專家子目錄中的所有專家。 當使用者在網路監視器 UI 的 [**工具**] 功能表上選取 **專家** 時，網路監視器載入專家 dll。 專家是透過 [註冊專家](register-expert.md) 進入點來呼叫，以提供專家的基本詳細資料。

![網路監視器專家對話方塊](images/expick.png)

網路監視器會呼叫下列函數來管理專家：

-   [**DllMain**](dllmain-expert.md)
-   [**註冊專家**](register-expert.md)
-   [**執行**](run.md)
-   [**設定**](configure.md)

專家必須執行上述各項功能。

 

 



