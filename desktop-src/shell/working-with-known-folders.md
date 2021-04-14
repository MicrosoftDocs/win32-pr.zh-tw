---
description: 已知的資料夾系統會提供一種方式，讓您與 Windows 中預設存在的某些高階設定檔資料夾互動。
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: 使用應用程式中的已知資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468589"
---
# <a name="working-with-known-folders-in-applications"></a><span data-ttu-id="c4fc7-103">使用應用程式中的已知資料夾</span><span class="sxs-lookup"><span data-stu-id="c4fc7-103">Working with Known Folders in Applications</span></span>

<span data-ttu-id="c4fc7-104">已知的資料夾系統會提供一種方式，讓您與 Windows 中預設存在的某些高階設定檔資料夾互動。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-104">The Known Folder system provides a way to interact with certain high-profile folders that are present by default in Windows.</span></span> <span data-ttu-id="c4fc7-105">它也允許應用程式與安裝並向已知資料夾系統註冊的資料夾進行相同的互動。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-105">It also allows those same interactions with folders installed and registered with the Known Folder system by applications.</span></span> <span data-ttu-id="c4fc7-106">本主題討論已知的資料夾 Api 提供的可能互動。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-106">This topic discusses those possible interactions as they are provided by the Known Folder APIs.</span></span>

