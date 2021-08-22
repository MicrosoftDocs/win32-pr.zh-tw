---
title: Windows 應用程式的封裝、部署和查詢
description: 以程式設計方式建立 Windows 應用程式的應用程式套件，以及安裝、更新、查詢和卸載應用程式套件。
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814271"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Windows 應用程式的封裝、部署和查詢

您可以透過 msix/.appx 應用程式套件（以 OPC 格式為基礎）部署、管理和服務 Windows 應用程式 (包括 UWPs 和桌面) 應用程式。 每個應用程式套件都包含構成應用程式的檔案，以及描述要 Windows 之軟體的資訊清單檔。

## <a name="introduction"></a>簡介

開發人員通常會使用 Visual Studio 來建立和簽署應用程式套件。 如需詳細資訊，請參閱[使用 Visual Studio 封裝 UWP 應用程式](/windows/msix/package/packaging-uwp-apps)。

Microsoft Store 可讓您輕鬆地建立、提交應用程式，並將其銷售給全球各地的客戶。 如需詳細資訊，請參閱 [應用程式提交](/windows/uwp/publish/app-submissions)。

Windows PowerShell Cmdlet 可讓您在不使用存放區的情況下，安裝和管理企業營運 Windows 應用程式。 如需詳細資訊，請參閱 [Appx 模組 Cmdlet](/powershell/module/appx/index?view=win10-ps)。

您可以使用封裝、部署和查詢 Api，以程式設計方式執行下列工作：

-   建立 Windows 應用程式的應用程式套件
-   部署封裝的 Windows 應用程式
-   列舉系統上安裝的應用程式套件，並從其資訊清單取得其相關資訊
-   使用應用程式套件的內容

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                    | 描述                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何建立應用程式套件 (C++)](how-to-create-a-package.md)                                        | 瞭解如何使用封裝 API 來建立應用程式套件。                                                                                                                           |
| [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)      | 瞭解如何使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) 建立測試程式碼簽署憑證，讓您可以簽署應用程式套件。 |
| [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)                    | 瞭解如何使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署您的應用程式套件，以便進行部署。                                                                    |
| [如何針對應用程式封裝簽章錯誤進行疑難排解](how-to-troubleshoot-app-package-signature-errors.md) | 應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。 瞭解如何辨識這些失敗，以及該怎麼做。          |
| [如何以程式設計方式簽署應用程式套件 (c + +) ](how-to-programmatically-sign-a-package.md)          | 瞭解如何使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函數來簽署應用程式套件。                                                                                   |
| [如何開發使用自訂檔案的 OEM 應用程式](how-to-develop-oem-app-with-custom-file.md)         | 瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。                                                                                             |
| [ (c + +) 解壓縮應用程式套件內容 ](how-to-extract-content-from-a-package.md)                          | 瞭解如何使用封裝 API 從應用程式封裝解壓縮檔案。                                                                                                               |
| [查詢應用程式封裝資訊清單資訊 (c + +) ](how-to-query-package-identity-information.md)                   | 瞭解如何使用封裝 API 從應用程式套件資訊清單取得資訊                                                                                                            |
| [疑難排解](troubleshooting.md)                                                                   | 提供資訊，協助您針對封裝、部署或查詢應用程式封裝時所遇到的問題進行疑難排解。                                                                 |
| [封裝 API 參考](interfaces.md)                                                                | 封裝 API 會建立、讀取和寫入應用程式套件。                                                                                                                            |
| [部署 API 參考](package-deployment-api.md)                                                   | 部署 API 會安裝、更新及卸載應用程式套件。                                                                                                                    |
| [查詢 API 參考](functions.md)                                                                     | 查詢 API 會取得系統上所安裝之應用程式套件的相關資訊。                                                                                                               |
| [工具和 PowerShell Cmdlet](appx-packaging-tools.md)                                                 | 使用這些工具和 Cmdlet 來建立、安裝及管理應用程式套件。                                                                                                              |
| [SDK 範例](appx-packaging-samples.md)                                                                | 下載 SDK 範例，以示範 Windows apps 的封裝、部署和查詢 api。                                                                               |
| [詞彙](appx-packaging-glossary.md)                                                                  | 瞭解封裝、部署和查詢 Windows apps 的相關條款。                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**其他參考**
</dt> <dt>

[應用程式套件資訊清單結構描述](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows。ApplicationModel 封裝**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows。ApplicationModel. PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 