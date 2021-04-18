---
description: 示範如何註冊為同步根提供者，並將雲端存放裝置提供者整合至流覽窗格的根層級。
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: 整合雲端存放裝置提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21fdc5abfbf9881bfe23b00a924fce989aec7c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564631"
---
# <a name="integrate-a-cloud-storage-provider"></a><span data-ttu-id="be038-103">整合雲端存放裝置提供者</span><span class="sxs-lookup"><span data-stu-id="be038-103">Integrate a Cloud Storage Provider</span></span>

<span data-ttu-id="be038-104">當您有雲端存放裝置提供者時，您必須採取幾個步驟，才能為使用者提供一致且慣用的體驗。</span><span class="sxs-lookup"><span data-stu-id="be038-104">When you have a cloud storage provider, there are a couple of steps you should take in order to provide a consistent and preferred experience for the user.</span></span> <span data-ttu-id="be038-105">這兩個專案會註冊為同步根提供者，並將您的應用程式整合到流覽窗格的根層級中。</span><span class="sxs-lookup"><span data-stu-id="be038-105">These two things are registering as a sync root provider and integrating your application into the root level of the Navigation Pane.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be038-106">從 Windows 10 開始，才支援整合雲端存放裝置提供者。</span><span class="sxs-lookup"><span data-stu-id="be038-106">Integrating your cloud storage provider is only supported starting in Windows 10.</span></span>

 

<span data-ttu-id="be038-107">第一件事是註冊為同步根提供者。</span><span class="sxs-lookup"><span data-stu-id="be038-107">The first thing is to register as a sync root provider.</span></span> <span data-ttu-id="be038-108">這可讓 Windows Shell 知道您的應用程式，而且您的應用程式會負責同步處理根的檔案。</span><span class="sxs-lookup"><span data-stu-id="be038-108">This lets the Windows Shell know about your application and that your application will be responsible for synchronizing files under your sync root.</span></span> <span data-ttu-id="be038-109">這也可讓其他應用程式知道您要同步處理這些檔案，讓它們能夠適當地回應。</span><span class="sxs-lookup"><span data-stu-id="be038-109">This will also let other applications know that you are synchronizing these files so that they can respond appropriately.</span></span> <span data-ttu-id="be038-110">然後，其他應用程式就可以使用 [**StorageFile**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) 來取得應用程式的 [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) 和 [**Id**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) 。</span><span class="sxs-lookup"><span data-stu-id="be038-110">Other applications can then use [**StorageFile.Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) to get the [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) and [**Id**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) of your application.</span></span>

<span data-ttu-id="be038-111">為了註冊為同步根提供者，您必須建立多個登錄專案。</span><span class="sxs-lookup"><span data-stu-id="be038-111">In order to register as a sync root provider, you will need to create multiple registry entries.</span></span> <span data-ttu-id="be038-112">在提供索引鍵/值組的清單之前，以下是一些您應該以自己的應用程式資料取代的預留位置。</span><span class="sxs-lookup"><span data-stu-id="be038-112">Before providing the list of key-value pairs, here are some placeholders that you should replace with your own application data.</span></span>