-   [<span data-ttu-id="c4fc7-107">已知的資料夾介面</span><span class="sxs-lookup"><span data-stu-id="c4fc7-107">Known Folder Interfaces</span></span>](#known-folder-interfaces)
-   [<span data-ttu-id="c4fc7-108">重新導向</span><span class="sxs-lookup"><span data-stu-id="c4fc7-108">Redirection</span></span>](#redirection)
-   [<span data-ttu-id="c4fc7-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4fc7-109">Related topics</span></span>](#related-topics)

> [!IMPORTANT]
> <span data-ttu-id="c4fc7-110">若要將 [檔]、[圖片] 或 [桌面] 資料夾重新導向至 OneDrive，請使用 OneDrive 已知資料夾移動，而不是本文中所述的重新導向方法。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-110">To redirect the Documents, Pictures, or Desktop folders to OneDrive, use OneDrive Known Folder Move instead of the redirection method described in this article.</span></span> <span data-ttu-id="c4fc7-111">如需詳細資訊，請參閱 [將 Windows 已知資料夾重新導向並移至 OneDrive](/onedrive/redirect-known-folders)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-111">For information, see [Redirect and move Windows known folders to OneDrive](/onedrive/redirect-known-folders).</span></span>  

## <a name="known-folder-interfaces"></a><span data-ttu-id="c4fc7-112">已知的資料夾介面</span><span class="sxs-lookup"><span data-stu-id="c4fc7-112">Known Folder Interfaces</span></span>

<span data-ttu-id="c4fc7-113">有兩個已知的資料夾介面： [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 和 [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-113">There are two Known Folder interfaces: [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) and [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).</span></span>

<span data-ttu-id="c4fc7-114">[**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) 提供許多關於這些資料夾的一般功能。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-114">[**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) provides many of the more general functions in regard to these folders.</span></span> <span data-ttu-id="c4fc7-115">它的方法可讓您：</span><span class="sxs-lookup"><span data-stu-id="c4fc7-115">Its methods allow you to:</span></span>

-   <span data-ttu-id="c4fc7-116">根據該資料夾的 [**KNOWNFOLDERID**](knownfolderid.md)、其正式名稱、其路徑（以字串表示）或其路徑（以 idlist.txt 表示）來抓取 [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-116">Retrieve an [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) based on either that folder's [**KNOWNFOLDERID**](knownfolderid.md), its canonical name, its path expressed as a string, or its path expressed as an IDList.</span></span>
-   <span data-ttu-id="c4fc7-117">將 CSIDL 轉換為其相等的 [**KNOWNFOLDERID**](knownfolderid.md) ，或將 **KNOWNFOLDERID** 轉換為其舊版 CSIDL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-117">Convert a CSIDL to its [**KNOWNFOLDERID**](knownfolderid.md) equivalent or convert a **KNOWNFOLDERID** to its legacy CSIDL equivalent.</span></span>
-   <span data-ttu-id="c4fc7-118">向系統註冊或取消註冊已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-118">Register or unregister a Known Folder with the system.</span></span>
-   <span data-ttu-id="c4fc7-119">取出在該系統上註冊的所有 [**KNOWNFOLDERID**](knownfolderid.md) 值。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-119">Retrieve all [**KNOWNFOLDERID**](knownfolderid.md) values registered on that system.</span></span>
-   <span data-ttu-id="c4fc7-120">將已知資料夾重新導向至新位置。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-120">Redirect a Known Folder to a new location.</span></span>

<span data-ttu-id="c4fc7-121">[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 提供一種方法，可讓資料夾藉由提供新的路徑來重新導向。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-121">[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) provides a method that allows a folder to redirect itself by providing a new path.</span></span> <span data-ttu-id="c4fc7-122">它的其他方法會取得特定已知資料夾的相關資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="c4fc7-122">Its other methods get information about a specific Known Folder, including:</span></span>

-   <span data-ttu-id="c4fc7-123">資料夾的類別：虛擬、固定、通用或每位使用者。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-123">The category of the folder: virtual, fixed, common, or per-user.</span></span>
-   <span data-ttu-id="c4fc7-124">資料夾的類型，例如壓縮檔、檔、圖片或使用者檔案。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-124">The type of the folder, such as compressed, documents, pictures, or user files.</span></span>
-   <span data-ttu-id="c4fc7-125">資料夾的 [**KNOWNFOLDERID**](knownfolderid.md) 。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-125">The [**KNOWNFOLDERID**](knownfolderid.md) of the folder.</span></span>
-   <span data-ttu-id="c4fc7-126">資料夾的完整路徑，做為 Idlist.txt 或字串。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-126">The full path of the folder as an IDList or as a string.</span></span> <span data-ttu-id="c4fc7-127">也是其父資料夾的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-127">Also its relative path to a parent folder.</span></span>
-   <span data-ttu-id="c4fc7-128">資料夾的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-128">The canonical name of the folder.</span></span>
-   <span data-ttu-id="c4fc7-129">針對資料夾顯示的工具提示。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-129">The tooltip displayed for the folder.</span></span>
-   <span data-ttu-id="c4fc7-130">針對資料夾顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-130">The icon displayed for the folder.</span></span>
-   <span data-ttu-id="c4fc7-131">說明其目的和使用的資料夾描述。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-131">A description of the folder that explains its purpose and use.</span></span>
-   <span data-ttu-id="c4fc7-132">是否能夠將資料夾重新導向。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-132">Whether the folder is capable of being redirected.</span></span>

<span data-ttu-id="c4fc7-133">[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 也會提供一種方法，以根據資料夾來取得 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-133">[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) also provides a method to retrieve an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) based on the folder.</span></span> <span data-ttu-id="c4fc7-134">這可讓您將資料夾系結至處理常式、比較兩個資料夾，以及抓取資料夾的屬性、顯示名稱和上層資料夾。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-134">That allows you to bind the folder to a handler, compare two folders, and retrieve the folder's attributes, display name, and parent folder.</span></span>

## <a name="redirection"></a><span data-ttu-id="c4fc7-135">重新導向</span><span class="sxs-lookup"><span data-stu-id="c4fc7-135">Redirection</span></span>

<span data-ttu-id="c4fc7-136">資料夾重新導向是已知資料夾系統的一項重要功能。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-136">Folder redirection is an important feature of the known folder system.</span></span> <span data-ttu-id="c4fc7-137">類別通用 KF 類別目錄的所有已知資料夾（一般 [  \_ \_ \* \*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) \* \* \* 或 [**每位使用者** KF \_ 類別 \_ PERUSER \* \*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) \* \*）都是可重新導向。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-137">All known folders of category [**common** KF\_CATEGORY\_COMMON\*\*\*\*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) or [**per-user** KF\_CATEGORY\_PERUSER\*\*\*\*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) are redirectable.</span></span> <span data-ttu-id="c4fc7-138">但無法重新導向類別 [**虛擬** KF \_ 類別 \_ 虛擬 \* \*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) \* \* \* 或 [ **fixedr** KF \_ 類別 \_ 固定](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-138">Folder of category [**virtual** KF\_CATEGORY\_VIRTUAL\*\*\*\*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) or [**fixedr** KF\_CATEGORY\_FIXED\*\*\*\*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category), however, cannot be redirected.</span></span>

<span data-ttu-id="c4fc7-139">您可以將資料夾重新導向至同一部電腦上的其他位置，或重新導向至網路上的位置。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-139">Folders can be redirected either to another location on the same computer or to a location on a network.</span></span> <span data-ttu-id="c4fc7-140">在網路重新導向的情況下，可以透過用戶端快取在本機快取資料夾，以提供離線存取。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-140">In the case of a network redirection, the folder can be cached locally through client-side caching to provide offline access.</span></span> <span data-ttu-id="c4fc7-141">但是，即使本機快取存在，也必須透過網路存取重新導向的資料夾本身。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-141">However, even if a local cache exists, the redirected folder itself must be accessed through the network.</span></span>

<span data-ttu-id="c4fc7-142">資料夾重新導向不是 Windows Vista 的新功能。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-142">Folder redirection is not new for Windows Vista.</span></span> <span data-ttu-id="c4fc7-143">例如，在 Windows XP 中，透過 CSIDL 系統識別的某些資料夾，可以透過呼叫 [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) 或藉由修改登錄中的 CSIDL 專案來重新導向。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-143">For example, in Windows XP some folders identified through the CSIDL system could be redirected through a call to [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) or by modifying the CSIDL's entry in the registry.</span></span> <span data-ttu-id="c4fc7-144">在 Windows Vista 和更新版本中，重新導向應該透過 [**IKnownFolder：： SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) 或 [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)來完成。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-144">In Windows Vista and later, redirection should be accomplished through [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) or [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).</span></span>

<span data-ttu-id="c4fc7-145">若要判斷是否可以重新導向資料夾，請呼叫 [**IKnownFolder：： GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-145">To determine whether a folder can be redirected, call [**IKnownFolder::GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities).</span></span> <span data-ttu-id="c4fc7-146">如果無法重新導向資料夾，此呼叫可以提供說明。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-146">If the folder cannot be redirected, this call can give an explanation.</span></span>

<span data-ttu-id="c4fc7-147">如果將資料夾重新導向至網路位置，則仍可在其上成功呼叫 [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 方法。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-147">If a folder is redirected to a network location, the [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) methods can still be successfully called on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4fc7-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4fc7-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c4fc7-149">[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4fc7-149">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
