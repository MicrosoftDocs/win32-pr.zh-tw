---
title: 設定虛擬目錄的許可權
description: 基於安全性理由，背景智慧型傳送服務 (位) 不會將檔案上傳到已啟用腳本和執行許可權的虛擬目錄。
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023694"
---
# <a name="setting-permissions-on-virtual-directories"></a>設定虛擬目錄的許可權

基於安全性理由，背景智慧型傳送服務 (位) 不會將檔案上傳到已啟用腳本和執行許可權的虛擬目錄。 如果您將檔案上傳到已啟用這些許可權的虛擬目錄，則作業會失敗，並出現錯誤碼為 \_ [ \_ 執行 BG E SERVER] \_ \_ 。

BITS 不需要啟用寫入虛擬目錄，因此建議您關閉虛擬目錄的寫入權限。

驗證的使用者 (或 IIS 匿名驗證的匿名使用者) 必須具有虛擬目錄所對應實體目錄的變更許可權;授與寫入權限沒有足夠的許可權。

## <a name="specifying-permissions-for-notifications"></a>指定通知的許可權

您為虛擬目錄和通知 URL 指定的驗證配置 (查看 [BITSServerNotificationURL](bits-iis-extension-properties.md) 屬性) 必須相容。 BITS 會使用針對虛擬目錄所指定的驗證配置來存取通知 URL。 如果 BITS 因為驗證失敗而無法存取通知 URL，則上傳作業會失敗。

如果通知類型 (看到[以傳址方式](using-bits-notification-request-response-headers.md)) 的[BITSServerNotificationType](bits-iis-extension-properties.md)屬性，應用程式必須確定使用者具有所參考檔案的存取權 (查看[BITS-要求-資料檔案名稱](notification-protocol-for-server-applications.md)標頭) 。 BITS 會將參考檔案上的 Acl 設定為虛擬目錄所對應之實體目錄的 Acl。

> [!Note]  
> 通知的應用程式必須能夠對應及存取遠端檔案，即使是由 web 伺服器所提供的服務，與實體上傳目錄不同的電腦上也一樣。 [位要求-資料檔案名稱](notification-protocol-for-server-applications.md)標頭一律包含相對於裝載 BITS 延伸模組元件之電腦的路徑規格。 在另一部電腦上執行的應用程式可能需要先將路徑轉換成 UNC 路徑，才能存取它。

 

BITS 支援許多驗證配置組合。 不過，您應該將下列驗證配置用於虛擬目錄和相符的通知 URL。

-   若要透過參考通知支援，您應該將虛擬目錄設定為使用 NTLM (協商) 驗證如果實體上傳目錄 (虛擬目錄所指向的目錄，) 使用非匿名的驗證配置。 如果實體上傳目錄允許匿名要求 (沒有驗證) ，虛擬目錄應該啟用匿名 (不) 驗證。

    您必須設定實體上傳目錄上的 Acl，讓已驗證的使用者可以讀取通知 URL 所指向之目錄中的檔案。 BITS 會使用實體上傳目錄的 Acl 來設定暫存上傳檔案的 Acl， ([位--](notification-protocol-for-server-applications.md) ------------------Name 標頭包含暫存檔) 的路徑

-   由於傳 [值](using-bits-notification-request-response-headers.md) 通知不需要通知的應用程式存取包含上傳內容的暫存檔，因此驗證配置可以是匿名或 (NTLM) 的 negotiate。 唯一的需求是，虛擬目錄的已驗證使用者也必須獲得授權，才能存取通知 URL。

## <a name="specifying-permissions-for-remote-shares"></a>指定遠端共用的許可權

虛擬目錄可指向不同電腦或網路共用上的對應磁片磁碟機。 如果它指向對應的網路磁碟機機，則用來對應磁片磁碟機的認證應該會在遠端共用上具有完整控制權。

如果虛擬目錄指向網路共用，BITS 會使用虛擬目錄的 **Connect As** 使用者認證來存取遠端共用。 若要存取遠端共用，[線上帳戶 **]** 帳戶必須具有許可權功能的檔中所 [**述的許可權**](/windows/desktop/api/winbase/nf-winbase-logonusera) 。 BITS 會使用 LOGON32 \_ 登入 \_ 批次或 LOGON32 \_ 登入 \_ 互動式登入類型來登入。 **Connect As** 使用者帳戶需要 Full-Access 遠端共用的許可權;授與寫入權限沒有足夠的許可權。

當實體上傳目錄對應到網路共用時，要求通知 URL 之呼叫端的身分識別是 [連接身分使用者] 或 [實體上傳 **]** 目錄的已驗證使用者 (只有在 IIS 6.0 和更新版本中，當您在 [**連接** 身分]) 對話方塊上選取 [**驗證網路資源的存取權時，一律使用已驗證的使用者認證**

 

 