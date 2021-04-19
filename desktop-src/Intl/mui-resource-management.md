---
description: 您的全球化應用程式必須定義各種使用者介面元素，例如功能表、對話方塊、說明字串，以及其他以當地語系化資源表示的專案。
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: MUI 資源管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000257"
---
# <a name="mui-resource-management"></a><span data-ttu-id="90845-103">MUI 資源管理</span><span class="sxs-lookup"><span data-stu-id="90845-103">MUI Resource Management</span></span>

<span data-ttu-id="90845-104">您的全球化應用程式必須定義各種使用者介面元素，例如功能表、對話方塊、說明字串，以及其他以當地語系化資源表示的專案。</span><span class="sxs-lookup"><span data-stu-id="90845-104">Your globalized application must define a variety of user interface elements, such as menus, dialog boxes, help strings, and other items, represented as localized resources.</span></span> <span data-ttu-id="90845-105">使用者介面語言會成為應用程式的其中一個設定。</span><span class="sxs-lookup"><span data-stu-id="90845-105">The user interface language becomes one of the settings for the application.</span></span> <span data-ttu-id="90845-106">本節說明 MUI 資源技術，我們建議您使用這些資源技術來建立您的應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="90845-106">This section describes the MUI resource technology, which we recommend that you use for creating your application resources.</span></span>

## <a name="features-of-the-mui-resource-technology"></a><span data-ttu-id="90845-107">MUI 資源技術的功能</span><span class="sxs-lookup"><span data-stu-id="90845-107">Features of the MUI Resource Technology</span></span>

<span data-ttu-id="90845-108">在 Windows Vista 和更新版本中公開的 MUI 資源技術具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="90845-108">The MUI resource technology, exposed in Windows Vista and later, has the following characteristics:</span></span>

-   <span data-ttu-id="90845-109">特定語言的資源檔會與應用程式程式碼二進位檔分開儲存，因此程式碼變更不會影響資源。</span><span class="sxs-lookup"><span data-stu-id="90845-109">Language-specific resource files are stored separately from the application code binary, so that a code change does not affect the resources.</span></span>
-   <span data-ttu-id="90845-110">多個語言的資源可以部署在單一安裝中，或針對每個語言個別安裝。</span><span class="sxs-lookup"><span data-stu-id="90845-110">The resources for multiple languages can be deployed in a single installation or separate installations for each language.</span></span>
-   <span data-ttu-id="90845-111">資源會根據使用者設定的應用程式語言來載入和顯示。</span><span class="sxs-lookup"><span data-stu-id="90845-111">A resource is loaded and displayed according to the language of the application as set by the user.</span></span>

<span data-ttu-id="90845-112">這項技術會將語言特定檔案中定義的資源與特定版本的語言中性 (LN) 檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="90845-112">This technology associates the resources defined in language-specific files with a particular version of a language-neutral (LN) file.</span></span> <span data-ttu-id="90845-113">LN 檔案是 Win32 PE 檔案，代表應用程式程式碼二進位檔和非語言相關的資源。</span><span class="sxs-lookup"><span data-stu-id="90845-113">The LN file is a Win32 PE file representing the application code binary and language-neutral resources.</span></span> <span data-ttu-id="90845-114">檔案的關聯會使用反映在所有相關聯檔案所含之資源設定資料中的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="90845-114">Association of files uses a checksum reflected in resource configuration data contained in all associated files.</span></span> <span data-ttu-id="90845-115">資源載入器會使用總和檢查碼來確認檔案保存相同版本的必要資源。</span><span class="sxs-lookup"><span data-stu-id="90845-115">The resource loader uses the checksum to verify that the files hold the same version of the required resources.</span></span> <span data-ttu-id="90845-116">它也會以其資料夾名稱驗證語言特定檔案中的語言。</span><span class="sxs-lookup"><span data-stu-id="90845-116">It also validates the language in the language-specific file with its folder name.</span></span> <span data-ttu-id="90845-117">如果未建立適當的關聯，則載入器不會載入資源檔。</span><span class="sxs-lookup"><span data-stu-id="90845-117">The loader does not load a resource file if the appropriate association is not established.</span></span>

<span data-ttu-id="90845-118">具體而言，主要總和檢查碼的計算是從檔案的主要和次要版本號碼，以及檔案名 (區分大小寫的) ，這些都是從版本資源取得的。</span><span class="sxs-lookup"><span data-stu-id="90845-118">Specifically the main checksum is calculated from the major and minor version numbers of a file and the file name (case sensitive), which are obtained from the version resource.</span></span> <span data-ttu-id="90845-119">此總和檢查碼不應該在相同元件的 RTM 和 service pack 版本之間變更。</span><span class="sxs-lookup"><span data-stu-id="90845-119">This checksum should not change between RTM and service pack versions of the same component.</span></span> <span data-ttu-id="90845-120">此外，也會使用服務總和檢查碼來決定要載入之特定語言資源檔的適當版本。</span><span class="sxs-lookup"><span data-stu-id="90845-120">Additionally, a service checksum is used to determine the appropriate version of the language-specific resource file to load.</span></span> <span data-ttu-id="90845-121">此總和檢查碼是根據檔案中可當地語系化的資源來計算。</span><span class="sxs-lookup"><span data-stu-id="90845-121">This checksum is calculated based on the localizable resources in the file.</span></span>

