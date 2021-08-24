---
title: 如何開發使用自訂檔案的 OEM 應用程式
description: 瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780e930d057c325038c94dc86fc375c70bdb1cc8dca34ac6169436bc0f0e323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855318"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>如何開發使用自訂檔案的 OEM 應用程式

如需有關建立和使用自訂資料檔案的詳細資訊，請參閱 [DISM 應用程式封裝 ( .appx 或 .appxbundle) 服務 Command-Line 選項](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)。

瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。

針對您針對 OEM 部署所建立的應用程式，您可以使用自訂檔案，將資訊從 OEM 傳遞給應用程式。 若要將 OEM 資訊傳遞至應用程式，您可以在 microsoft.system] 資料夾中建立自訂的資料檔。 這個檔案名是作業系統的特殊名稱，會在作業系統更新期間自動繼續執行。 Oem 可以使用這個檔案來傳入自訂識別碼，讓應用程式知道 Oem 何時部署它們。 每個應用程式只能有一個自訂的資料檔案。 應用程式必須能夠正確地尋找和讀取此檔案。 開發人員將檔案視為不受信任的資料。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [快速入門：查詢應用程式套件資訊清單資訊](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>必要條件

-   您需要 [部署映射服務與管理 (DISM) ](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) 工具來新增應用程式套件與自訂資料檔案。

## <a name="instructions"></a>指示

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>步驟1：建立自訂檔案，並將它新增至封裝元資料檔案夾

您可以設計應用程式，以使用您為自訂資料選擇的任何格式。 例如，您可以使用 XML、文字檔或其他檔案類型來組織您的資料。 建議您考慮如何測試及驗證檔案。 例如，您可以建立 XML 架構來驗證 XML 檔案。

您可以指定任何類型的檔案，其中包含自訂資料的任何檔案名。 當您使用 [dism](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) 工具在自訂資料檔中新增應用程式封裝時，DISM 會將自訂檔案重新命名為自訂檔案，並將檔案儲存到 microsoft.system] 資料夾。

> [!Note]  
> 應用程式無法修改自訂資料檔案。 這是唯讀的資源。

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>步驟2：存取應用程式的自訂資料檔案

您可以使用 Windows api 取得目前封裝的資訊，從程式碼存取應用程式的自訂資料檔。 例如：

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

如需使用 [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) 屬性進行開發的詳細資訊，請參閱 [快速入門：查詢應用程式套件資訊清單資訊](how-to-query-package-identity-information.md)。

如需有關使用 [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) 存取自訂資料檔以及使用 [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) 物件的詳細資訊，請參閱 [存取資料和](/previous-versions/windows/apps/hh464959(v=win.10))檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門：查詢應用程式套件資訊清單資訊](how-to-query-package-identity-information.md)
</dt> </dl>

 

 