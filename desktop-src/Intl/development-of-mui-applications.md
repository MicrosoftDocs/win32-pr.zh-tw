---
description: 本主題摘要說明在您的應用程式中加入 MUI 功能時，要牢記在心的主要程式設計考慮。
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: 開發 MUI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851816"
---
# <a name="development-of-mui-applications"></a>開發 MUI 應用程式

本主題摘要說明在您的應用程式中加入 MUI 功能時，要牢記在心的主要程式設計考慮。

## <a name="requirements-for-a-mui-application"></a>MUI 應用程式的需求

MUI 功能只適用于完整全球化應用程式的當地語系化，使用稱為軟體國際化的程式建立。 Microsoft [Go 全球開發人員中心](https://msdn.microsoft.com/goglobal) 提供廣泛的相關檔，可協助您設計、建立及部署可供使用的全球應用程式。 這些檔可協助您考慮不同人類語言的特性如何影響您的軟體設計。 請注意，入口網站也會提供 Dr. 國際資料行的完整保存。

您的 MUI 應用程式可以在任何語言或地區設定下執行，而且使用者可以要求應用程式包含支援的任何語言。 因此，應用程式必須將使用者介面文字編碼，以支援最廣泛的可能各種語言。 最重要的一點是使用 [Unicode](unicode.md) 來處理所有文字處理。 如需使用 Unicode 進行全球化的詳細資訊，請參閱 Microsoft [Go 全球開發人員中心](https://msdn.microsoft.com/goglobal)。

## <a name="supported-programming-environments"></a>支援的程式設計環境

您可以依照此 SDK 所述，將 MUI 功能新增至全球化的 Win32 forms 應用程式或主控台應用程式。 此外，您可以使用與 MUI 相容的 .NET Framework 來建立受控應用程式。 如需詳細資訊，請參閱 [.Net 開發](/previous-versions/ff361664(v=vs.100))。

## <a name="user-interface-language-settings"></a>消費者介面語言設定

在規劃 MUI 應用程式時，您必須先決定使用者介面的語言，以及將它們呈現給使用者的方式。 應用程式可透過下列其中一種方式支援語言：

-   遵循系統語言設定。 假設使用者慣用的 UI 語言和系統慣用的 UI 語言（結合在一起）表示使用者可用的語言。 使用資源載入器的回溯機制來選擇語言。
-   建立應用程式特定的語言設定。 支援特定語言，並向使用者呈現選取機制。

## <a name="resource-creation"></a>資源建立

本節說明為應用程式建立使用者介面語言資源的可能性。 如需詳細資訊，請參閱 [準備資源](preparing-resources.md)。

> [!Note]  
> 在 Windows Vista 之前版本的作業系統上，您通常會以可執行檔中包含的資源區段所支援的語言，建立靜態和個別封裝的單一語言當地語系化應用程式。 這種類型的實大部分已淘汰，建議您選擇本節中所述的其他資源建立技巧，以支援 Windows Vista 和更新版本。 然後，您可以使用 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)，在 Windows Vista 之前的作業系統上執行此應用程式。

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>使用資源 DLL 中的單一語言 (MUI 資源技術) 

許多 Microsoft 應用程式都會使用標準的附屬 DLL 資源實作為。 在此情況下，會針對 MUI 應用程式使用核心可執行檔，並為每個支援的語言建立一個資源 DLL。 使用附屬 DLL 適用于在任何 Windows 作業系統上執行的應用程式。 如 [Mui 資源管理](mui-resource-management.md)中所述，mui 資源技術支援標準附屬 DLL 執行的變化。

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>在資源 DLL 中使用多種語言

您可以選擇為您的 MUI 應用程式建立一個核心可執行檔，並為與支援語言相關聯的資源建立一個資源 DLL。 相同資源識別碼的複本會在基礎語言資源檔中定義 ( .rc 延伸模組) 在所有支援語言的不同語言標記下。

### <a name="use-of-an-application-specific-resource-mechanism"></a>使用 Application-Specific 資源機制

您可以規劃 MUI 應用程式以使用自訂的資源機制。 在此情況下，應用程式會以特殊方式處理其資源載入。

## <a name="resource-localization"></a>資源當地語系化

若要支援 MUI 應用程式的使用者介面語言，您必須將語言資源當地語系化。 MUI 支援兩種類型的當地語系化，如下表所述。



| 當地語系化類型       | Description                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 預先建立當地語系化  | 在建立應用程式和特定語言的資源之前，先要求當地語系化。 針對每個支援的語言，會針對支援的使用者介面語言複製並重新命名基底語言資源檔，並視需要將這些複本提供給當地語系化人員。 |
| 組建後當地語系化 | 建立應用程式的可執行檔和資源 DLL 之後，要求當地語系化。 在此情況下，會將資源 DLL 的複本提供給每個當地語系化人員。                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多語系消費者介面](about-multilingual-user-interface.md)
</dt> </dl>

 

 