-   <span data-ttu-id="be038-113">*\[ 儲存提供者 \] 識別碼*：雲端儲存體提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="be038-113">*\[storage provider ID\]*: The name of your cloud storage provider.</span></span> <span data-ttu-id="be038-114">無論您的應用程式版本為何，此名稱都應該一致。</span><span class="sxs-lookup"><span data-stu-id="be038-114">This name should be consistent regardless of the version of your application.</span></span> <span data-ttu-id="be038-115">這是 OneDrive 的範例。</span><span class="sxs-lookup"><span data-stu-id="be038-115">An example of this is OneDrive.</span></span>
-   <span data-ttu-id="be038-116">*\[ Windows sid \]*：識別使用者的唯一 Windows sid。</span><span class="sxs-lookup"><span data-stu-id="be038-116">*\[Windows SID\]*: The unique Windows SID that identifies the user.</span></span> <span data-ttu-id="be038-117">如果您的應用程式在單一電腦上支援多個使用者的多個安裝，則需要此部分。</span><span class="sxs-lookup"><span data-stu-id="be038-117">If your app supports multiple installations for multiple users on a single machine, this piece is required.</span></span>
-   <span data-ttu-id="be038-118">*\[ 帳戶識別碼 \]*：此使用者目前帳戶的服務提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="be038-118">*\[Account ID\]*: The service provider identifier for this user's current account.</span></span> <span data-ttu-id="be038-119">有些提供者需要能夠為使用者提供多個同步處理根。</span><span class="sxs-lookup"><span data-stu-id="be038-119">Some providers require the ability to provide multiple synchronization roots for a user.</span></span> <span data-ttu-id="be038-120">其中一個範例是工作和個人帳戶。</span><span class="sxs-lookup"><span data-stu-id="be038-120">One example of this is a work and a personal account.</span></span> <span data-ttu-id="be038-121">*帳戶識別碼* 可讓您為一位使用者註冊多個帳戶。</span><span class="sxs-lookup"><span data-stu-id="be038-121">The *Account ID* enables you to have multiple accounts registered for one user.</span></span> <span data-ttu-id="be038-122">如果您的提供者支援每位使用者多個同步處理根，則需要此部分。</span><span class="sxs-lookup"><span data-stu-id="be038-122">If your provider does support multiple synchronization roots per user, this piece is required.</span></span>

<span data-ttu-id="be038-123">這些預留位置會合並在一起，以形成同步根識別碼。您必須將 **！**</span><span class="sxs-lookup"><span data-stu-id="be038-123">These placeholders are combined together to form the sync root id. You must place a **!**</span></span> <span data-ttu-id="be038-124">形成同步根識別碼時，每個預留位置之間的字元。以下是需要建立的機碼值組。</span><span class="sxs-lookup"><span data-stu-id="be038-124">character between each of the placeholders when forming the sync root id. Here are the key-value pairs that need to be created.</span></span>

-   <span data-ttu-id="be038-125">**HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ DisplayNameResource_* ：指向 Windows Shell 或其他應用程式可以為您的同步根目錄取得使用者易記名稱的資源。</span><span class="sxs-lookup"><span data-stu-id="be038-125">**HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\SyncRootManager\\**_\[storage provider ID\]_*_!_*_\[Windows SID\]_*_!_*_\[Account ID\]_*_\\DisplayNameResource_* : Points to the resource where the Windows Shell or other applications can get a user-friendly name for your sync root.</span></span>
-   <span data-ttu-id="be038-126">**HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ IconResource_* ：指向 Windows Shell 或其他應用程式可以為您的同步根目錄取得圖示的資源。</span><span class="sxs-lookup"><span data-stu-id="be038-126">**HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\SyncRootManager\\**_\[storage provider ID\]_*_!_*_\[Windows SID\]_*_!_*_\[Account ID\]_*_\\IconResource_* : Points to the resource where the Windows Shell or other applications can get an icon for your sync root.</span></span>
-   <span data-ttu-id="be038-127">**HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ UserSyncRoots \\_* _\[ Windows SID \]_ ：同步根目錄所在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="be038-127">**HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\SyncRootManager\\**_\[storage provider ID\]_*_!_*_\[Windows SID\]_*_!_*_\[Account ID\]_*_\\UserSyncRoots\\_*_\[Windows SID\]_ : The location on disk where the sync root is located.</span></span>

<span data-ttu-id="be038-128">除了註冊為同步根提供者之外，您也希望使用者能夠輕鬆存取您提供的資料。</span><span class="sxs-lookup"><span data-stu-id="be038-128">Other than registering as a sync root provider, you also want users to have easy access to the data you provide.</span></span> <span data-ttu-id="be038-129">檔案總管命名空間的設計目的，是為了提供可輕鬆存取的方法。</span><span class="sxs-lookup"><span data-stu-id="be038-129">The File Explorer namespace is designed to provide a method for that easy access.</span></span> <span data-ttu-id="be038-130">建立提供者的命名空間延伸模組並將其併入檔案總管視窗中，可讓使用者與服務的根層級互動，就像是與其他檔案總管專案搭配使用一樣。</span><span class="sxs-lookup"><span data-stu-id="be038-130">Creating a namespace extension for your provider and incorporating it into the File Explorer window will allow users to interact with the root level of your services just like they are used to with other File Explorer items.</span></span> <span data-ttu-id="be038-131">本主題說明如何擴充檔案總管命名空間，讓您的提供者會出現在流覽窗格中的根層級。</span><span class="sxs-lookup"><span data-stu-id="be038-131">This topic explains how to extend the File Explorer namespace so that your provider will appear at the root level in the Navigation Pane.</span></span>

