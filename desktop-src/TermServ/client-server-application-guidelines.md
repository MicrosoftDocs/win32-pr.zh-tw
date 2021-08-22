---
title: 用戶端/伺服器應用程式指導方針
description: 用戶端/伺服器應用程式不能假設單一電腦連接相當於單一使用者會話。
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d27f5bd024e2311307f39e4f86584747b59b874576e5cd5aa28e735b2945d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001616"
---
# <a name="clientserver-application-guidelines"></a>用戶端/伺服器應用程式指導方針

用戶端/伺服器應用程式不能假設單一電腦連接相當於單一使用者會話。 這是 [IP 位址和電腦名稱稱](ip-addresses-and-computer-names.md)中所討論之問題的特殊案例。

若要唯一識別用戶端/伺服器連接，每個用戶端模組都必須使用唯一的名稱或識別碼。 應用程式可以使用命名物件或管道、通訊端或其他 IPC 方法。 如需詳細資訊，請參閱 [核心物件命名空間](kernel-object-namespaces.md)。

若要遠端桌面服務相容，用戶端/伺服器應用程式中的伺服器模組必須能夠處理從同一部電腦連接的多個用戶端。 為了達成此目的，伺服器模組必須透過定義完善的全域介面（例如 RPC 或具名管道）接受用戶端連接。 伺服器和用戶端必須為每個使用者會話協調不同的通道。 用戶端必須使用可輕鬆支援這類作業的通訊協定（例如 TCP/IP）來建立與伺服器的連線，其中每個用戶端應用程式都可以使用不同的通訊端連線。

用戶端模組可以呼叫 [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) 函式，以取得其遠端桌面服務會話的識別碼。 然後，用戶端會使用某種形式的處理序間通訊，將其會話識別碼傳遞至伺服器模組。 然後，用戶端和伺服器模組可以使用會話識別碼設定私人通道。 例如，伺服器模組可以使用會話識別碼來存取核心物件的會話命名空間中的物件。

此外，伺服器模組可以使用 [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) 呼叫中的會話識別碼，來取得用戶端的其他相關資訊。 伺服器模組也可以使用 [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) 呼叫中的會話識別碼，在用戶端終端機上顯示訊息。 伺服器模組也可以建立兩個事件，以監視會話的用戶端連接和中斷連接。 但是，它必須在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上註冊才能完成此動作。 如需詳細資訊，請參閱 [監視會話連接和中斷連接](monitoring-session-connections-and-disconnections.md)。

提示使用者輸入是用戶端/伺服器應用程式可能發生的問題來源。 例如，如果服務呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) 函式，則訊息方塊會顯示在 RD 工作階段主機伺服器的桌面上，而不會顯示在用戶端桌面上。 若要在用戶端桌面上顯示訊息，服務可以呼叫 [**WtsSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) 函數。 或者，服務可以要求用戶端模組的輸入，而且用戶端模組可以顯示使用者介面，並將產生的輸入傳回服務。

從多個會話產生的進程，可以透過使用共用記憶體區塊，將資料傳送到彼此，並接收彼此的資料。 如需詳細資訊，請參閱 [建立命名共用記憶體](/windows/desktop/Memory/creating-named-shared-memory)。 在下列情況下，無法使用共用記憶體：

-   使用共用記憶體區塊的處理常式是由多個會話所產生。
-   這些會話會共用相同的使用者驗證認證。

 

 