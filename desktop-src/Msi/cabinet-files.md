---
description: 封包是單一檔案（通常副檔名為 .cab），可將壓縮檔案儲存在檔案庫中。
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: 封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996698"
---
# <a name="cabinet-files"></a>封包檔

封包是單一檔案（通常副檔名為 .cab），可將壓縮檔案儲存在檔案庫中。 封包格式是封裝多個檔案的有效方式，因為壓縮會跨檔案界限執行，如此可大幅改善壓縮率。

開發人員可以使用封包檔建立工具（例如 Makecab.exe）製作封包檔，以與安裝程式套件搭配使用。 Makecab.exe 公用程式包含在 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。

開發人員也可以使用封包檔建立工具（例如 Cabarc.exe）製作封包檔，以與安裝程式套件搭配使用。 此工具會寫入鑽石封包結構。

封包檔內儲存之檔案的檔案索引鍵必須與檔案 [資料表](file-table.md) 的 file 資料行中的專案相符，而且封包中的檔案順序必須符合 [順序] 資料行中指定的檔案順序。 如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

大型檔案可以分割成兩個或多個封包檔。 在下一個封包檔中，任何一個封包檔中都不能有15個以上的檔案。 例如，如果您有三個封包檔，則第一個封包可以有15個檔案跨越第二個封包檔，而第二個封包檔可以有15個檔案跨越第三封封包檔。

安裝程式會根據安裝所需的封包解壓縮檔案，並依照儲存在封包檔中的相同順序來安裝檔案。 安裝封包中儲存之檔案的空間需求與安裝未壓縮檔案的空間需求不同。

封包檔可以位於 .msi 檔案的內部或外部。 從在 Windows 7 或 Windows Server 2008 R2 上執行的 Windows Installer 5.0 開始，安裝程式會先儲存任何內嵌在 .msi 檔案中的封包，再快取安裝套件。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 為了節省磁碟空間，安裝程式一律會移除任何內嵌在 .msi 檔案中的封包，然後才在使用者的電腦上快取安裝套件。

 

 