<span data-ttu-id="be038-132">檔案總管視窗的導覽窗格是顯示在左側視窗的部分。</span><span class="sxs-lookup"><span data-stu-id="be038-132">The Navigation Pane of the File Explorer window is the portion of the window displayed on the left side.</span></span> <span data-ttu-id="be038-133">在下圖中，您可以看到此使用者的命名空間結構。</span><span class="sxs-lookup"><span data-stu-id="be038-133">In the image below, you can see the namespace structure for this user.</span></span> <span data-ttu-id="be038-134">流覽窗格中的根層級包括 **OneDrive**、這部 **電腦** 和 **網路** 的物件。</span><span class="sxs-lookup"><span data-stu-id="be038-134">The root level on the Navigation Pane includes the objects for **OneDrive**, **This PC**, and **Network**.</span></span> <span data-ttu-id="be038-135">遵循這些步驟會將您的延伸模組加入至相同的層級。</span><span class="sxs-lookup"><span data-stu-id="be038-135">Following these steps will add your extension to the same level.</span></span>

![瀏覽窗格](images/navigationpane.png)

<span data-ttu-id="be038-137">若要將擴充功能新增至流覽窗格，您必須先具備下列各項，才能編輯登錄：</span><span class="sxs-lookup"><span data-stu-id="be038-137">In order to add your extension to the Navigation Pane, you will need to have the following before editing the registry:</span></span>

-   <span data-ttu-id="be038-138">檔系統資料夾，其中包含要向使用者顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="be038-138">A file system folder that contains the data to display to the user.</span></span>

-   <span data-ttu-id="be038-139">將出現在流覽窗格中的雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="be038-139">Name of your cloud service that will appear in the Navigation Pane.</span></span> <span data-ttu-id="be038-140">如果您的服務支援多個帳戶，這也可以是實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="be038-140">This could also be the name of the instance if your service supports multiple accounts.</span></span>

-   <span data-ttu-id="be038-141">應用程式的可識別圖示。</span><span class="sxs-lookup"><span data-stu-id="be038-141">Identifiable icon for your application.</span></span>

-   <span data-ttu-id="be038-142">應用程式的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="be038-142">A CLSID for your application.</span></span> <span data-ttu-id="be038-143">為您的應用程式產生 CLSID 的其中一種方式是使用 Uuidgen.exe。</span><span class="sxs-lookup"><span data-stu-id="be038-143">One way to generate a CLSID for your application is to use the Uuidgen.exe.</span></span> <span data-ttu-id="be038-144">如需 CLSID 的詳細資訊，請參閱 [Clsid 金鑰](../com/clsid-key-hklm.md) 。</span><span class="sxs-lookup"><span data-stu-id="be038-144">See [CLSID Key](../com/clsid-key-hklm.md) for more information about CLSID.</span></span>

<span data-ttu-id="be038-145">下列步驟會修改登錄，以便在檔案總管命名空間中取得必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="be038-145">The following steps modify the registry in order to get the necessary information into the File Explorer namespace.</span></span> <span data-ttu-id="be038-146">特定步驟會執行三項工作。</span><span class="sxs-lookup"><span data-stu-id="be038-146">The specific steps do three things.</span></span>

-   <span data-ttu-id="be038-147">在登錄中為您的 CLSID 建立機碼，其中包含您的延伸模組名稱和圖示值，以及定義其行為的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="be038-147">Create keys in the registry for your CLSID that includes values for the name and icon for your extension as well as other information that defines its behavior.</span></span>

-   <span data-ttu-id="be038-148">將您的延伸模組設定為整合到適當位置的流覽窗格中，並具有適當的可見度。</span><span class="sxs-lookup"><span data-stu-id="be038-148">Configure your extension to be integrated into the Navigation Pane in the proper location and with the proper visibility.</span></span>

