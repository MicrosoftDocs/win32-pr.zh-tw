---
description: 使用 Per-Application 設定檔
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: 使用 Per-Application 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbc38a2433d2da6d2a39985523a5ebffd0d971102bc883e44ae24d9fcc165ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372338"
---
# <a name="using-per-application-configuration-files"></a>使用 Per-Application 設定檔

使用 COM + 的每個應用程式佈建檔需要下列基本步驟：

-   設定 COM + 應用程式的應用程式根目錄。
-   在 COM + 應用程式根目錄中建立應用程式資訊清單和 application.config 檔案。

> [!Note]  
> 從 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 開始，每個應用程式佈建檔案都可供使用。

 

**使用每個應用程式佈建檔**

1.  建立 .NET 類別庫，其中包含 System.enterpriseservices 元件的參考。

2.  類別庫應包含下列程式碼：

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    請注意，"ConfigData1" 是範例設定名稱。 您可以使用您選擇的設定名稱來取代此項。

3.  建立空的 COM + 應用程式。 如需如何進行此動作的指示，請參閱 [建立新的 COM + 應用程式](creating-a-new-com--application.md)。
4.  將您建立的類別庫安裝至 COM + 應用程式。 如需如何進行此動作的指示，請參閱 [安裝新元件](installing-new-components.md)。
5.  在 [元件服務] 系統管理工具中，以滑鼠右鍵按一下您建立的 COM + 應用程式，然後選取 [ **屬性**]。
6.  在 [ **屬性** ] 對話方塊中，選取 [ **啟用** ] 索引標籤。
7.  請確定 **啟用類型** 已設為 [ **伺服器應用程式**]。
8.  在 [ **應用程式根目錄** ] 文字方塊中，輸入路徑或流覽至您要儲存此應用程式之應用程式佈建檔的目錄。
9.  按一下 [確定]。

    請注意，您也可以透過 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別的 ApplicationDirectory 屬性來指定 com + 應用程式根目錄。 如需詳細資訊，請參閱 [**應用程式**](applications.md)。

10. 在您選擇用來儲存應用程式佈建檔的目錄中，建立名為 *application* 的檔案名。 使用文字編輯器，將下列文字新增至此檔案：

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. 在相同的目錄中，建立名為 *application*.config 的檔案。使用文字編輯器，將下列文字新增至此檔案：

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    請注意，此設定檔只是一個範例。 您可以使用不同的名稱和值來建立多個索引鍵。 不過請注意，"ConfigData1" 會與稍早建立的類別庫中所使用的設定名稱相符。

12. 建立 .NET 主控台應用程式，並參考您稍早建立的 .NET 類別庫，以及 System.enterpriseservices 元件的參考。
13. 主控台應用程式應包含下列程式碼：
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

執行主控台應用程式。 輸出應該是：

``` syntax
Configuration Data Number 1
```

 

 



