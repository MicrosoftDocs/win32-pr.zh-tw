---
description: 關聯陣列是登錄位置的排序清單，可用來儲存專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。
title: 關聯陣列
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112772"
---
# <a name="association-arrays"></a><span data-ttu-id="607fb-103">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-103">Association Arrays</span></span>

<span data-ttu-id="607fb-104">關聯陣列是登錄位置的排序清單，可用來儲存專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="607fb-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="607fb-105">Shell 會使用關聯陣列來查詢一組預先定義的登錄位置，其中可能包含 Shell 專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="607fb-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="607fb-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="607fb-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="607fb-107">關於關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="607fb-108">查詢關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="607fb-109">使用特定 Shell 資料來源的關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="607fb-110">Shell 資料來源關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="607fb-111">其他資源</span><span class="sxs-lookup"><span data-stu-id="607fb-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="607fb-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="607fb-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="607fb-113">關於關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-113">About Association Arrays</span></span>

<span data-ttu-id="607fb-114">關聯陣列是登錄位置的排序清單，其中包含專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="607fb-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="607fb-115">此專案類型的相關資訊可以在明確的不同層級進行註冊。</span><span class="sxs-lookup"><span data-stu-id="607fb-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="607fb-116">例如，您可以註冊只會顯示特定檔案類型的動詞 (例如 .jpg) ，或所有具有相同 system.string 的專案 (例如，system.string = picture) ，或所有專案的所有專案。</span><span class="sxs-lookup"><span data-stu-id="607fb-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="607fb-117">Shell 會使用關聯陣列來查詢一組預先定義的登錄位置，其中可能包含專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="607fb-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="607fb-118">您可以使用關聯陣列 Api，從登錄子機碼中取出包含所要求資訊的單一值，而該值來自陣列中提供它的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="607fb-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="607fb-119">例如，預設圖示值會以這種方式抓取。</span><span class="sxs-lookup"><span data-stu-id="607fb-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="607fb-120">關聯陣列也可以用來抓取儲存在登錄子機碼中的一組值。</span><span class="sxs-lookup"><span data-stu-id="607fb-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="607fb-121">例如，動詞清單是根據在所有子機碼下註冊的動詞來建立。</span><span class="sxs-lookup"><span data-stu-id="607fb-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="607fb-122">在 Shell 查詢一組預先定義的登錄位置以取得 Shell 專案的相關資訊之後，它會將登錄位置從最特定的位置排列到最一般的陣列中。</span><span class="sxs-lookup"><span data-stu-id="607fb-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="607fb-123">因為關聯陣列是已排序的清單，所以會為應用程式開發人員提供一個機制，將資訊加入至將針對特定類型的專案傳回的登錄中。</span><span class="sxs-lookup"><span data-stu-id="607fb-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="607fb-124">同樣地，當這些專案在更一般的位置註冊時，關聯陣列可讓應用程式開發人員將資訊新增至特定專案群組的登錄中。</span><span class="sxs-lookup"><span data-stu-id="607fb-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="607fb-125">此邏輯會通知您有關登錄中最適當位置的決定，以儲存 Shell 專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="607fb-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="607fb-126">在預設的 Windows 系統上，.jpg 檔案具有下列關聯陣列：</span><span class="sxs-lookup"><span data-stu-id="607fb-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="607fb-127">**HKEY \_類別 \_ 根** \\ **jpgfile**</span><span class="sxs-lookup"><span data-stu-id="607fb-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="607fb-128">**HKEY \_類別 \_ 根目錄** \\ **SystemFileAssociations** \\ **.jpg**</span><span class="sxs-lookup"><span data-stu-id="607fb-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="607fb-129">**HKEY \_類別 \_ 根** \\ **映射**</span><span class="sxs-lookup"><span data-stu-id="607fb-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="607fb-130">**HKEY \_類別 \_ 根目錄** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="607fb-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="607fb-131">_ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="607fb-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="607fb-132">如需註冊關聯陣列的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="607fb-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="607fb-133">查詢關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-133">Querying Association Arrays</span></span>