-   <span data-ttu-id="be038-149">設定您的延伸模組，使其在導覽窗格中具有元素的預期行為。</span><span class="sxs-lookup"><span data-stu-id="be038-149">Configure your extension to have the expected behavior for an element in the navigation pane.</span></span>

<span data-ttu-id="be038-150">這些指示特別使用 **reg.exe** 命令，不過您可以使用任何您選擇的登錄編輯工具。</span><span class="sxs-lookup"><span data-stu-id="be038-150">These instructions specifically use the **reg.exe** command, however you can use any registry editing tool of your choice.</span></span> <span data-ttu-id="be038-151">您甚至可以將這些步驟整合到以程式設計方式更新登錄的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="be038-151">You can even integrate these steps into an installer that updates the registry programmatically.</span></span>

## <a name="instructions"></a><span data-ttu-id="be038-152">指示</span><span class="sxs-lookup"><span data-stu-id="be038-152">Instructions</span></span>

### <a name="step-1-add-your-clsid-and-name-your-extension"></a><span data-ttu-id="be038-153">步驟1：加入您的 CLSID 並命名您的延伸模組</span><span class="sxs-lookup"><span data-stu-id="be038-153">Step 1: Add your CLSID and name your extension</span></span>

<span data-ttu-id="be038-154">在 [HKEY 目前使用者] 下，將您的擴充功能名稱新增至登錄 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="be038-154">Add the name of your extension to the registry under HKEY\_CURRENT\_USER.</span></span> <span data-ttu-id="be038-155">您也將新增此延伸模組的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="be038-155">You will also be adding the unique identifier for this extension.</span></span> <span data-ttu-id="be038-156">每位使用者可以加入多個擴充功能，但在此情況下，每個延伸模組都需要唯一的名稱和識別碼。</span><span class="sxs-lookup"><span data-stu-id="be038-156">It is possible to add more than one extension per user, but in that case you will need a unique name and identifier for each extension.</span></span> <span data-ttu-id="be038-157">在這些步驟的其餘部分中，此名稱和識別碼必須保持一致。</span><span class="sxs-lookup"><span data-stu-id="be038-157">This name and identifier must be consistent throughout the rest of these steps.</span></span> <span data-ttu-id="be038-158">在此範例中，名稱是 *MyCloudStorageApp*。</span><span class="sxs-lookup"><span data-stu-id="be038-158">In this example, the name is *MyCloudStorageApp*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be038-159">在這些步驟中 (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) 提供的識別碼，只是作為範例使用。</span><span class="sxs-lookup"><span data-stu-id="be038-159">The identifier provided (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) in these steps is just used as a sample.</span></span> <span data-ttu-id="be038-160">您必須將此變更為您的唯一 CLSID。</span><span class="sxs-lookup"><span data-stu-id="be038-160">You will need to change this to your unique CLSID.</span></span>

 

<span data-ttu-id="be038-161">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d "MyCloudStorageApp"/f**</span><span class="sxs-lookup"><span data-stu-id="be038-161">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG\_SZ /d "MyCloudStorageApp" /f**</span></span>

### <a name="step-2-set-the-image-for-your-icon"></a><span data-ttu-id="be038-162">步驟2：設定圖示的影像</span><span class="sxs-lookup"><span data-stu-id="be038-162">Step 2: Set the image for your icon</span></span>

<span data-ttu-id="be038-163">提供要顯示在導覽窗格中的圖示路徑。</span><span class="sxs-lookup"><span data-stu-id="be038-163">Provide the path to the icon that should be displayed in the Navigation Pane.</span></span> <span data-ttu-id="be038-164">在下列範例中， *1043* 是指指定之 DLL 中圖示的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="be038-164">In the example below, *1043* refers to the resource identifier for the icon in the indicated DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be038-165">您必須更新映射路徑。</span><span class="sxs-lookup"><span data-stu-id="be038-165">You need to update the image path.</span></span> <span data-ttu-id="be038-166">它應該指向您的應用程式安裝映射的一般路徑。</span><span class="sxs-lookup"><span data-stu-id="be038-166">It should point to a generic path where your app installed an image.</span></span>

 

