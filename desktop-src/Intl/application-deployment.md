---
description: 本節說明部署 MUI 應用程式以達到最佳應用程式載入邏輯和資源載入器使用的考慮。
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: 應用程式部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2023e5fc2dbde51a6ef996126e7557c9ffce8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990505"
---
# <a name="application-deployment"></a>應用程式部署

本節說明部署 MUI 應用程式以達到最佳應用程式載入邏輯和資源載入器使用的考慮。

## <a name="packaging"></a>包裝

應用程式的封裝取決於所提供的語言支援類型，因為 Windows 會根據使用者喜好設定來安裝語言套件。 例如，如果您已決定支援系統語言設定，您可能會想要在單一套件中提供所有語言支援，不論所需的使用者為何。

如果應用程式和資源很大，您應該針對每個支援的語言使用一個套件。 比方說，如果您的應用程式呈現使用者可選取的語言，而且使用者需要動態新增和移除語言資源，您可能會使用此封裝類型。

## <a name="file-placement-on-windows-vista-and-later"></a>Windows Vista 和更新版本上的檔案放置

本節說明以 Windows Vista 和更新版本為目標的 MUI 應用程式檔案放置。

### <a name="place-the-ln-file"></a>放置 LN 檔案

MUI 應用程式的一般 LN 檔是 .exe 檔案或 .dll 檔案，例如 BakerDelta.dll。 您應該將這個檔案放在您的應用程式安裝所在的根資料夾中，例如 X： \\ \\ <somepath> \\BakerDelta.dll。

### <a name="place-language-specific-resource-files"></a>放置 Language-Specific 資源檔

特定語言的資源檔必須具有可預測的名稱，方法是將 "mui" 附加到 LN 檔案的完整名稱，例如 BakerDelta.dll mui。 這些檔案必須放在以適當 [語言名稱](language-names.md)命名的子資料夾中。 下列範例會顯示 BakerDelta.dll LN 檔案的資源位置，以及英文的語言專屬資源檔 (英國) 、英文 (美國) 、中性英文、西班牙文 (西班牙) 、西班牙文 (墨西哥) 和中性西班牙文：

-   X： \\ \\ <somepath> \\BakerDelta.dll
-   X： \\ \\ <somepath> \\ en-us \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ en-us \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ en \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ es \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ es-MX \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ es \\BakerDelta.dll mui

資源檔必須放在安裝 MUI 應用程式或語言套件期間的正確位置。 請務必將每個檔案放在正確的資料夾中，否則資源載入器無法正常運作。 使用上述範例，資源載入器會檢查 X： \\ <somepath> \\ en-us \\BakerDelta.dll 的英文 (美國) 資源。 如果載入器會查看該檔案，而且只會遇到西班牙文語言的資源，則會失敗。

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Windows Vista 前版作業系統上的檔案放置

在 Windows Vista 之前的作業系統上執行的應用程式可以使用 Windows Vista 慣例，將語言特定的資源檔放在以語言名稱為基礎的資料夾中。 或者，應用程式可以符合從 [語言識別項](language-identifiers.md)形成路徑的較舊慣例。 針對僅支援單一語言的應用程式，您可以將特定語言的資源檔放在具有二進位檔案的根目錄中。

例如，假設有一個名為 BakerDelta.dll 的 LN 檔案，其中包含英文 (英國) 的語言特定資源檔、英文 (美國) 、中性英文、西班牙文 (西班牙) 、西班牙文 (墨西哥) 和中性西班牙文。 在 Windows Vista 前版作業系統上安裝可能會將這些檔案放在下面，如下所示：

-   X： \\ \\ <somepath> \\BakerDelta.dll
-   X： \\ \\ <somepath> \\BakerDelta.dll mui (選用的 mui 檔案，其中包含作業系統語言的資源，作為最終的回溯) 
-   X： \\ \\ <somepath> \\ mui \\ 0809 \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ mui \\ 0409 \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ mui \\ 040a \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ mui \\ 080a \\BakerDelta.dll mui
-   X： \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll mui

除了這些檔案之外，應用程式也可以設定絕佳的回溯語言專屬資源檔，與應用程式本身位於相同的資料夾中。 在上述範例中，這個檔案是 X： \\ <somepath> \\BakerDelta.dll 的 mui。

## <a name="installation"></a>安裝

複製和設定應用程式檔的安裝邏輯依賴支援的語言，以及語言資源檔在正確安裝位置的位置。 安裝程式必須安裝並設定應用程式，讓使用者可以輕鬆地新增和移除語言。

如果您的應用程式只安裝目標作業系統的語言，安裝程式必須偵測作業系統使用者介面，以判斷要安裝的應用程式資源。 為了支援最佳的使用者體驗，安裝程式也應該偵測使用者介面語言，為安裝本身提供當地語系化的使用者介面。

建議使用 Windows Installer (MSI) 來建立您的安裝軟體。 相關聯的資源應該包含在基礎語言資源檔中，如 [建立基礎語言資源檔](creating-the-base-language-resource-file.md)中所述。 如需使用 MSI 來準備應用程式安裝程式的指示，請參閱 [Windows Installer](../msi/windows-installer-portal.md)。

## <a name="uninstall-program"></a>卸載程式

您也可能想要使用您的 MUI 應用程式來提供卸載程式。 也建議您建立此程式的 MSI。 如需使用 MSI 準備卸載軟體的指示，請參閱 [Windows Installer](../msi/windows-installer-portal.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多語系消費者介面](using-multilingual-user-interface.md)
</dt> </dl>

 

 
