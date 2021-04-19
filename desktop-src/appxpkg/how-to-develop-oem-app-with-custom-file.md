---
title: 如何開發使用自訂檔案的 OEM 應用程式
description: 瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106966235"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="139e4-103">如何開發使用自訂檔案的 OEM 應用程式</span><span class="sxs-lookup"><span data-stu-id="139e4-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="139e4-104">如需有關建立和使用自訂資料檔案的詳細資訊，請參閱 [DISM 應用程式封裝 ( .appx 或 .appxbundle) 服務 Command-Line 選項](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)。</span><span class="sxs-lookup"><span data-stu-id="139e4-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="139e4-105">瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="139e4-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="139e4-106">針對您針對 OEM 部署所建立的應用程式，您可以使用自訂檔案，將資訊從 OEM 傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="139e4-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="139e4-107">若要將 OEM 資訊傳遞至應用程式，您可以在 microsoft.system] 資料夾中建立自訂的資料檔。</span><span class="sxs-lookup"><span data-stu-id="139e4-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="139e4-108">這個檔案名是作業系統的特殊名稱，會在作業系統更新期間自動繼續執行。</span><span class="sxs-lookup"><span data-stu-id="139e4-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="139e4-109">Oem 可以使用這個檔案來傳入自訂識別碼，讓應用程式知道 Oem 何時部署它們。</span><span class="sxs-lookup"><span data-stu-id="139e4-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="139e4-110">每個應用程式只能有一個自訂的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="139e4-111">應用程式必須能夠正確地尋找和讀取此檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="139e4-112">開發人員將檔案視為不受信任的資料。</span><span class="sxs-lookup"><span data-stu-id="139e4-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="139e4-113">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="139e4-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="139e4-114">技術</span><span class="sxs-lookup"><span data-stu-id="139e4-114">Technologies</span></span>

-   [<span data-ttu-id="139e4-115">快速入門：查詢應用程式套件資訊清單資訊</span><span class="sxs-lookup"><span data-stu-id="139e4-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="139e4-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="139e4-116">Prerequisites</span></span>

-   <span data-ttu-id="139e4-117">您需要 [部署映射服務與管理 (DISM) ](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) 工具來新增應用程式套件與自訂資料檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="139e4-118">指示</span><span class="sxs-lookup"><span data-stu-id="139e4-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="139e4-119">步驟1：建立自訂檔案，並將它新增至封裝元資料檔案夾</span><span class="sxs-lookup"><span data-stu-id="139e4-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="139e4-120">您可以設計應用程式，以使用您為自訂資料選擇的任何格式。</span><span class="sxs-lookup"><span data-stu-id="139e4-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="139e4-121">例如，您可以使用 XML、文字檔或其他檔案類型來組織您的資料。</span><span class="sxs-lookup"><span data-stu-id="139e4-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="139e4-122">建議您考慮如何測試及驗證檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="139e4-123">例如，您可以建立 XML 架構來驗證 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="139e4-124">您可以指定任何類型的檔案，其中包含自訂資料的任何檔案名。</span><span class="sxs-lookup"><span data-stu-id="139e4-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="139e4-125">當您使用 [dism](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) 工具在自訂資料檔中新增應用程式封裝時，DISM 會將自訂檔案重新命名為自訂檔案，並將檔案儲存到 microsoft.system] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="139e4-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="139e4-126">應用程式無法修改自訂資料檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="139e4-127">這是唯讀的資源。</span><span class="sxs-lookup"><span data-stu-id="139e4-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="139e4-128">步驟2：存取應用程式的自訂資料檔案</span><span class="sxs-lookup"><span data-stu-id="139e4-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="139e4-129">您可以從程式碼使用 Windows Api 取得目前封裝的資訊，以存取應用程式的自訂資料檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="139e4-130">例如：</span><span class="sxs-lookup"><span data-stu-id="139e4-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="139e4-131">如需使用 [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) 屬性進行開發的詳細資訊，請參閱 [快速入門：查詢應用程式套件資訊清單資訊](how-to-query-package-identity-information.md)。</span><span class="sxs-lookup"><span data-stu-id="139e4-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="139e4-132">如需有關使用 [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) 存取自訂資料檔以及使用 [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) 物件的詳細資訊，請參閱 [存取資料和](/previous-versions/windows/apps/hh464959(v=win.10))檔案。</span><span class="sxs-lookup"><span data-stu-id="139e4-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="139e4-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="139e4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="139e4-134">快速入門：查詢應用程式套件資訊清單資訊</span><span class="sxs-lookup"><span data-stu-id="139e4-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 