---
description: 因為安裝套件可以包含組成應用程式的檔案，以及其安裝所需的資訊，所以 Windows Installer 可以用來更新應用程式。
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: 修補和升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cee185461ac14c8eac336a5af0c1315eb5e027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944296"
---
# <a name="patching-and-upgrades"></a>修補和升級

因為安裝套件可以包含組成應用程式的檔案，以及其安裝所需的資訊，所以 Windows Installer 可以用來更新應用程式。 安裝程式可以更新安裝套件的下列部分中的資訊：

-   .Msi 檔案。
-   應用程式的檔案。
-   Windows Installer 的註冊資訊。

更新的類型可以是更新對應用程式產品代碼、產品版本和封裝程式碼所進行的變更。 應用程式的產品版本會儲存在 [**ProductVersion**](productversion.md) 屬性中。 應用程式的產品代碼會儲存在 [ [**ProductCode**](productcode.md) ] 屬性中。 應用程式的 [封裝程式碼](package-codes.md) 會儲存在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中。

變更應用程式的 [**ProductCode**](productcode.md) 需要將應用程式變更為另一個產品的更新。 如需哪些更新需要變更 **ProductCode** 的詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md)。 如果未來的應用程式版本需要區分目前產品的更新版本和 nonupdated 版本，則更新可能會變更 [**ProductVersion**](productversion.md) ，並讓 **ProductCode** 保持不變。 [封裝程式碼](package-codes.md)可唯一識別安裝套件，而且每當更新或升級變更安裝套件中的任何資訊時，都應該一律變更。

決定是否要變更產品版本時，您應該考慮未來的應用程式版本是否需要區分目前產品的更新版本與 nonupdated 版本。 為了確保未來的差異，應使用 [次要升級](minor-upgrades.md) ，而不是 [小型更新](small-updates.md)。

-   如果更新變更 .msi 檔案和應用程式檔，但是未變更 [ [**ProductCode**](productcode.md) ] 屬性或 [ [**ProductVersion**](productversion.md) ] 屬性，則稱為「 [小型更新](small-updates.md)」。
-   如果更新變更了 [**ProductVersion**](productversion.md)，但是未變更 [**ProductCode**](productcode.md)，則稱為「 [次要升級](minor-upgrades.md)」。
-   如果更新將安裝變更為完全不同的產品，則必須變更 [**ProductCode**](productcode.md) ，更新也稱為 [主要升級](major-upgrades.md)。

> [!Note]  
> 為了確保未來的產品版本有差異，應該使用 [次要升級](minor-upgrades.md) ，而不是 [小型更新](small-updates.md)。

 

下表摘要說明不同類型的更新。



| 更新類型                       | Productcode | ProductVersion | Description                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Small Update](small-updates.md)    | 沒有變更   | 沒有變更      | 對一或多個太小的檔案進行更新，以保證無法變更 [**ProductVersion**](productversion.md)。 [**修訂編號摘要**](revision-number-summary.md)屬性中的封裝程式碼確實有變更。 可以作為完整的安裝套件或 [修補套件](patch-packages.md)來傳送。 |
| [次要升級](minor-upgrades.md)  | 沒有變更   | 已變更        | 這項小更新大幅改變，足以保證變更 [**ProductVersion**](productversion.md) 屬性。 可以作為完整的安裝套件或 [修補套件](patch-packages.md)來傳送。                                                                                                |
| [主要升級](major-upgrades.md) | 已變更     | 已變更        | 產品的完整更新會 warranting [ [**ProductCode**](productcode.md) ] 屬性中的變更。 隨附于 [修補套件](patch-packages.md) 或完整產品安裝套件。                                                                                                             |



 

> [!Note]  
> Windows Installer 可以為電腦的所有使用者安裝應用程式或更新 (個別電腦內容) 或特定使用者 (個別使用者內容) 根據使用者的存取權限、 [**ALLUSERS**](allusers.md) 屬性的值和作業系統的版本而定，。 應用程式開發人員應該考慮將會安裝內容更新。 如果應用程式和更新的內容不同，則應用程式可能不會如預期般更新。

 

使用者可以重新安裝應用程式的 Windows Installer 套件，以更新應用程式。 請注意， [次要升級](minor-upgrades.md) 的套用方式與 [小型更新](small-updates.md)相同。 如需重新安裝應用程式以更新應用程式的詳細資訊，請參閱下列各節：

-   [重新安裝產品以套用小型更新](applying-small-updates-by-reinstalling-the-product.md)
-   [藉由安裝產品來套用主要升級](applying-major-upgrades-by-installing-the-product.md)

您可以將應用程式更新提供給使用者，以做為 Windows Installer patch 套件。 修補程式可包含整個檔案，或只包含更新部分檔案所需的檔案位。 這表示使用者可以下載的升級修補程式遠小於整個產品，並且可透過升級保留使用者自訂。 請注意， [次要升級](minor-upgrades.md) 的套用方式與 [小型更新](small-updates.md)相同。 如需有關使用修補程式更新應用程式的詳細資訊，請參閱下列各節：

-   [修補](patching.md)
-   [建立小型更新修補程式](creating-a-small-update-patch.md)
-   [藉由修補產品的本機安裝來套用小型更新](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [藉由修補系統管理映射來套用小型更新](applying-small-updates-by-patching-an-administrative-image.md)
-   [藉由修補產品的本機安裝來套用主要升級](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



