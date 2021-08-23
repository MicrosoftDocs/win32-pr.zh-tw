---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows媒體格式 SDK，設定檔
- Advanced Systems Format (ASF) ，設定檔
- ASF (Advanced Systems Format) ，設定檔
- Windows媒體格式 SDK，prx 檔案
- Advanced Systems Format (ASF) prx 檔案
- ASF (Advanced Systems Format) ，prx files
- Windows媒體格式 SDK，設定檔編輯器
- Advanced Systems Format (ASF) ，設定檔編輯器
- ASF (Advanced 系統格式) ，設定檔編輯器
- prx 檔案
- prx 檔案
- 設定檔編輯器
- Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a89c06f031c9cf8214888efb35f2986135f88207fc94a631e1e111c94ce16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707410"
---
# <a name="profiles"></a>Profiles

設定檔是描述 ASF 檔案設定的資料集合。 設定檔至少必須包含單一資料流程的設定。

設定檔中的資料流程資訊包含資料流程的位元速率、緩衝區視窗和媒體屬性。 音訊和影片的串流資訊會完全描述檔案中的媒體設定方式，包括在使用任何) 來壓縮資料時 (的編解碼器。

設定檔也包含各種 ASF 檔案功能的相關資訊，這些功能將用於以它建立的檔案。 這些包括 [互斥](mutual-exclusion.md)、 [串流優先順序](stream-prioritization.md)、 [頻寬共用](bandwidth-sharing.md)和 [資料單位延伸](data-unit-extensions.md)。

舊版 Windows 媒體格式 SDK 提供預先設定的系統設定檔，可用來建立一般類型的檔案，或稍微改變以符合您應用程式的需求。 Windows Media 9 系列編解碼器不支援系統設定檔。 這是因為「一般」檔案類型的數目隨著新功能的增加而以指數方式成長。 預期幾乎每個內容建立者都需要超越系統設定檔所提供的簡單解決方案。 您仍然可以使用舊的系統設定檔作為起點。 如需詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。

您必須為寫入器提供每個檔案的設定檔。 您可以藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)來指定要搭配寫入器使用的設定檔。

設定檔資料有數種不同的形式，可供 Windows 媒體格式 SDK 使用。 您也可以透過數種方式來存取設定檔資訊。 這可能會對設定檔及其使用方式造成混淆。

下圖顯示如何在 SDK 中使用設定檔資料。

![顯示設定檔資訊流程的圖表。](images/formatsdk01.png)

設定檔資料採用三種不同的形式：包含在應用程式中的設定檔物件內的資料、在磁片上的 XML 檔案，以及 ASF 檔案標頭中的資料。 這兩種形式的資料會顯示為圖表中的陰影矩形。

## <a name="data-in-a-profile-object"></a>設定檔物件中的資料

當您編輯設定檔時，您會使用設定檔物件，該物件會封裝所有的設定檔資料。 您可以使用 [配置檔案管理員] 物件來建立空白的設定檔物件。 您也可以使用配置檔案管理員物件，將現有的設定檔資料載入至設定檔物件。

大部分的設定檔資料都必須透過使用代表設定檔個別部分的物件來新增和操作。 這些包括串流設定物件、相互排除物件、頻寬共用物件，以及資料流程優先順序物件。 您可以使用設定檔物件中的方法來建立每個物件類型。 除非您使用設定檔物件中的方法，以包含來自其他物件的更新資料，否則對這些物件進行變更並不會影響設定檔物件。

## <a name="data-in-an-xml-file"></a>XML 檔案中的資料

設定檔資料會以 XML 檔案的形式儲存在磁片上，其副檔名為 prx。 Windows 媒體格式 SDK 隨附的設定檔集合，稱為系統設定檔，其中涵蓋最常見的 ASF 檔類型。 系統設定檔會儲存在名為 WMSysPr9. prx 的檔案中。  (請注意，此檔案實際上不包含 Windows Media 9 系列的系統設定檔，因為系統設定檔的概念已不再使用 ) 。當您儲存自己的自訂設定檔時，您必須將它們儲存到您自己的檔案中。

您可以使用 [配置檔案管理員] 物件，將設定檔物件的資料儲存至 XML 文字字串。 然後，您可以使用任何您想要的檔案 i/o 功能，將字串儲存到磁片上的檔案中。

## <a name="data-in-the-header-of-an-asf-file"></a>ASF 檔案標頭中的資料

寫入器會取得設定檔中的資訊，並使用它來建立資料流程，以進入 ASF 檔案的資料區段。 寫入檔案時，大量的設定檔資料會儲存在檔案的標頭區段中。 在播放時，[讀取器] 物件 (或同步讀取器物件) 可以存取檔案標頭中的資訊。 在此情況下，讀取物件會建立設定檔物件，並在其中填入標頭中的資料。

當您使用讀取器 (或同步讀取器) 來存取設定檔資料時，可以變更設定檔資訊，但無法在讀取器中將這些變更套用至檔案。 您可以將讀取器檔案中的設定檔資訊套用至寫入器中的設定檔，以建立新檔案，其設定與讀取器中的檔案相同。 在此情況下，您對設定檔中的設定檔資訊進行的任何變更，都會反映在寫入器所註冊的設定檔資訊中。

## <a name="using-profile-editor"></a>使用設定檔編輯器

與其使用 Windows 媒體格式 SDK 來建立設定檔，您可以使用設定檔編輯器（Windows 媒體編碼器隨附的公用程式），而不是使用媒體格式 SDK 來建立設定檔。 在您的編碼應用程式中，使用 **IWMProfileManager：： LoadProfileByData** 方法載入儲存的設定檔。 在某些情況下，例如，如果您使用永遠不會動態修改的有限設定檔數目，使用設定檔編輯器來建立您的設定檔可能會更方便。

但是，如果您使用設定檔編輯器，建議您不要使用 [影片大小：與影片輸入相同] 設定。 核取此核取方塊時，[設定檔編輯器] 會建立一個設定檔，其中的影片輸出高度和寬度設定為零。 當 Windows 媒體編碼器遇到這些設定檔時，會設定正確的值以符合其影片輸入。 不過，Windows 媒體格式 SDK 中的寫入器不會自動執行這項作業，因此您必須確保應用程式在設定檔沒有任何情況下，設定影片框架大小。

**注意** 部分串流設定專案不會儲存在設定檔中。 設定檔中的資料會描述已完成之 ASF 檔案的格式。 寫入器物件用來設定編解碼器的輸入媒體屬性和其他設定資料，不會儲存在設定檔中。 這包括使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法設定的所有屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**頻寬共用物件**](bandwidth-sharing-object.md)
</dt> <dt>

[**概念**](concepts.md)
</dt> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**相互排除物件**](mutual-exclusion-object.md)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> <dt>

[**串流設定物件**](stream-configuration-object.md)
</dt> <dt>

[**串流優先順序物件**](stream-prioritization-object.md)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




