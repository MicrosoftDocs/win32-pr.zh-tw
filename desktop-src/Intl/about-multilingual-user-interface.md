---
description: 多語系消費者介面 (MUI) 是一種技術，可為使用者提供全球化應用程式的當地語系化使用者介面，以及 Windows 作業系統中的使用者介面語言資源管理。
ms.assetid: 1982931c-fce9-418f-a35d-439b7b886fd9
title: 關於多語系消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2971533310878e40049c591ae6537e43aa4f666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985210"
---
# <a name="about-multilingual-user-interface"></a>關於多語系消費者介面

多語系消費者介面 (MUI) 是一種技術，可為使用者提供全球化應用程式的當地語系化使用者介面，以及 Windows 作業系統中的使用者介面語言資源管理。 提供支援，可將 MUI 功能新增至全球化應用程式，以在 Windows Vista 和更新版本上執行，以及許多 Windows Vista 之前的作業系統。 MUI 當地語系化和資源管理模型可增強對全球化軟體的開發、測試和支援。

MUI 技術的功能包括：

-   簡化軟體當地語系化的語言管理。 MUI 允許根據使用者喜好設定，將作業系統的語言設定變更為支援的語言。
-   以語言資源檔中的應用程式程式碼二進位檔分割為基礎的創新資源技術。 您可以新增其他語言的資源，而不需要重新編譯或重新連結您的應用程式。 其他當地語系化的資源會變成選用的增益集。
-    (API) 的完整應用程式設計介面。 Windows Vista 和更新版本會公開 MUI API，供您用來將 MUI 功能新增至全球化應用程式。 語言管理功能可讓您的應用程式支援各種不同的使用者介面語言。 此 API 也包含資源載入功能，可讓資源載入器載入 Windows Vista 和更新版本的資源，以及 Windows Vista 之前的作業系統。
-   一組語言套件管理工具，可在國際部署映射管理中提供彈性。 這些工具並非以開發人員為目標，因此不會涵蓋在 SDK 中。 如需詳細資訊，請參閱 Technet 上提供的 Windows 自動化安裝套件。

MUI 最明顯的優點是，多個使用者可以共用相同的工作站，並以不同的語言來查看使用者介面。 公司和 Oem 將受益于使用單一安裝來推出、支援及維護多語系映射所需的功能。 但是，MUI 的主要優點是開發、建立及服務應用程式時所獲得的效率。 您可以提供一個適用于所有平臺的核心功能二進位檔，其與 UI 語言無關，可大幅減少開發和測試工作。 如果您必須發行更新或 service pack，則會套用至所有支援的語言，而不需要額外的工程工作。 後續對其他語言的支援會成為當地語系化專案，而不是完整的軟體發展專案。

本節包含下列主題：

-   [瞭解 MUI](understanding-mui.md)
-   [MUI 的可用性](availability-of-mui.md)
-   [MUI 資源管理](mui-resource-management.md)
-   [消費者介面語言管理](user-interface-language-management.md)
-   [開發 MUI 應用程式](development-of-mui-applications.md)
-   [應用程式部署](application-deployment.md)

 

 



