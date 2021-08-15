---
description: 此範例說明如何建立 Windows Installer 套件的 URL 型安裝。
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: 以 URL 為基礎的 Windows Installer 安裝範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c25fb4f84ff3507505be7f16675b8da39afd349cb1b4c78520ee3de004df749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013326"
---
# <a name="a-url-based-windows-installer-installation-example"></a>以 URL 為基礎的 Windows Installer 安裝範例

此範例說明如何建立 Windows Installer 套件的 URL 型安裝。 如需保護安裝和使用數位憑證的詳細資訊，請參閱[撰寫安全安裝](guidelines-for-authoring-secure-installations.md)和[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。

若要重現此範例，您需要 [SignTool](../seccrypto/signtool.md) 公用程式。 如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的[CryptoAPI 工具參考](../seccrypto/cryptoapi-tools-reference.md)。 您也需要[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)的[Msistuff.exe](msistuff-exe.md)和 Setup.exe 公用程式。 如需詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)啟動載入。

此範例具有下列規格：

-   當使用者造訪您的網站並按一下 [>mysetup.bat 安裝] 連結時，會顯示從該位置儲存或執行的選項。 如果使用者選取從該位置執行，Setup.exe 會在其電腦上升級 Windows Installer 的版本（如有必要），在安裝程式套件上驗證數位簽章，並在其電腦上安裝套件。
-   有一個 Mycert.cer 的數位憑證，Mycert.cer. pvk 提供了私密金鑰。
-   客戶會造訪以安裝套件之假設網站的 URL 為 HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html。
-   Web 服務器版面配置如下所示。 

    | URL                                                               | 檔案        | 描述                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Setup.exe 啟動載入器。                        |
    | HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | 安裝套件                           |
    | HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | 來源檔案封包 \# 1                        |
    | HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | 來源檔案封包 \# 2                        |
    | HTTPs： \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi    | Instmsi.exe | ANSI Windows Installer 2.0 可轉散發套件。    |
    | HTTPs： \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2.0 可轉散發套件。 |

    

     

[繼續](configuring-the-setup-exe-resources.md)

 

 
