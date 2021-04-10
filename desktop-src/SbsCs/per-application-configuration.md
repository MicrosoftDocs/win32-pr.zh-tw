---
description: 每個應用程式設定會將特定應用程式的相依性，從並存元件的某個版本重新導向至元件的另一個版本。
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: 每個應用程式設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194539"
---
# <a name="per-application-configuration"></a>每個應用程式設定

每個應用程式設定會將特定應用程式的相依性，從並存元件的某個版本重新導向至元件的另一個版本。 如果特定應用程式的正確作業需要的元件版本與通常指定為 [預設](default-configuration.md) 設定或 [發行者](publisher-configuration.md)設定的版本不同，則可能會需要個別應用程式設定。 例如，發行者的元件版本全域更新可能會修正元件，但會中斷這個特定的應用程式。 在此情況下，每個應用程式的設定可能會用來讓應用程式繼續以先前的元件版本執行。

從 Windows Server 2003 開始，每個應用程式設定一律會以個別應用程式為基礎覆寫 [預設](default-configuration.md) 設定。 只有當 [應用程式佈建檔](application-configuration-files.md)在 **>publisherpolicy** 中指定 *apply = "No"* ，且應用程式相容性資料庫中有對應的專案時，每個應用程式設定才會覆寫每個應用程式的 [發行者](publisher-configuration.md)設定。

> [!Note]  
> 在 Windows XP 中，每個應用程式設定會以個別應用程式為基礎覆寫 [預設](default-configuration.md) 設定和 [發行者](publisher-configuration.md) 設定。 如需詳細資訊，請參閱 [WINDOWS XP 上的每個應用程式](per-application-configuration-on-windows-xp.md)設定。

 

從 Windows Server 2003 開始，如果 [應用程式佈建檔](application-configuration-files.md)在 **>publisherpolicy** 中指定 *apply = "yes"* ，且已針對應用程式相容性資料庫中的應用程式設定 EnableAppConfig 旗標，則每個應用程式的設定將會覆寫 [發行者](publisher-configuration.md)設定。 使用每一應用程式設定覆寫發行者設定的這項功能，可讓應用程式在安全模式中執行。 如需有關應用程式相容性資料庫和安全模式的詳細資訊，請參閱 Windows 應用程式相容性工具組。 您可以從取得 Windows 應用程式相容性工具組 [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) 。

> [!Note]  
> 如果您使用 [應用程式佈建檔](application-configuration-files.md)來傳送元件 ( .config 檔案) 在 **>publisherpolicy** 中指定 *apply = "no"* ，這會導致產生啟用內容失敗。 如果您在 **>publisherpolicy** 中以指定 *apply = "yes"* 的 .config 檔案傳送元件，則會忽略每個應用程式的設定。

 

應用程式系統管理員可以撰寫和安裝應用程式佈建檔，並更新應用程式相容性資料庫，以執行每個應用程式的設定。 然後，應用程式佈建檔應該部署並安裝到與應用程式可執行檔相同的資料夾中。 如需檔案架構的清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。 應用程式相容性資料庫必須依照應用程式相容性工具組中的說明進行散發。

> [!Note]  
> 如果您的應用程式在安全模式中執行，它將不會收到任何重要的安全性修正或錯誤修正。元件的發行者可能會以發行者設定檔的形式發行。 因此，使用每個應用程式設定的應用程式可能會維持不安全，或即使在具有這些修正程式的新元件套用至系統之後仍無法正常運作。 基於這個理由，應用程式開發人員絕對不應該使用每個應用程式的設定來傳送應用程式。 只有在發行者設定中斷應用程式時，公司系統管理員才能使用每個應用程式設定做為暫時的修正程式。 在此情況下，永久的解決方案是元件的開發人員和應用程式開發人員必須共同合作，以確保具有發行者設定的元件能完全回溯相容。

 

以下是應用程式佈建檔的範例。 如需詳細資訊，請參閱應用程式佈建檔。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

應用程式系統管理員應該將必要的專案加入至應用程式相容性資料庫。 從下載並安裝 Windows 應用程式相容性工具組 2.6 [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) 。 使用此工具組中所述的相容性系統管理員，建立新的自訂或更新現有的資料庫。 您想要為應用程式的相容性層級選擇的相容性修正程式是 EnableAppConfig。 您必須一律先測試應用程式，再安裝新的相容性資料庫。

 

 



