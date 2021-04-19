---
description: COM + 應用程式的類型
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: COM + 應用程式的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973391"
---
# <a name="types-of-com-applications"></a>COM + 應用程式的類型

以下是四種基本的 COM + 應用程式類型：

-   **伺服器應用程式。** COM + *伺服器應用程式* 會在自己的進程中執行。 伺服器應用程式可支援所有 COM + 服務。
-   **程式庫應用程式。** COM + 連結 *庫應用程式* 是在建立它的用戶端的進程中執行。 更具體來說，程式庫應用程式中的元件一律會載入至建立者的進程。 程式庫應用程式未與伺服器進程明確相關聯。 他們可以使用以角色為基礎的安全性，但不支援遠端存取或已排入佇列的元件。
-   **應用程式 proxy。** *應用程式 proxy* 是一組檔案，其中包含可讓用戶端從遠端存取服務器應用程式的註冊資訊。 在用戶端電腦上執行時，應用程式 proxy 檔案會將 COM + 伺服器應用程式的相關資訊（包括 Clsid、Progid、RemoteServerName 和封送處理資訊）寫入用戶端電腦。 然後可以從用戶端電腦遠端存取服務器應用程式。
-   **Com + 預先安裝的應用程式**。 COM + 包含一組預先安裝的應用程式，可處理內建函式。 預先安裝的應用程式會列在 [元件服務] 系統管理工具的 [COM + 應用程式] 資料夾中，但無法修改或刪除這些應用程式。 這些應用程式包括下列各項：
    -   .NET 公用程式
    -   分析器控制項發行者應用程式
    -   COM + Explorer
    -   COM + QC 無效信件佇列接聽程式
    -   COM + 公用程式
    -   IIS In-Process 應用程式
    -   IIS 跨進程集區應用程式
    -   系統應用程式

## <a name="notes"></a>備註

從 Windows Server 2003，即使已停用系統應用程式，也可以執行 COM + 應用程式。 COM + 應用程式將會執行，但不會有系統應用程式通常提供的服務。 這些服務包括使用元件服務系統管理工具和系統事件追蹤。

此外，從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。 此值會在啟動系統應用程式時，將 CoInitializeSecurity 函式與[](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)函式搭配使用，以停用啟動為啟動 (AAA) 啟用。 將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。

 

 