<span data-ttu-id="be038-167">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t REG \_ EXPAND \_ SZ/d%% SystemRoot%% \\ system32 \\imageres.dll，-1043/f**</span><span class="sxs-lookup"><span data-stu-id="be038-167">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\DefaultIcon /ve /t REG\_EXPAND\_SZ /d %%SystemRoot%%\\system32\\imageres.dll,-1043 /f**</span></span>

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a><span data-ttu-id="be038-168">步驟3：將您的擴充功能新增至流覽窗格並讓它顯示</span><span class="sxs-lookup"><span data-stu-id="be038-168">Step 3: Add your extension to the Navigation Pane and make it visible</span></span>

<span data-ttu-id="be038-169">將此值設定為0x1 表示延伸模組應固定。</span><span class="sxs-lookup"><span data-stu-id="be038-169">Setting this value to 0x1 indicates that the extension should be pinned.</span></span> <span data-ttu-id="be038-170">這可確保預設會對使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="be038-170">This will make sure it is shown to users by default.</span></span> <span data-ttu-id="be038-171">使用者的預設設定是只有釘選的專案會顯示在流覽窗格中。</span><span class="sxs-lookup"><span data-stu-id="be038-171">The default configuration for a user is that only pinned items will be shown in the Navigation Pane.</span></span> <span data-ttu-id="be038-172">使用者可以在流覽窗格中按一下滑鼠右鍵，然後選取 [ **顯示所有資料夾**] 來變更該設定。</span><span class="sxs-lookup"><span data-stu-id="be038-172">A user can change that setting by right-clicking in the Navigation Pane and selecting **Show all folders**.</span></span> <span data-ttu-id="be038-173">如果您不想要釘選您的延伸模組，您可以將此值設定為0x0。</span><span class="sxs-lookup"><span data-stu-id="be038-173">If you don't want to pin your extension, you can set this value to 0x0.</span></span> <span data-ttu-id="be038-174">這不會移除您的延伸模組，只會防止預設顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="be038-174">That will not remove your extension, but merely prevent it from being displayed to the user by default.</span></span>

<span data-ttu-id="be038-175">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/v SYSTEM. IsPinnedToNameSpaceTree/t REG \_ DWORD/d 0x1/f**</span><span class="sxs-lookup"><span data-stu-id="be038-175">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v System.IsPinnedToNameSpaceTree /t REG\_DWORD /d 0x1 /f**</span></span>

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a><span data-ttu-id="be038-176">步驟4：在流覽窗格中設定延伸模組的位置</span><span class="sxs-lookup"><span data-stu-id="be038-176">Step 4: Set the location for your extension in the Navigation Pane</span></span>

<span data-ttu-id="be038-177">這一點很重要，因為這是為了確保流覽窗格能為使用者提供一致的體驗。</span><span class="sxs-lookup"><span data-stu-id="be038-177">This is critical in order to make sure the Navigation Pane provides a consistent experience for the user.</span></span>

<span data-ttu-id="be038-178">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/V SortOrderIndex/t REG \_ DWORD/d 0x42/f**</span><span class="sxs-lookup"><span data-stu-id="be038-178">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v SortOrderIndex /t REG\_DWORD /d 0x42 /f**</span></span>

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a><span data-ttu-id="be038-179">步驟5：提供裝載您延伸模組的 dll。</span><span class="sxs-lookup"><span data-stu-id="be038-179">Step 5: Provide the dll that hosts your extension.</span></span>

<span data-ttu-id="be038-180">使用 shell32.dll 模擬預設的 windows 資料夾。</span><span class="sxs-lookup"><span data-stu-id="be038-180">Use the shell32.dll to emulate default windows folders.</span></span> <span data-ttu-id="be038-181">只有當您有特定原因要進行變更時，才需要變更，並熟悉命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="be038-181">Only change this if you have a specific reason to do so and are familiar with namespace extensions.</span></span>

<span data-ttu-id="be038-182">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32/ve/t REG \_ EXPAND \_ SZ/d%% systemroot%% \\ system32 \\shell32.dll/f**</span><span class="sxs-lookup"><span data-stu-id="be038-182">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\InProcServer32 /ve /t REG\_EXPAND\_SZ /d %%systemroot%%\\system32\\shell32.dll /f**</span></span>

