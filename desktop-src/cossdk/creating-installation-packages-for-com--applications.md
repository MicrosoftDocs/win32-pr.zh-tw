---
description: 建立 COM + 應用程式的安裝套件
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: 建立 COM + 應用程式的安裝套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972966"
---
# <a name="creating-installation-packages-for-com-applications"></a>建立 COM + 應用程式的安裝套件

您可以使用 [元件服務] 系統管理工具或 COM + 管理程式庫來建立 COM + 應用程式和應用程式 proxy 的安裝套件。

COM + 會產生 Windows Installer 安裝套件，其中單一檔案包含在另一部電腦上安裝 COM + 應用程式的所有必要部分。

匯出 COM + 應用程式時，[元件服務] 系統管理工具會決定應用程式的類別、元件和屬性集合，以及應用層級的屬性。 從這項資訊，[元件服務] 系統管理工具會產生單一 .msi 檔案，其中包含下列各項：

-   Windows Installer 具有 COM 註冊資訊的資料表 (如需詳細資料) ，請參閱 Windows Installer 檔。
-   包含應用程式屬性的 apl 檔。  (這是內部檔案;此檔案的格式未記載。 ) 
-   描述 COM + 應用程式類別所執行之介面的 Dll 和型別程式庫。

除了 .msi 檔案以外，[元件服務] 系統管理工具也會產生 ( .cab) 檔案的封包。 這個檔案會包裝 .msi 檔案，讓開發人員透過 Microsoft Internet Explorer 部署 COM + 應用程式。

> [!Note]  
> 匯出 COM + 應用程式時，[元件服務] 系統管理工具只會封裝應用程式的標準 COM + 元件。 例如，它不會封裝任何相依的 DLL 或資料檔案。 相依的 DLL 檔案必須先安裝在電腦上，再安裝 COM + 應用程式。 或者，您也可以使用 Windows Installer authoring tool，將這些相依檔案新增至「元件服務」系統管理工具所產生的 .msi 檔案。  (請參閱 Windows Installer 檔以取得詳細資料。 ) 

 

## <a name="installing-com-applications-on-other-computers"></a>在其他電腦上安裝 COM + 應用程式

[元件服務] 系統管理工具所產生的 Windows Installer ( .msi) 檔，可用來將 COM + 應用程式安裝在另一部電腦上。 包含 COM + 應用程式的 .msi 檔案只能安裝在支援 COM + 服務的電腦上。 如需部署 COM + 應用程式的詳細程式，請參閱元件服務管理說明中的「安裝 COM + 應用程式」。

除非使用 Windows Installer authoring tool 修改 .msi 檔案，否則使用 Windows Installer 安裝的 COM + 應用程式會出現在 [新增/移除程式] 控制台中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[部署應用程式 proxy](deploying-application-proxies.md)
</dt> <dt>

[COM + 類別目錄](the-com--catalog.md)
</dt> </dl>

 

 