<span data-ttu-id="90845-122">MUI 提供兩個資源公用程式，可供您用來準備應用程式的資源檔。</span><span class="sxs-lookup"><span data-stu-id="90845-122">MUI furnishes two resource utilities that you can use to prepare resource files for your application.</span></span> <span data-ttu-id="90845-123">MUI 專屬公用程式（稱為 MUIRCT）可讓您建立 LN 檔和相關聯的語言特定資源檔。</span><span class="sxs-lookup"><span data-stu-id="90845-123">A MUI-specific utility, called MUIRCT, allows you to build an LN file and associated language-specific resource files.</span></span> <span data-ttu-id="90845-124">在 Windows Vista 和更新版本上，Windows RC 編譯器也已經過修改，可根據 MUI 資源技術來建立這些檔案。</span><span class="sxs-lookup"><span data-stu-id="90845-124">On Windows Vista and later, the Windows RC Compiler has also been modified to build these files according to the MUI resource technology.</span></span> <span data-ttu-id="90845-125">如需這些工具的語法和詳細資料，請參閱 [資源公用程式](resource-utilities.md)。</span><span class="sxs-lookup"><span data-stu-id="90845-125">For syntax and details of these tools, see [Resource Utilities](resource-utilities.md).</span></span>

## <a name="ln-file"></a><span data-ttu-id="90845-126">LN 檔</span><span class="sxs-lookup"><span data-stu-id="90845-126">LN File</span></span>

<span data-ttu-id="90845-127">MUI 應用程式的 LN 檔案包含可執行程式碼和語言中立的資源，這些資源是由應用程式的所有語言版本所共用和安裝。</span><span class="sxs-lookup"><span data-stu-id="90845-127">The LN file for a MUI application contains executable code and language-neutral resources that are shared and installed by all language versions of the application.</span></span>

## <a name="language-specific-resource-file"></a><span data-ttu-id="90845-128">Language-Specific 資源檔</span><span class="sxs-lookup"><span data-stu-id="90845-128">Language-Specific Resource File</span></span>

<span data-ttu-id="90845-129">特定語言的資源檔通常會包含使用者介面字串，以及需要針對特定語言進行當地語系化的其他元素。</span><span class="sxs-lookup"><span data-stu-id="90845-129">A language-specific resource file normally contains user interface strings and other elements that require localization for a particular language.</span></span> <span data-ttu-id="90845-130">您的 MUI 應用程式會針對每個支援的語言使用一個特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="90845-130">Your MUI application uses one language-specific resource file per supported language.</span></span> <span data-ttu-id="90845-131">適用于每個語言專屬資源檔的應用程式的 LN 檔案都相同。</span><span class="sxs-lookup"><span data-stu-id="90845-131">The LN file for the application is the same for each language-specific resource file.</span></span>

<span data-ttu-id="90845-132">使用 MUI 資源技術建立時，語言特定檔案的副檔名為 "mui"，並以下列方式處理：</span><span class="sxs-lookup"><span data-stu-id="90845-132">When built using the MUI resource technology, language-specific files have a ".mui" extension and are handled as follows:</span></span>

-   <span data-ttu-id="90845-133">與指定之 LN 檔案相關聯的特定語言檔案全都共用相同的檔案名，這是藉由將副檔名 ". mui" 新增至完整檔案名 (加上對應之 LN 檔案的副檔名) 來形成相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="90845-133">The language-specific files associated with a given LN file all share the same file name, which is formed by adding the extension ".mui" to the full file name (with extension) of the corresponding LN file.</span></span> <span data-ttu-id="90845-134">例如，名為 "Myfile.dll" 的 LN 檔案包含名為 "Myfile.dll mui" 的語言特定檔案。</span><span class="sxs-lookup"><span data-stu-id="90845-134">For example, an LN file named "Myfile.dll" has language-specific files named "Myfile.dll.mui".</span></span>
-   <span data-ttu-id="90845-135">特定語言的檔案位於包含 LN 檔案之資料夾的子資料夾中。</span><span class="sxs-lookup"><span data-stu-id="90845-135">The language-specific files reside in subfolders of the folder containing the LN file.</span></span> <span data-ttu-id="90845-136">每個資料夾名稱都會反映出語言。</span><span class="sxs-lookup"><span data-stu-id="90845-136">Each folder name reflects the language.</span></span>

## <a name="resource-configuration-data"></a><span data-ttu-id="90845-137">資源設定資料</span><span class="sxs-lookup"><span data-stu-id="90845-137">Resource Configuration Data</span></span>

<span data-ttu-id="90845-138">為了建立 LN 檔案與其語言特定檔案的關聯，MUI 資源技術會使用資源設定資料，包括總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="90845-138">To associate an LN file with its language-specific files, the MUI resource technology uses resource configuration data, including the checksum.</span></span> <span data-ttu-id="90845-139">資源建立程式會將這項資訊放在每個 LN 和語言特定檔案的 RC Config 區段中。</span><span class="sxs-lookup"><span data-stu-id="90845-139">The resource build procedure places this information in an RC Config section of each LN and language-specific file.</span></span> <span data-ttu-id="90845-140">您可以透過 MUIRCT 公用程式取得這項資訊的人們可讀取形式。</span><span class="sxs-lookup"><span data-stu-id="90845-140">A human-readable form of this information is available via the MUIRCT utility.</span></span> <span data-ttu-id="90845-141">如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)。</span><span class="sxs-lookup"><span data-stu-id="90845-141">For more information, see [Resource Utilities](resource-utilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90845-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="90845-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90845-143">關於多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="90845-143">About Multilingual User Interface</span></span>](about-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="90845-144">資源公用程式</span><span class="sxs-lookup"><span data-stu-id="90845-144">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