### <a name="step-6-define-the-instance-object"></a><span data-ttu-id="be038-183">步驟6：定義實例物件</span><span class="sxs-lookup"><span data-stu-id="be038-183">Step 6: Define the instance object</span></span>

<span data-ttu-id="be038-184">指出您的命名空間延伸模組應如檔案總管中的其他檔案資料夾結構一樣運作。</span><span class="sxs-lookup"><span data-stu-id="be038-184">Indicate that your namespace extension should function like other file folder structures in File Explorer.</span></span> <span data-ttu-id="be038-185">如需 shell 實例物件的詳細資訊，請參閱 [使用 Shell 實例物件建立 Shell 延伸](/previous-versions/ms997573(v=msdn.10))模組。</span><span class="sxs-lookup"><span data-stu-id="be038-185">For more information about shell instance objects, see [Creating Shell Extensions with Shell Instance Objects](/previous-versions/ms997573(v=msdn.10)).</span></span>

<span data-ttu-id="be038-186">**reg add HKCU \\ Software \\ 類別 \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance/v clsid/T REG \_ SZ/d {0E5AAE11-A475-4c5b-AB00-C66DE400274E}/f**</span><span class="sxs-lookup"><span data-stu-id="be038-186">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\Instance /v CLSID /t REG\_SZ /d {0E5AAE11-A475-4c5b-AB00-C66DE400274E} /f**</span></span>

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a><span data-ttu-id="be038-187">步驟7：提供目的檔案夾的檔案系統屬性</span><span class="sxs-lookup"><span data-stu-id="be038-187">Step 7: Provide the file system attributes of the target folder</span></span>

