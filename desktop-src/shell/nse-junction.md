---
description: 命名空間延伸的根目錄通常會 Windows 檔案總管顯示為樹狀目錄和資料夾檢視中的資料夾。
title: 指定命名空間延伸模組的位置
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850044"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="fdf20-103">指定命名空間延伸模組的位置</span><span class="sxs-lookup"><span data-stu-id="fdf20-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="fdf20-104">命名空間延伸的根目錄通常會 Windows 檔案總管顯示為樹狀目錄和資料夾檢視中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="fdf20-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="fdf20-105">若要讓 Windows 檔案總管顯示延伸模組的檔案和子資料夾，您必須指定根資料夾位於 Shell 命名空間階層中的位置。</span><span class="sxs-lookup"><span data-stu-id="fdf20-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="fdf20-106">這個位置稱為「 *連接點*」。</span><span class="sxs-lookup"><span data-stu-id="fdf20-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="fdf20-107">使用虛擬資料夾做為連接點</span><span class="sxs-lookup"><span data-stu-id="fdf20-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="fdf20-108">使用檔系統資料夾做為連接點</span><span class="sxs-lookup"><span data-stu-id="fdf20-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="fdf20-109">開啟命名空間延伸模組的視圖</span><span class="sxs-lookup"><span data-stu-id="fdf20-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="fdf20-110">使用虛擬資料夾做為連接點</span><span class="sxs-lookup"><span data-stu-id="fdf20-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="fdf20-111">定義延伸模組連接點最簡單的方式，就是將根資料夾設為系統虛擬資料夾的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="fdf20-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="fdf20-112">這種類型的連接點稱為 *虛擬連接點*。</span><span class="sxs-lookup"><span data-stu-id="fdf20-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="fdf20-113">**桌上型電腦** 和 **我的電腦** 資料夾是虛擬連接點的典型位置，但您也可以在遠端電腦上或在 [**我的網路位置**]、[ **Internet Explorer**] 和 [**主控台**] 資料夾中定義虛擬連接點。</span><span class="sxs-lookup"><span data-stu-id="fdf20-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="fdf20-114">若要定義虛擬連接點，請建立代表適當虛擬資料夾的機碼子機碼，並將它命名為您的延伸模組類別識別碼的字串格式， (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="fdf20-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="fdf20-115">註冊的 CLSID 會如下所示。</span><span class="sxs-lookup"><span data-stu-id="fdf20-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="fdf20-116">*虛擬資料夾名稱* 是下表中的其中一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="fdf20-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="fdf20-117">Location</span><span class="sxs-lookup"><span data-stu-id="fdf20-117">Location</span></span>          | <span data-ttu-id="fdf20-118">虛擬資料夾名稱</span><span class="sxs-lookup"><span data-stu-id="fdf20-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="fdf20-119">控制台</span><span class="sxs-lookup"><span data-stu-id="fdf20-119">Control Panel</span></span>     | <span data-ttu-id="fdf20-120">**控制台**</span><span class="sxs-lookup"><span data-stu-id="fdf20-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="fdf20-121">桌面</span><span class="sxs-lookup"><span data-stu-id="fdf20-121">Desktop</span></span>           | <span data-ttu-id="fdf20-122">**桌上型電腦**</span><span class="sxs-lookup"><span data-stu-id="fdf20-122">**Desktop**</span></span>                                |
| <span data-ttu-id="fdf20-123">整個網路</span><span class="sxs-lookup"><span data-stu-id="fdf20-123">Entire Network</span></span>    | <span data-ttu-id="fdf20-124">**NetworkNeighborhood** \\**EntireNetwork**</span><span class="sxs-lookup"><span data-stu-id="fdf20-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="fdf20-125">我的電腦</span><span class="sxs-lookup"><span data-stu-id="fdf20-125">My Computer</span></span>       | <span data-ttu-id="fdf20-126">**MyComputer**</span><span class="sxs-lookup"><span data-stu-id="fdf20-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="fdf20-127">網路上的芳鄰</span><span class="sxs-lookup"><span data-stu-id="fdf20-127">My Network Places</span></span> | <span data-ttu-id="fdf20-128">**NetworkNeighborhood**</span><span class="sxs-lookup"><span data-stu-id="fdf20-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="fdf20-129">遠端電腦</span><span class="sxs-lookup"><span data-stu-id="fdf20-129">Remote Computer</span></span>   | <span data-ttu-id="fdf20-130">**RemoteComputer**</span><span class="sxs-lookup"><span data-stu-id="fdf20-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="fdf20-131">使用者檔案</span><span class="sxs-lookup"><span data-stu-id="fdf20-131">Users Files</span></span>       | <span data-ttu-id="fdf20-132">**UsersFiles**</span><span class="sxs-lookup"><span data-stu-id="fdf20-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="fdf20-133">遠端擴充必須使用 [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer)初始化。</span><span class="sxs-lookup"><span data-stu-id="fdf20-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="fdf20-134">使用檔系統資料夾做為連接點</span><span class="sxs-lookup"><span data-stu-id="fdf20-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="fdf20-135">有兩種方式可將檔系統資料夾定義為連接點。</span><span class="sxs-lookup"><span data-stu-id="fdf20-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="fdf20-136">最簡單的方法是在適當的位置建立資料夾，並將句點附加到資料夾的名稱，後面接著您的延伸模組 CLSID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="fdf20-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="fdf20-137">Windows 檔案總管中只會顯示資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="fdf20-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="fdf20-138">下列範例會建立具有 MyFolder 顯示名稱的連接點。</span><span class="sxs-lookup"><span data-stu-id="fdf20-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="fdf20-139">或者，您可以透過下列方式，將傳統命名資料夾定義為連接點：</span><span class="sxs-lookup"><span data-stu-id="fdf20-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="fdf20-140">將資料夾設為唯讀。</span><span class="sxs-lookup"><span data-stu-id="fdf20-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="fdf20-141">藉由呼叫 [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera)，將資料夾設為系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="fdf20-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="fdf20-142">將隱藏的 Desktop.ini 檔案放在包含副檔名 CLSID 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="fdf20-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="fdf20-143">Desktop.ini 是標準文字檔，可新增至任何資料夾，以自訂資料夾行為的特定層面。</span><span class="sxs-lookup"><span data-stu-id="fdf20-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="fdf20-144">如需如何使用此檔案的一般討論，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。</span><span class="sxs-lookup"><span data-stu-id="fdf20-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="fdf20-145">若要將資料夾定義為連接點，則為 \[ 。\] Desktop.ini 的 ShellClassInfo 區段必須包含擴充功能的 CLSID，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fdf20-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="fdf20-146">開啟命名空間延伸模組的視圖</span><span class="sxs-lookup"><span data-stu-id="fdf20-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="fdf20-147">當使用者流覽到連接點時，Windows 檔案總管會自動建立根資料夾的視圖。</span><span class="sxs-lookup"><span data-stu-id="fdf20-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="fdf20-148">您也可以藉由將副檔名為 CLSID 的 Explorer.exe 明確地啟動為引數，來建立一個 view。</span><span class="sxs-lookup"><span data-stu-id="fdf20-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="fdf20-149">比方說，您可以使用這個方法，從快捷方式功能表或快捷方式啟動擴充功能的觀點。</span><span class="sxs-lookup"><span data-stu-id="fdf20-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="fdf20-150">例如，若要啟動包含樹狀檢視的 MyExtension，您可以使用下列命令字串。</span><span class="sxs-lookup"><span data-stu-id="fdf20-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="fdf20-151">替代的命令字串可以用來啟動延伸模組內的物件檢視。</span><span class="sxs-lookup"><span data-stu-id="fdf20-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="fdf20-152">這項功能對於使用資料夾檢視的延伸模組很有用，例如，可讓使用者查看其中一個壓縮檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="fdf20-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="fdf20-153">*Objectname* 參數是要查看之物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdf20-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="fdf20-154">Windows 檔案總管將名稱轉換為其對應的 PIDL，並將 PIDL 傳遞至新的資料夾物件的 [**IPersistFolder：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="fdf20-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="fdf20-155">CLSID 字串的前面必須加上一對冒號 (：： ) 或命令將會失敗。</span><span class="sxs-lookup"><span data-stu-id="fdf20-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="fdf20-156">上述兩個範例命令列中使用的斜線-e (/e) 旗標會指示 Windows 檔案總管顯示樹狀檢視。</span><span class="sxs-lookup"><span data-stu-id="fdf20-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="fdf20-157">旗標必須以逗號分隔，並以兩個冒號分隔。</span><span class="sxs-lookup"><span data-stu-id="fdf20-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="fdf20-158">如果您不想要樹狀檢視，請省略/e 旗標和逗號。</span><span class="sxs-lookup"><span data-stu-id="fdf20-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 



