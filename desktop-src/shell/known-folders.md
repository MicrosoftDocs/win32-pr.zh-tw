---
description: Windows Vista 引進了新的儲存案例和新的使用者設定檔命名空間。
title: 已知的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973493"
---
# <a name="known-folders"></a><span data-ttu-id="1fd95-103">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="1fd95-103">Known Folders</span></span>

<span data-ttu-id="1fd95-104">Windows Vista 引進了新的儲存案例和新的使用者設定檔命名空間。</span><span class="sxs-lookup"><span data-stu-id="1fd95-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="1fd95-105">為了解決這些新的因素，已取代以 [**CSIDL**](csidl.md) 值參照標準資料夾的較舊系統。</span><span class="sxs-lookup"><span data-stu-id="1fd95-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="1fd95-106">在 Windows Vista 中，這些資料夾是由一組新的 GUID 值所參考，稱為已知的資料夾識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fd95-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="1fd95-107">已知的資料夾系統提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="1fd95-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="1fd95-108">獨立軟體廠商 (Isv) 可以自行擴充已知的資料夾識別碼集。</span><span class="sxs-lookup"><span data-stu-id="1fd95-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="1fd95-109">他們可以定義資料夾、提供其識別碼，並向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="1fd95-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="1fd95-110">無法擴充 CSIDL 值。</span><span class="sxs-lookup"><span data-stu-id="1fd95-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="1fd95-111">系統上所有已知的資料夾都可以列舉。</span><span class="sxs-lookup"><span data-stu-id="1fd95-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="1fd95-112">沒有任何 API 提供這種 CSIDL 值的功能。</span><span class="sxs-lookup"><span data-stu-id="1fd95-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="1fd95-113">如需詳細資訊，請參閱 [**IKnownFolderManager：： GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) 。</span><span class="sxs-lookup"><span data-stu-id="1fd95-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="1fd95-114">ISV 新增的已知資料夾可以新增自訂屬性，讓它解釋其用途和預定用途。</span><span class="sxs-lookup"><span data-stu-id="1fd95-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="1fd95-115">許多已知的資料夾都可以重新導向至新的位置，包括網路位置。</span><span class="sxs-lookup"><span data-stu-id="1fd95-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="1fd95-116">在 CSIDL 系統下，只能重新導向 **我的檔** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1fd95-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="1fd95-117">已知的資料夾可以有自訂處理常式，可在建立或刪除期間使用。</span><span class="sxs-lookup"><span data-stu-id="1fd95-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="1fd95-118">使用 CSIDL 值的 CSIDL 系統和 Api 仍支援相容性。</span><span class="sxs-lookup"><span data-stu-id="1fd95-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="1fd95-119">但是，不建議在任何新的開發中使用它們。</span><span class="sxs-lookup"><span data-stu-id="1fd95-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="1fd95-120">下列主題討論已知資料夾系統的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1fd95-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="1fd95-121">使用應用程式中的已知資料夾</span><span class="sxs-lookup"><span data-stu-id="1fd95-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="1fd95-122">如何使用自訂資料夾擴充已知資料夾</span><span class="sxs-lookup"><span data-stu-id="1fd95-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="1fd95-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="1fd95-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="1fd95-124">下列參考頁面說明 Win32 已知資料夾函式，可用來取出已知資料夾的位置，或將其重新導向至新的位置。</span><span class="sxs-lookup"><span data-stu-id="1fd95-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="1fd95-125">這些函式會取代較舊的 Win32 函數。</span><span class="sxs-lookup"><span data-stu-id="1fd95-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="1fd95-126">系統會提供新的函式，將對等的行為提供給舊的函式，但元件物件模型也會複製每個新函數， (COM) API。</span><span class="sxs-lookup"><span data-stu-id="1fd95-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="1fd95-127">New 函式</span><span class="sxs-lookup"><span data-stu-id="1fd95-127">New Function</span></span>                                             | <span data-ttu-id="1fd95-128">取代</span><span class="sxs-lookup"><span data-stu-id="1fd95-128">Replaces</span></span>                                           | <span data-ttu-id="1fd95-129">COM 對等專案</span><span class="sxs-lookup"><span data-stu-id="1fd95-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="1fd95-130">**SHGetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="1fd95-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="1fd95-132">**IKnownFolder：： GetPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="1fd95-133">**SHGetKnownFolderIDList**</span><span class="sxs-lookup"><span data-stu-id="1fd95-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="1fd95-134">**SHGetFolderLocation**</span><span class="sxs-lookup"><span data-stu-id="1fd95-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="1fd95-135">**IKnownFolder::GetIDList**</span><span class="sxs-lookup"><span data-stu-id="1fd95-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="1fd95-136">**SHSetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="1fd95-137">**SHSetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="1fd95-138">**IKnownFolder::SetPath**</span><span class="sxs-lookup"><span data-stu-id="1fd95-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="1fd95-139">下列參考頁面說明 COM 已知的資料夾 Api，其提供上列 Win32 Api 的所有功能，並新增列舉所有已知資料夾的功能、存取已知的資料夾屬性，以及延伸標準的已知資料夾集。</span><span class="sxs-lookup"><span data-stu-id="1fd95-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="1fd95-140">**IKnownFolder**</span><span class="sxs-lookup"><span data-stu-id="1fd95-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="1fd95-141">**IKnownFolderManager**</span><span class="sxs-lookup"><span data-stu-id="1fd95-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="1fd95-142">示範已知資料夾 Api 的 c + + 範例包含在 Windows 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="1fd95-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1fd95-143">當您在電腦上安裝 Windows SDK 之後，就可以在% ProgramFiles% \\ Microsoft sdk \\ Windows \\ 6.0 \\ 範例 \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders 中找到此範例。</span><span class="sxs-lookup"><span data-stu-id="1fd95-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd95-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fd95-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1fd95-145">[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fd95-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
