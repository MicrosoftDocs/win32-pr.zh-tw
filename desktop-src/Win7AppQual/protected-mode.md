---
description: 受保護模式
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: 受保護模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116446"
---
# <a name="protected-mode"></a>受保護模式

在 Windows XP Service Pack 2 (SP2) 作業系統和更新版本的 Internet Explorer 8 中，大部分的 Windows Internet Explorer 8 安全性功能都有提供。 受保護模式僅適用于 Windows Vista 或更新版本，因為它是以 Windows Vista 的新功能為基礎：

-   [ (UAC) 的使用者帳戶控制 ](https://msdn.microsoft.com/library/aa511445.aspx) 可讓您在沒有系統管理員許可權的情況下輕鬆執行。 當使用者以有限的使用者權限執行程式時，攻擊者會比使用系統管理員許可權執行的程式更安全。 Windows 作業系統可以限制惡意程式碼免于執行損害的動作。
-   完整性機制會以較低完整性的程式限制對 [安全物件](../secauthz/securable-objects.md) 的寫入存取權，就像使用者帳戶群組成員資格限制使用者存取機密系統元件的許可權一樣。
-   [消費者介面許可權隔離 (UIPI) ](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) 可防止進程將選取的視窗訊息和其他使用者 api 傳送至以較高完整性執行的進程。

Windows 整合機制安全性基礎結構可讓受保護模式為 Windows Internet Explorer 提供使用者流覽 web 所需的許可權，以及使用者需要以無訊息模式安裝程式或修改機密系統資料的必要許可權。

使用者可以透過核取方塊停用這項功能，系統管理員可以使用群組原則來停用此功能。

> [!IMPORTANT]
> 在進行疑難排解時，您應該只將此功能停用為暫時量值，以在功能啟用時比較應用程式的行為。 建議您將此功能永久啟用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
