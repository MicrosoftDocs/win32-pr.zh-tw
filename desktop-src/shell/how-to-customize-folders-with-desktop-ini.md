---
description: 使用 Desktop.ini 自訂個別資料夾的外觀和行為。
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: 如何使用 Desktop.ini 自訂資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550017"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="00387-103">如何使用 Desktop.ini 自訂資料夾</span><span class="sxs-lookup"><span data-stu-id="00387-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="00387-104">檔系統資料夾通常會以標準圖示和一組屬性來顯示，以指定是否共用資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="00387-105">您可以建立該資料夾的 Desktop.ini 檔案，以自訂個別資料夾的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="00387-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="00387-106">指示</span><span class="sxs-lookup"><span data-stu-id="00387-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="00387-107">使用 Desktop.ini 檔案</span><span class="sxs-lookup"><span data-stu-id="00387-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="00387-108">資料夾通常會顯示標準資料夾圖示。</span><span class="sxs-lookup"><span data-stu-id="00387-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="00387-109">Desktop.ini 檔案的常見用法是將自訂圖示或縮圖影像指派給資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="00387-110">您也可以使用 Desktop.ini 來建立資訊 *提示，以* 顯示資料夾的相關資訊，並控制資料夾行為的某些層面，例如指定資料夾或資料夾中專案的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="00387-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="00387-111">**您可以使用下列程式，利用 Desktop.ini 自訂資料夾的樣式：**</span><span class="sxs-lookup"><span data-stu-id="00387-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="00387-112">使用 [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) 將資料夾設為系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="00387-113">這會將資料夾的唯讀位設定為，以指出應啟用針對 Desktop.ini 保留的特殊行為。</span><span class="sxs-lookup"><span data-stu-id="00387-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="00387-114">您也可以使用 **attrib + s** *資料夾資料夾*，從命令列將資料夾設為系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="00387-115">建立資料夾的 Desktop.ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="00387-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="00387-116">您應該將它標示為 *隱藏* 和 *系統* ，以確保它會從一般使用者中隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="00387-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="00387-117">請確定您建立的 Desktop.ini 檔案是 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="00387-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="00387-118">這是儲存可顯示給使用者之當地語系化字串的必要動作。</span><span class="sxs-lookup"><span data-stu-id="00387-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="00387-119">建立 Desktop.ini 檔案</span><span class="sxs-lookup"><span data-stu-id="00387-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="00387-120">Desktop.ini 檔案是一個文字檔，可讓您指定如何查看檔系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="00387-121">\[。ShellClassInfo \] 區段可讓您將值指派給數個專案，以自訂資料夾的視圖：</span><span class="sxs-lookup"><span data-stu-id="00387-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00387-122">**進入**</span><span class="sxs-lookup"><span data-stu-id="00387-122">**Entry**</span></span>         | <span data-ttu-id="00387-123">**值**</span><span class="sxs-lookup"><span data-stu-id="00387-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="00387-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="00387-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="00387-125">將此專案設定為0，以避免在刪除或移動資料夾時出現「您正在刪除系統資料夾」警告。</span><span class="sxs-lookup"><span data-stu-id="00387-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="00387-126">**NoSharing**</span><span class="sxs-lookup"><span data-stu-id="00387-126">**NoSharing**</span></span>     | <span data-ttu-id="00387-127">在 Windows Vista 或更新版本下不支援。</span><span class="sxs-lookup"><span data-stu-id="00387-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="00387-128">將此專案設定為1，以防止資料夾共用。</span><span class="sxs-lookup"><span data-stu-id="00387-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="00387-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="00387-129">**IconFile**</span></span>      | <span data-ttu-id="00387-130">如果您想要指定資料夾的自訂圖示，請將此專案設定為圖示的檔案名。</span><span class="sxs-lookup"><span data-stu-id="00387-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="00387-131">.Ico 副檔名是慣用的，但也可以指定 .bmp 檔，或包含圖示的 .exe 和 .dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="00387-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="00387-132">如果您使用相對路徑，則圖示可供透過網路觀看資料夾的人員使用。</span><span class="sxs-lookup"><span data-stu-id="00387-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="00387-133">您也必須設定 **>iconindex** 專案。</span><span class="sxs-lookup"><span data-stu-id="00387-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="00387-134">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="00387-134">**IconIndex**</span></span>     | <span data-ttu-id="00387-135">設定此專案可指定自訂圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="00387-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="00387-136">如果指派給 **IconFile** 的檔案只包含單一圖示，請將 **>iconindex** 設定為0。</span><span class="sxs-lookup"><span data-stu-id="00387-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="00387-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="00387-137">**InfoTip**</span></span>       | <span data-ttu-id="00387-138">將此專案設定為資訊文字字串。</span><span class="sxs-lookup"><span data-stu-id="00387-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="00387-139">當游標停留在資料夾上時，它會顯示為提示。</span><span class="sxs-lookup"><span data-stu-id="00387-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="00387-140">如果使用者按一下資料夾，資訊文字會顯示在資料夾的 [資訊] 區塊中，位於標準資訊下方。</span><span class="sxs-lookup"><span data-stu-id="00387-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="00387-141">下圖是含有自訂 Desktop.ini 檔案的 [音樂] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="00387-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="00387-142">資料夾現在：</span><span class="sxs-lookup"><span data-stu-id="00387-142">The folder now:</span></span>

-   <span data-ttu-id="00387-143">具有自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="00387-143">Has a custom icon.</span></span>
-   <span data-ttu-id="00387-144">如果資料夾已移動或刪除，則不會顯示「您正在刪除系統資料夾」警告。</span><span class="sxs-lookup"><span data-stu-id="00387-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="00387-145">無法共用。</span><span class="sxs-lookup"><span data-stu-id="00387-145">Cannot be shared.</span></span>
-   <span data-ttu-id="00387-146">當游標停留在資料夾上時，顯示資訊文字。</span><span class="sxs-lookup"><span data-stu-id="00387-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="00387-147">下圖中的資料夾選項設定為顯示隱藏的檔案，以便顯示 Desktop.ini。</span><span class="sxs-lookup"><span data-stu-id="00387-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="00387-148">資料夾看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="00387-148">The folder looks like this:</span></span>

![具有自訂圖示之資料夾的螢幕擷取畫面](images/webview4.jpg)

<span data-ttu-id="00387-150">當游標停留在資料夾上時，就會顯示提示。</span><span class="sxs-lookup"><span data-stu-id="00387-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![具有提示的資料夾螢幕擷取畫面](images/webview6.jpg)

<span data-ttu-id="00387-152">自訂圖示會取代資料夾名稱出現位置的資料夾圖示。</span><span class="sxs-lookup"><span data-stu-id="00387-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![取代資料夾圖示的自訂圖示螢幕擷取畫面](images/webview5.jpg)

<span data-ttu-id="00387-154">下列 desktop.ini 檔案是用來自訂 [音樂] 資料夾，如先前的圖例所示。</span><span class="sxs-lookup"><span data-stu-id="00387-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



