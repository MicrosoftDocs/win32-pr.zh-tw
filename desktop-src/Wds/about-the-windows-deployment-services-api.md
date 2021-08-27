---
title: 關於 Windows 部署服務 API
description: Windows (WDS) 部署服務是一套元件，可讓您部署 Windows 作業系統，尤其是 Windows Vista 和更新版本，以及 Windows Server 2008 和更新版本。
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows部署服務 Windows 部署服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098678"
---
# <a name="about-the-windows-deployment-services-api"></a>關於 Windows 部署服務 API

Windows (WDS) 部署服務是一套元件，可讓您部署 Windows 作業系統，尤其是 Windows Vista 和更新版本，以及 Windows Server 2008 和更新版本。 您可以使用它來設定使用以網路為基礎之安裝的新電腦。

oem、系統建造商和企業 IT 專業人員，想要瞭解如何將 Windows 部署到新電腦上的詳細資訊，請參閱[Windows 部署服務更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10))和[Windows 自動化安裝套件 (WAIK) ](https://www.microsoft.com/download/details.aspx?id=10333)中的標準 WDS 解決方案的相關資訊。

在無法使用標準 WDS 解決方案的環境中，WDS API 可讓您以程式設計方式存取某些 WDS 元件。

-   [Windows 部署服務伺服器函數](windows-deployment-services-server-functions.md)可讓您以程式設計方式存取 WDS 開機前執行環境 (PXE) 伺服器。 WDS 伺服器元件包含 PXE 伺服器和簡單檔案傳輸通訊協定 (TFTP) server，以便網路將電腦開機以載入和安裝作業系統。
-   [Windows 部署服務用戶端](windows-deployment-services-client-functions.md)函式可讓您以程式設計方式存取 WDS 用戶端。 WDS 用戶端元件包含在 Windows 預先安裝環境內執行的圖形化使用者介面 (Windows PE) 並與伺服器元件通訊，以選取並安裝作業系統映射。
-   WDS 管理元件沒有 API。 這些元件是您用來管理伺服器、作業系統映像以及用戶端電腦帳戶的一組工具。 如需 WDS 管理元件的詳細資訊，請參閱[Windows 部署服務更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10))。

WDS PXE 伺服器是由 PXE 伺服器和 PXE 提供者所組成。 PXE 伺服器包含核心網路功能。 PXE 伺服器支援外掛程式介面，也就是所謂的 PXE 提供者。 此提供者模型可讓您開發自訂 PXE 解決方案，同時繼續使用核心 PXE 伺服器網路程式碼基底。

-   開發人員可以使用[Windows 部署服務 Server](windows-deployment-services-server-functions.md)函式來撰寫自訂提供者的 DLL，以便在 WDS 伺服器上與標準開機資訊協商層（ (BINL) ）一起取代或執行。 例如，自訂提供者可以使用文字檔做為其資料存放區，而不是 Active Directory。
-   開發人員可以使用[Windows 部署服務伺服器](windows-deployment-services-server-functions.md)函式，在已註冊之提供者的已排序清單中，撰寫在 BINL 或任何其他 PXE 提供者之前排序的篩選器提供者。 第二個提供者只會服務選取的 PXE 要求，而第一個提供者會處理其他要求。 例如，這可以讓已排序清單中的第二個已註冊提供者提供新功能，而不會中斷第一個提供者所執行的現有 WDS 解決方案。

WDS 用戶端包含圖形化使用者介面，可在 Windows 預先安裝環境內執行 (Windows PE) 並與伺服器元件通訊，以選取並安裝作業系統映射。 WDS 用戶端程式庫支援開發可使用 WDS 伺服器的自訂用戶端應用程式。

-   開發人員可以使用[Windows 部署服務用戶端功能](windows-deployment-services-client-functions.md)來撰寫自己的自訂用戶端應用程式，以取代 WDS 用戶端。 例如，自訂應用程式可以列舉儲存在 WDS 伺服器上的映射，並將安裝進度訊息傳送至 PXE 伺服器事件記錄檔。

## <a name="windows-deployment-services-samples"></a>Windows部署服務範例

microsoft Windows 軟體開發套件 (sdk) 提供範例自訂 PXE 提供者、篩選提供者和 WDS 用戶端應用程式，請參閱[microsoft Windows 軟體開發套件 (sdk) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)。

您可以在 [桌面程式碼庫](https://github.com/microsoft/Windows-classic-samples)中，線上下載下列 WDS 範例。

<dl>

[Windows部署服務篩選器提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows部署服務映射列舉範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows部署服務多播取用者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows部署服務多播提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows部署服務提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows部署服務傳輸管理員範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Windows 部署服務伺服器 API](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[使用 Windows 部署服務用戶端 API](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 