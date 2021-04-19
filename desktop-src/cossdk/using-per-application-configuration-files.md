---
description: 使用 Per-Application 設定檔
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: 使用 Per-Application 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970104"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="cf3bc-103">使用 Per-Application 設定檔</span><span class="sxs-lookup"><span data-stu-id="cf3bc-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="cf3bc-104">使用 COM + 的每個應用程式佈建檔需要下列基本步驟：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="cf3bc-105">設定 COM + 應用程式的應用程式根目錄。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="cf3bc-106">在 COM + 應用程式根目錄中建立應用程式資訊清單和 application.config 檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="cf3bc-107">從 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 開始，每個應用程式佈建檔案都可供使用。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="cf3bc-108">**使用每個應用程式佈建檔**</span><span class="sxs-lookup"><span data-stu-id="cf3bc-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="cf3bc-109">建立 .NET 類別庫，其中包含 System.enterpriseservices 元件的參考。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="cf3bc-110">類別庫應包含下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-110">The class library should contain the following code:</span></span>

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

    

    <span data-ttu-id="cf3bc-111">請注意，"ConfigData1" 是範例設定名稱。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="cf3bc-112">您可以使用您選擇的設定名稱來取代此項。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="cf3bc-113">建立空的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-113">Create an empty COM+ application.</span></span> <span data-ttu-id="cf3bc-114">如需如何進行此動作的指示，請參閱 [建立新的 COM + 應用程式](creating-a-new-com--application.md)。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="cf3bc-115">將您建立的類別庫安裝至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="cf3bc-116">如需如何進行此動作的指示，請參閱 [安裝新元件](installing-new-components.md)。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="cf3bc-117">在 [元件服務] 系統管理工具中，以滑鼠右鍵按一下您建立的 COM + 應用程式，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="cf3bc-118">在 [ **屬性** ] 對話方塊中，選取 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="cf3bc-119">請確定 **啟用類型** 已設為 [ **伺服器應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="cf3bc-120">在 [ **應用程式根目錄** ] 文字方塊中，輸入路徑或流覽至您要儲存此應用程式之應用程式佈建檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="cf3bc-121">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-121">Click **OK**.</span></span>

    <span data-ttu-id="cf3bc-122">請注意，您也可以透過 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別的 ApplicationDirectory 屬性來指定 com + 應用程式根目錄。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="cf3bc-123">如需詳細資訊，請參閱 [**應用程式**](applications.md)。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="cf3bc-124">在您選擇用來儲存應用程式佈建檔的目錄中，建立名為 *application* 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="cf3bc-125">使用文字編輯器，將下列文字新增至此檔案：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="cf3bc-126">在相同的目錄中， *建立名為* app.config 的檔案。使用文字編輯器，將下列文字新增至此檔案：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="cf3bc-127">請注意，此設定檔只是一個範例。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="cf3bc-128">您可以使用不同的名稱和值來建立多個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="cf3bc-129">不過請注意，"ConfigData1" 會與稍早建立的類別庫中所使用的設定名稱相符。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="cf3bc-130">建立 .NET 主控台應用程式，並參考您稍早建立的 .NET 類別庫，以及 System.enterpriseservices 元件的參考。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="cf3bc-131">主控台應用程式應包含下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-131">The console application should contain the following code:</span></span>
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

    

<span data-ttu-id="cf3bc-132">執行主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf3bc-132">Run the console application.</span></span> <span data-ttu-id="cf3bc-133">輸出應該是：</span><span class="sxs-lookup"><span data-stu-id="cf3bc-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