<span data-ttu-id="607fb-134">有 Shell Api 可從某個範圍的登錄子機碼取得資訊，從最特定的登錄子機碼到所有登錄子機碼的資訊超集合。</span><span class="sxs-lookup"><span data-stu-id="607fb-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="607fb-135">關聯陣列最常見的用法是查詢 Shell 從陣列中具有所要求資訊的最特定元素傳回的單一值。</span><span class="sxs-lookup"><span data-stu-id="607fb-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="607fb-136">下列程式碼範例示範如何執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="607fb-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="607fb-137">下列 Api 可用來查詢關聯陣列，或是用來建立可查詢的關聯陣列 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 物件：</span><span class="sxs-lookup"><span data-stu-id="607fb-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="607fb-138">Windows Vista) 之前的 [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (</span><span class="sxs-lookup"><span data-stu-id="607fb-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="607fb-139">**AssocCreateForClasses**</span><span class="sxs-lookup"><span data-stu-id="607fb-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="607fb-140">**AssocQueryString**</span><span class="sxs-lookup"><span data-stu-id="607fb-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="607fb-141">使用特定 Shell 資料來源的關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="607fb-142">每個 Shell 資料來源都會定義其專案的關聯陣列。</span><span class="sxs-lookup"><span data-stu-id="607fb-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="607fb-143">定義關聯陣列通常是專案類型的函式。</span><span class="sxs-lookup"><span data-stu-id="607fb-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="607fb-144">Shell 資料來源實作者應定義並記載關聯陣列，讓應用程式能夠擴充這些類型的行為，例如註冊動詞或其他資訊。</span><span class="sxs-lookup"><span data-stu-id="607fb-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="607fb-145">應用程式可以根據將資料加入至關聯陣列子機碼（例如新增專案的動詞）來擴充專案的行為。</span><span class="sxs-lookup"><span data-stu-id="607fb-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="607fb-146">檔案系統資料來源會根據下列登錄子機碼和特殊 Progid 來建立檔案的關聯陣列：</span><span class="sxs-lookup"><span data-stu-id="607fb-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="607fb-147">如果檔案具有已註冊的 ProgID，則會使用 **HKEY \_ 類別的 \_ 根目錄** \\ *ProgID* 。</span><span class="sxs-lookup"><span data-stu-id="607fb-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="607fb-148">否則會使用 **HKEY \_ 類別 \_ 根** \\ **未知**。</span><span class="sxs-lookup"><span data-stu-id="607fb-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="607fb-149">副檔名是在 **HKEY \_ 類別 \_ 根** \\ **SystemFileAssociations** \\ *. fileExtension* 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="607fb-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="607fb-150">下表顯示特殊的 Progid。</span><span class="sxs-lookup"><span data-stu-id="607fb-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="607fb-151">特殊 progID</span><span class="sxs-lookup"><span data-stu-id="607fb-151">Special progID</span></span>                                    | <span data-ttu-id="607fb-152">Description</span><span class="sxs-lookup"><span data-stu-id="607fb-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="607fb-153">**HKEY \_類別 \_ 根目錄** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="607fb-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="607fb-154">所有檔案 (非資料夾) </span><span class="sxs-lookup"><span data-stu-id="607fb-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="607fb-155">_ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="607fb-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="607fb-156">檔案和檔系統資料夾</span><span class="sxs-lookup"><span data-stu-id="607fb-156">Files and file system folders</span></span> |
    | <span data-ttu-id="607fb-157">**HKEY \_類別 \_ 根目錄** \\ </span><span class="sxs-lookup"><span data-stu-id="607fb-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="607fb-158">檔系統資料夾</span><span class="sxs-lookup"><span data-stu-id="607fb-158">File system folders</span></span>           |
    | <span data-ttu-id="607fb-159">**HKEY \_類別 \_ 根** \\ **資料夾**</span><span class="sxs-lookup"><span data-stu-id="607fb-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="607fb-160">Shell 容器</span><span class="sxs-lookup"><span data-stu-id="607fb-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="607fb-161">Shell 資料來源關聯陣列</span><span class="sxs-lookup"><span data-stu-id="607fb-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="607fb-162">下列清單表示某些 Shell 資料存放區關聯陣列，可用於本主題中所述的用途：</span><span class="sxs-lookup"><span data-stu-id="607fb-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="607fb-163">**HKEY \_類別 \_ 根目錄** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="607fb-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="607fb-164">_ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="607fb-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="607fb-165">**HKEY \_類別 \_ 根目錄** \\ **Kind.Doc>ument**</span><span class="sxs-lookup"><span data-stu-id="607fb-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="607fb-166">**HKEY \_類別 \_ 根** \\ **結果**</span><span class="sxs-lookup"><span data-stu-id="607fb-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="607fb-167">**HKEY \_類別 \_ 根目錄** \\ **SystemFileAssociations** \\ **.docx**</span><span class="sxs-lookup"><span data-stu-id="607fb-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="607fb-168">**HKEY \_類別 \_ 根目錄** \\ **Word.Doc>ument 12**</span><span class="sxs-lookup"><span data-stu-id="607fb-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="607fb-169">可以用於 DBFolder (Shell 資料存放區（代表搜尋結果中的專案）和查詢型視圖) 的 shell 資料來源關聯陣列如下所示：</span><span class="sxs-lookup"><span data-stu-id="607fb-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="607fb-170">磁碟機</span><span class="sxs-lookup"><span data-stu-id="607fb-170">Drives</span></span>
-   <span data-ttu-id="607fb-171">網路</span><span class="sxs-lookup"><span data-stu-id="607fb-171">Network</span></span>
-   <span data-ttu-id="607fb-172">RegItems</span><span class="sxs-lookup"><span data-stu-id="607fb-172">RegItems</span></span>
-   <span data-ttu-id="607fb-173">範例：</span><span class="sxs-lookup"><span data-stu-id="607fb-173">Examples:</span></span>
    -   <span data-ttu-id="607fb-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="607fb-174">ContentView</span></span>
    -   <span data-ttu-id="607fb-175">動詞</span><span class="sxs-lookup"><span data-stu-id="607fb-175">Verbs</span></span>

<span data-ttu-id="607fb-176">其他常見的關聯陣列包括資料夾和印表機。</span><span class="sxs-lookup"><span data-stu-id="607fb-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="607fb-177">其他資源</span><span class="sxs-lookup"><span data-stu-id="607fb-177">Additional Resources</span></span>

-   <span data-ttu-id="607fb-178">若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](nse-implement.md)。</span><span class="sxs-lookup"><span data-stu-id="607fb-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="607fb-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="607fb-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="607fb-180">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="607fb-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="607fb-181">檔案類型</span><span class="sxs-lookup"><span data-stu-id="607fb-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="607fb-182">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="607fb-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="607fb-183">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="607fb-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="607fb-184">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="607fb-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="607fb-185">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="607fb-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="607fb-186">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="607fb-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="607fb-187">認知類型</span><span class="sxs-lookup"><span data-stu-id="607fb-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