<span data-ttu-id="be038-188">這是必要的，以確保檔案總管為使用者提供一致且預期的體驗。</span><span class="sxs-lookup"><span data-stu-id="be038-188">This is required to make sure that the File Explorer provides a consistent and expected experience for users.</span></span> <span data-ttu-id="be038-189">此命令會設定 **檔 \_ 屬性 \_ 目錄** 和 **檔 \_ 屬性 \_ READONLY**，兩者都是 [**檔案屬性常數**](../fileio/file-attribute-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="be038-189">This command sets **FILE\_ATTRIBUTE\_DIRECTORY** and **FILE\_ATTRIBUTE\_READONLY**, both of which are [**File Attribute Constants**](../fileio/file-attribute-constants.md).</span></span>

<span data-ttu-id="be038-190">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ INSTANCE \\ InitPropertyBag/v Attributes/t REG \_ DWORD/d 0x11/f**</span><span class="sxs-lookup"><span data-stu-id="be038-190">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\Instance\\InitPropertyBag /v Attributes /t REG\_DWORD /d 0x11 /f**</span></span>

### <a name="step-8-set-the-path-for-the-sync-root"></a><span data-ttu-id="be038-191">步驟8：設定同步根的路徑</span><span class="sxs-lookup"><span data-stu-id="be038-191">Step 8: Set the path for the sync root</span></span>

<span data-ttu-id="be038-192">設定同步根的路徑。</span><span class="sxs-lookup"><span data-stu-id="be038-192">Set the path for the sync root.</span></span>

<span data-ttu-id="be038-193">**reg add HKCU \\ Software \\ 類別 \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ 實例 \\ InitPropertyBag/v TargetFolderPath/t REG \_ EXPAND \_ SZ/d%% USERPROFILE%% \\ MyCloudStorageApp/f**</span><span class="sxs-lookup"><span data-stu-id="be038-193">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\Instance\\InitPropertyBag /v TargetFolderPath /t REG\_EXPAND\_SZ /d %%USERPROFILE%%\\MyCloudStorageApp /f**</span></span>

### <a name="step-9-set-appropriate-shell-flags"></a><span data-ttu-id="be038-194">步驟9：設定適當的 shell 旗標</span><span class="sxs-lookup"><span data-stu-id="be038-194">Step 9: Set appropriate shell flags</span></span>

<span data-ttu-id="be038-195">設定將命名空間延伸模組釘選到檔案總管樹狀結構所需的一些旗標。</span><span class="sxs-lookup"><span data-stu-id="be038-195">Set some flags necessary to pin your namespace extension to the File Explorer tree.</span></span>

<span data-ttu-id="be038-196">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v FolderValueFlags/t REG \_ DWORD/d 0x28/f**</span><span class="sxs-lookup"><span data-stu-id="be038-196">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\ShellFolder /v FolderValueFlags /t REG\_DWORD /d 0x28 /f**</span></span>

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a><span data-ttu-id="be038-197">步驟10：設定適當的旗標，以控制您的 shell 行為</span><span class="sxs-lookup"><span data-stu-id="be038-197">Step 10: Set the appropriate flags to control your shell behavior</span></span>

<span data-ttu-id="be038-198">設定適當的 [**SFGAO**](sfgao.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="be038-198">Set the appropriate [**SFGAO**](sfgao.md) flags.</span></span> <span data-ttu-id="be038-199">相關的旗標為 SFGAO \_ CANCOPY、SFGAO \_ CANLINK、SFGAO \_ STORAGE、SFGAO \_ HASPROPSHEET、SFGAO \_ STORAGEANCESTOR、SFGAO \_ FILESYSANCESTOR、SFGAO \_ FOLDER、SFGAO \_ FILESYSTEM 和 SFGAO \_ HASSUBFOLDER。</span><span class="sxs-lookup"><span data-stu-id="be038-199">The relevant flags are SFGAO\_CANCOPY, SFGAO\_CANLINK, SFGAO\_STORAGE, SFGAO\_HASPROPSHEET, SFGAO\_STORAGEANCESTOR, SFGAO\_FILESYSANCESTOR, SFGAO\_FOLDER, SFGAO\_FILESYSTEM, and SFGAO\_HASSUBFOLDER.</span></span>

<span data-ttu-id="be038-200">**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v Attributes/t REG \_ DWORD/d 0xF080004D/f**</span><span class="sxs-lookup"><span data-stu-id="be038-200">**reg add HKCU\\Software\\Classes\\CLSID\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}\\ShellFolder /v Attributes /t REG\_DWORD /d 0xF080004D /f**</span></span>

### <a name="step-11-register-your-extension-in-the-namespace-root"></a><span data-ttu-id="be038-201">步驟11：在命名空間根目錄中註冊您的延伸模組</span><span class="sxs-lookup"><span data-stu-id="be038-201">Step 11: Register your extension in the namespace root</span></span>

<span data-ttu-id="be038-202">將命名空間延伸模組設定為 [桌面] 資料夾的子系。</span><span class="sxs-lookup"><span data-stu-id="be038-202">Configure the namespace extension to be a child of the desktop folder.</span></span>

<span data-ttu-id="be038-203">**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d MyCloudStorageApp/f**</span><span class="sxs-lookup"><span data-stu-id="be038-203">**reg add HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Desktop\\NameSpace\\{0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG\_SZ /d MyCloudStorageApp /f**</span></span>

### <a name="step-12-hide-your-extension-from-the-desktop"></a><span data-ttu-id="be038-204">步驟12：從桌面上隱藏您的延伸模組</span><span class="sxs-lookup"><span data-stu-id="be038-204">Step 12: Hide your extension from the Desktop</span></span>

<span data-ttu-id="be038-205">您的延伸模組必須只出現在檔案總管的導覽窗格上。</span><span class="sxs-lookup"><span data-stu-id="be038-205">It is important that your extension only appears on the Navigation Pane of the File Explorer.</span></span> <span data-ttu-id="be038-206">命名空間延伸模組的運作方式不像一般快捷方式。</span><span class="sxs-lookup"><span data-stu-id="be038-206">A namespace extension does not function like a normal shortcut.</span></span> <span data-ttu-id="be038-207">因此，您不應該使用這個方法來建立桌面快捷方式。</span><span class="sxs-lookup"><span data-stu-id="be038-207">Therefore, you should not use this method to create a Desktop shortcut.</span></span>

<span data-ttu-id="be038-208">**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/t REG \_ DWORD/d 0x1/f**</span><span class="sxs-lookup"><span data-stu-id="be038-208">**reg add HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\HideDesktopIcons\\NewStartPanel /v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /t REG\_DWORD /d 0x1 /f**</span></span>

 

 
