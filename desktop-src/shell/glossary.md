---
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
title: Shell 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319135"
---
# <a name="shell-glossary"></a><span data-ttu-id="6a334-103">Shell 詞彙</span><span class="sxs-lookup"><span data-stu-id="6a334-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="6a334-104">A</span><span class="sxs-lookup"><span data-stu-id="6a334-104">A</span></span>

<dl> <dt>

<span data-ttu-id="6a334-105">**關聯**</span><span class="sxs-lookup"><span data-stu-id="6a334-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-106">副檔名的對應 (例如，mp3) 或通訊協定 (例如，HTTP) 為程式設計識別碼 (ProgID) 。</span><span class="sxs-lookup"><span data-stu-id="6a334-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="6a334-107">這項對應會儲存在登錄中，作為每一使用者的每一電腦的回復設定。</span><span class="sxs-lookup"><span data-stu-id="6a334-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="6a334-108">參與預設程式系統的應用程式，會設定副檔名或通訊協定的關聯對應，以指向它們所擁有的 ProgID 金鑰。</span><span class="sxs-lookup"><span data-stu-id="6a334-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-109">**關聯陣列**</span><span class="sxs-lookup"><span data-stu-id="6a334-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-110">登錄位置的排序清單，用來儲存專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6a334-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="6a334-111">例如，.jpg 檔案在預設的 Windows 系統上具有下列關聯陣列： "HKCR \\ jpgfile"、"HKCR \\ SystemFileAssociations \\ .jpg"、"HKCR \\ SystemFileAssociations \\ image"、"HKCR \\ \* "、"HKCR \\ AllFileSystemObjects"。</span><span class="sxs-lookup"><span data-stu-id="6a334-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="6a334-112">B</span><span class="sxs-lookup"><span data-stu-id="6a334-112">B</span></span>

<dl> <dt>

<span data-ttu-id="6a334-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="6a334-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-114">載入或關聯程式碼與資料。</span><span class="sxs-lookup"><span data-stu-id="6a334-114">To load or associate code with data.</span></span> <span data-ttu-id="6a334-115">例如，處理常式可能會與 Shell 資料來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="6a334-116">C</span><span class="sxs-lookup"><span data-stu-id="6a334-116">C</span></span>

<dl> <dt>

<span data-ttu-id="6a334-117">**正式名稱**</span><span class="sxs-lookup"><span data-stu-id="6a334-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-118">資源的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="6a334-118">The unique name of a resource.</span></span> <span data-ttu-id="6a334-119">標準表示「根據規則」。</span><span class="sxs-lookup"><span data-stu-id="6a334-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="6a334-120">請參閱：標準動詞名稱。</span><span class="sxs-lookup"><span data-stu-id="6a334-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-121">**標準動詞名稱**</span><span class="sxs-lookup"><span data-stu-id="6a334-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-122">非語言相關名稱，不論使用者介面中的當地語系化字串為何，都可以用程式設計方式來參考動詞。</span><span class="sxs-lookup"><span data-stu-id="6a334-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="6a334-123">請參閱：標準名稱、動詞。</span><span class="sxs-lookup"><span data-stu-id="6a334-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-124">**container**</span><span class="sxs-lookup"><span data-stu-id="6a334-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-125">可包含其他專案的 Shell 專案類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="6a334-126">容器中的專案會使用 Shell 資料來源公開給 Shell 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6a334-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="6a334-127">範例包括資料夾、磁片磁碟機、網路伺服器，以及副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="6a334-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="6a334-128">另請參閱： Shell 資料來源、資料夾、Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-129">**content**</span><span class="sxs-lookup"><span data-stu-id="6a334-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-130">與可編制索引之 Shell 專案或內容來源相關聯的文字和屬性。</span><span class="sxs-lookup"><span data-stu-id="6a334-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-131">**內容來源**</span><span class="sxs-lookup"><span data-stu-id="6a334-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-132">可由索引子存取的專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="6a334-133">內容來源可透過 URL 定址，並由通訊協定處理常式提供給索引子。</span><span class="sxs-lookup"><span data-stu-id="6a334-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="6a334-134">範例包括：檔案系統檔案和資料夾、Microsoft Outlook 專案和資料夾、資料庫記錄和 Microsoft SharePoint 儲存的專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="6a334-135">您可以藉由執行 Shell 資料來源，將內容來源公開為 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="6a334-136">另請參閱： content、Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-137">**content view (內容檢視)**</span><span class="sxs-lookup"><span data-stu-id="6a334-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-138">在 Windows 7 和更新) 版本中提供的 Windows 檔案總管 (視圖，會根據清單的副檔名或種類關聯，顯示清單中每個專案的最相關內容。</span><span class="sxs-lookup"><span data-stu-id="6a334-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="6a334-139">當視窗大小減少時，內容視圖會使用調整大小的邏輯，以確保最重要的屬性仍然具有可清楚讀取的空間。</span><span class="sxs-lookup"><span data-stu-id="6a334-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="6a334-140">另請參閱：版面配置模式、種類、種類關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-141">**內容視圖模式**</span><span class="sxs-lookup"><span data-stu-id="6a334-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-142">請參閱： content view 的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-143">**內容功能表**</span><span class="sxs-lookup"><span data-stu-id="6a334-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-144">這個詞彙有時候是用來表示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="6a334-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="6a334-145">請參閱：快捷方式功能表的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-146">**內容功能表處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-147">這個詞彙有時候是用來表示快速鍵功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="6a334-148">請參閱：快捷方式功能表處理常式的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="6a334-149">D</span><span class="sxs-lookup"><span data-stu-id="6a334-149">D</span></span>

<dl> <dt>

<span data-ttu-id="6a334-150">**資料物件處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-151">為數據物件提供額外剪貼簿格式的處理常式， (IDataObject 的專案) 。</span><span class="sxs-lookup"><span data-stu-id="6a334-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="6a334-152">資料物件用於拖放和複製/貼上案例中。</span><span class="sxs-lookup"><span data-stu-id="6a334-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-153">**資料來源**</span><span class="sxs-lookup"><span data-stu-id="6a334-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-154">這個詞彙有時候是用來表示資料存放區或 Shell 資料來源。</span><span class="sxs-lookup"><span data-stu-id="6a334-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="6a334-155">請參閱：資料存放區、Shell 資料來源的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-156">**資料存放區**</span><span class="sxs-lookup"><span data-stu-id="6a334-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-157">資料存放庫。</span><span class="sxs-lookup"><span data-stu-id="6a334-157">A repository of data.</span></span> <span data-ttu-id="6a334-158">資料存放區可以使用 Shell 資料來源，以容器的形式公開給 Shell 程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="6a334-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="6a334-159">您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="6a334-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-160">**桌面電腦群組合**</span><span class="sxs-lookup"><span data-stu-id="6a334-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-161">Windows Vista 功能，可讓個別視窗繪製至視訊記憶體中的螢幕表面，而不是直接繪製到主要顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="6a334-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-162">**document**</span><span class="sxs-lookup"><span data-stu-id="6a334-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-163">包含文字以及可以實作為 IFilter 介面的 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-164">**捨棄處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-165">可讓特定專案類型支援拖放和複製/貼上案例的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-166">**放置目標**</span><span class="sxs-lookup"><span data-stu-id="6a334-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-167">拖放到檔案上的資料物件。</span><span class="sxs-lookup"><span data-stu-id="6a334-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="6a334-168">另請參閱：資料處理程式、drop handler。</span><span class="sxs-lookup"><span data-stu-id="6a334-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-169">**動態動詞**</span><span class="sxs-lookup"><span data-stu-id="6a334-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-170">相依于 Shell 專案或系統狀態的動詞;專案的外觀是以狀態為基礎，而且需要執行中的程式碼判斷專案是否應該出現。</span><span class="sxs-lookup"><span data-stu-id="6a334-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="6a334-171">另請參閱：快捷方式功能表處理常式、靜態動詞命令、動詞。</span><span class="sxs-lookup"><span data-stu-id="6a334-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="6a334-172">E</span><span class="sxs-lookup"><span data-stu-id="6a334-172">E</span></span>

<dl> <dt>

<span data-ttu-id="6a334-173">**Explorer 命令**</span><span class="sxs-lookup"><span data-stu-id="6a334-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-174">可以在 Windows 檔案總管視窗頂端附近顯示為按鈕的物件，以提供該視窗中專案和容器的功能。</span><span class="sxs-lookup"><span data-stu-id="6a334-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="6a334-175">Shell 資料來源為特定的容器專案提供 Windows 檔案總管的命令物件。</span><span class="sxs-lookup"><span data-stu-id="6a334-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="6a334-176">命令有時候會當做動詞使用。</span><span class="sxs-lookup"><span data-stu-id="6a334-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="6a334-177">F</span><span class="sxs-lookup"><span data-stu-id="6a334-177">F</span></span>

<dl> <dt>

<span data-ttu-id="6a334-178">**檔案關聯**</span><span class="sxs-lookup"><span data-stu-id="6a334-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-179">請參閱：檔案類型關聯的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-180">**檔案格式**</span><span class="sxs-lookup"><span data-stu-id="6a334-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-181">儲存在具有記載格式規格之檔案中的資料格式。</span><span class="sxs-lookup"><span data-stu-id="6a334-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="6a334-182">範例包括 OLE e、OPC、XML、ZIP 和其他知名的檔案格式規格。</span><span class="sxs-lookup"><span data-stu-id="6a334-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="6a334-183">檔案類型建立者通常會使用現有的檔案格式做為新檔案類型的基礎。</span><span class="sxs-lookup"><span data-stu-id="6a334-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="6a334-184">檔案格式可以只是未具現化為檔案類型的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-185">**檔案格式處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-186">此詞彙是檔案類型處理常式的同義字。</span><span class="sxs-lookup"><span data-stu-id="6a334-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="6a334-187">請參閱的定義：檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-188">**副檔名**</span><span class="sxs-lookup"><span data-stu-id="6a334-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-189">檔案系統專案之檔案類型的主要指標，是最後一個點後面的檔案名部分。</span><span class="sxs-lookup"><span data-stu-id="6a334-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="6a334-190">副檔名不能包含空格或非 ASCII 字元，而且只會套用至)  (不是資料夾的檔案。</span><span class="sxs-lookup"><span data-stu-id="6a334-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="6a334-191">使用不區分大小寫或地區設定的比較函式來比較副檔名。</span><span class="sxs-lookup"><span data-stu-id="6a334-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="6a334-192">另請參閱：檔案格式、檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-193">**檔案類型**</span><span class="sxs-lookup"><span data-stu-id="6a334-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-194">特定的副檔名值（例如 ".htm" 或 ".jpg"），可定義屬於相同類型且擁有一組通用關聯的檔案類別。</span><span class="sxs-lookup"><span data-stu-id="6a334-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="6a334-195">另請參閱：種類、檔案類型關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-196">**檔案類型關聯**</span><span class="sxs-lookup"><span data-stu-id="6a334-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-197">針對特定的副檔名，定義可以註冊處理常式和其他屬性的關聯陣列元素。</span><span class="sxs-lookup"><span data-stu-id="6a334-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="6a334-198">請參閱：關聯陣列、檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-199">**自訂檔案類型**</span><span class="sxs-lookup"><span data-stu-id="6a334-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-200">此關聯可讓 Shell 自訂 Shell 如何處理檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="6a334-201">檔案類型自訂包括：指定在按兩下時用來開啟檔案的應用程式、將命令新增至檔案類型的快捷方式功能表、指定自訂圖示、指定要與檔案類型相關聯的 MIME 內容類型、指定可見的類型，以及使用 [開啟檔案] 對話方塊指定與檔案類型相關聯的一或多個應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a334-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="6a334-202">另請參閱： PerceivedType。</span><span class="sxs-lookup"><span data-stu-id="6a334-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-203">**檔案類型處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-204">為檔案類型註冊的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-204">A handler registered for a file type.</span></span> <span data-ttu-id="6a334-205">另請參閱：處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-206">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="6a334-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-207">請參閱： container 的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-208">**完整 PIDL**</span><span class="sxs-lookup"><span data-stu-id="6a334-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-209">可唯一描述相對於桌面資料夾之物件的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="6a334-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="6a334-210">H</span><span class="sxs-lookup"><span data-stu-id="6a334-210">H</span></span>

<dl> <dt>

<span data-ttu-id="6a334-211">**處理器**</span><span class="sxs-lookup"><span data-stu-id="6a334-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-212">提供 Shell 專案功能的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="6a334-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="6a334-213">大部分的 Shell 資料來源都會提供可延伸的系統，以便將處理常式系結至專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="6a334-214">例如，檔系統資料夾使用關聯系統來查閱特定檔案類型的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="6a334-215">另請參閱：檔案關聯、檔案類型、檔案類型自訂。</span><span class="sxs-lookup"><span data-stu-id="6a334-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="6a334-216">I</span><span class="sxs-lookup"><span data-stu-id="6a334-216">I</span></span>

<dl> <dt>

<span data-ttu-id="6a334-217">**圖示處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-218">提供產生和快取專案圖示所需資訊的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="6a334-219">檔案系統資料存放區支援根據檔案類型載入專案的圖示處理常式，讓該處理常式能夠提供用於該檔案類型之所有實例的圖示。</span><span class="sxs-lookup"><span data-stu-id="6a334-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-220">**提示處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-221">當使用者將滑鼠指標停留在使用者介面物件上方時，提供快顯文字的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-222">**item**</span><span class="sxs-lookup"><span data-stu-id="6a334-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-223">請參閱： Shell 專案的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-224">**item 類別**</span><span class="sxs-lookup"><span data-stu-id="6a334-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-225">請參閱：檔案類型的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-226">**專案識別碼清單**</span><span class="sxs-lookup"><span data-stu-id="6a334-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-227">一或多個 SHITEMID 結構的序列，可唯一定義相對於某個根物件的物件。</span><span class="sxs-lookup"><span data-stu-id="6a334-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="6a334-228">K</span><span class="sxs-lookup"><span data-stu-id="6a334-228">K</span></span>

<dl> <dt>

<span data-ttu-id="6a334-229">**種類**</span><span class="sxs-lookup"><span data-stu-id="6a334-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-230">提供使用者易記種類名稱的屬性，而且可以與屬性清單和配置模式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="6a334-231">Windows Vista 引進了一種方式，是為了表達更適合使用者的檔案類型概念，並將其定義為多重值字串屬性， (標準字串值) ，因此您可以有「音訊」、「影片」或「連結; 檔」種類的值。</span><span class="sxs-lookup"><span data-stu-id="6a334-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="6a334-232">某些使用者易記的種類名稱已與屬性和配置模式相關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="6a334-233">例如，與 [>ument] 相關聯的專案與 [圖片] 和 [Kind.Doc] 相關聯的專案會顯示不同的屬性，即使它們位於相同的視圖中也一樣。</span><span class="sxs-lookup"><span data-stu-id="6a334-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="6a334-234">每個專案種類都可以與四種獨特的版面配置模式之一建立關聯，以定義每個專案和其配置所顯示的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="6a334-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="6a334-235">另請參閱：種類關聯、內容視圖、版面配置模式。</span><span class="sxs-lookup"><span data-stu-id="6a334-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="6a334-236">L</span><span class="sxs-lookup"><span data-stu-id="6a334-236">L</span></span>

<dl> <dt>

<span data-ttu-id="6a334-237">**版面配置模式**</span><span class="sxs-lookup"><span data-stu-id="6a334-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-238">顯示內容之數種相片順序的其中一種。</span><span class="sxs-lookup"><span data-stu-id="6a334-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="6a334-239">在 Windows 7 和更新版本中，當您要註冊新的檔案類型時，可以使用內容視圖來註冊檔案類型的自訂屬性清單和配置模式。</span><span class="sxs-lookup"><span data-stu-id="6a334-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="6a334-240">您可以從四種不同的配置模式中選擇： Alpha (適用于檔搜尋結果，其中包含程式碼片段)  (、適用于程式碼片段) 的電子郵件搜尋結果、Gamma (類似于 Alpha，但有兩行配置（而不是四) ），而 Delta (則顯示許多較短的屬性，例如使用音樂和圖片) 。</span><span class="sxs-lookup"><span data-stu-id="6a334-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="6a334-241">另請參閱：內容視圖、種類、種類關聯。</span><span class="sxs-lookup"><span data-stu-id="6a334-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="6a334-242">M</span><span class="sxs-lookup"><span data-stu-id="6a334-242">M</span></span>

<dl> <dt>

<span data-ttu-id="6a334-243">**元資料處理程式**</span><span class="sxs-lookup"><span data-stu-id="6a334-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-244">這個詞彙有時候是用來表示屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="6a334-245">請參閱：屬性處理常式的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="6a334-246">N</span><span class="sxs-lookup"><span data-stu-id="6a334-246">N</span></span>

<dl> <dt>

<span data-ttu-id="6a334-247">**命名空間延伸模組**</span><span class="sxs-lookup"><span data-stu-id="6a334-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-248">請參閱： Shell 資料來源的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="6a334-249">O</span><span class="sxs-lookup"><span data-stu-id="6a334-249">O</span></span>

<dl> <dt>

<span data-ttu-id="6a334-250">**物件連結與嵌入資料庫 (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="6a334-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-251">一組標準的介面，可提供隨處存取不同來源的資訊來源，例如檔案系統、電子郵件資料夾和資料庫。</span><span class="sxs-lookup"><span data-stu-id="6a334-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="6a334-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-253">請參閱：物件連結與嵌入資料庫的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="6a334-254">P</span><span class="sxs-lookup"><span data-stu-id="6a334-254">P</span></span>

<dl> <dt>

<span data-ttu-id="6a334-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="6a334-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-256">廣泛分類的檔案格式類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-256">A broad category of file format types.</span></span> <span data-ttu-id="6a334-257">PerceivedType 是在 Windows XP 中引進，並支援一組有限的已知檔案類型 (範例包括影像、文字、音訊和壓縮檔案類型) 。</span><span class="sxs-lookup"><span data-stu-id="6a334-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="6a334-258">檔案類型（通常是公用檔案類型）也可以有察覺的型別。</span><span class="sxs-lookup"><span data-stu-id="6a334-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="6a334-259">例如，圖像檔案類型 .bmp、.png、.jpg 和 .gif 也是認知型別影像。</span><span class="sxs-lookup"><span data-stu-id="6a334-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="6a334-260">在程式設計層，PerceivedType 是以整數表示。</span><span class="sxs-lookup"><span data-stu-id="6a334-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="6a334-261">由於有使用種類和 PerceivedType 的程式碼，因此檔案格式擁有者必須註冊這兩者。</span><span class="sxs-lookup"><span data-stu-id="6a334-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="6a334-262">例如，「全部播放」取決於 PerceivedType。</span><span class="sxs-lookup"><span data-stu-id="6a334-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="6a334-263">另請參閱：檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6a334-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-264">**預覽處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-265">此處理程式可快速產生唯讀、簡單的 Shell 專案查看，以顯示在 Windows 檔案總管預覽窗格中。</span><span class="sxs-lookup"><span data-stu-id="6a334-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-266">**屬性處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-267">將儲存在檔案中的資料轉譯成可辨識之結構化架構的處理常式，可由 Windows 檔案總管、Windows Search 和其他應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="6a334-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="6a334-268">這些系統接著可以與屬性處理常式互動，以在檔案中寫入和讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="6a334-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="6a334-269">轉譯的資料包含詳細資料檢視、提示、詳細資料窗格、屬性頁等等。</span><span class="sxs-lookup"><span data-stu-id="6a334-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="6a334-270">每個屬性處理常式都與特定檔案類型相關聯，該檔案類型是由副檔名所識別。</span><span class="sxs-lookup"><span data-stu-id="6a334-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="6a334-271">另請參閱：屬性系統。</span><span class="sxs-lookup"><span data-stu-id="6a334-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-272">**屬性工作表處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-273">用來建立自訂屬性工作表的處理常式，該工作表包含允許與檔案類型進行自訂互動的 UI 圖片和控制項。</span><span class="sxs-lookup"><span data-stu-id="6a334-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-274">**屬性系統**</span><span class="sxs-lookup"><span data-stu-id="6a334-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-275">資料定義的可延伸讀取/寫入系統，使用實作為成對名稱/值的屬性。</span><span class="sxs-lookup"><span data-stu-id="6a334-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="6a334-276">另請參閱：屬性處理常式、Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-277">**屬性值**</span><span class="sxs-lookup"><span data-stu-id="6a334-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-278">與 Shell 專案的屬性名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="6a334-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="6a334-279">例如，「作者」、「大小」和「拍攝日期」都是屬性。</span><span class="sxs-lookup"><span data-stu-id="6a334-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="6a334-280">屬性值會以 PROPVARIANT 結構表示。</span><span class="sxs-lookup"><span data-stu-id="6a334-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-281">**通訊協定處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-282">存取內容來源並為指定的通訊協定和 URL 提供 IUrlAccessor 物件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="6a334-283">通訊協定處理常式可延伸 Windows Search 的功能，並可提供變更通知給索引子。</span><span class="sxs-lookup"><span data-stu-id="6a334-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="6a334-284">需要不同的通訊協定處理常式來編制特定類型的資料存放區索引。</span><span class="sxs-lookup"><span data-stu-id="6a334-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="6a334-285">若要提供合理的使用者體驗，您也必須提供資料存放區的 Shell 資料來源，以及執行您的通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="6a334-286">通訊協定處理常式會將資料存放區中的專案公開給索引子，而 Shell 資料來源則會將資料存放區中的專案公開給 Shell。</span><span class="sxs-lookup"><span data-stu-id="6a334-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="6a334-287">R</span><span class="sxs-lookup"><span data-stu-id="6a334-287">R</span></span>

<dl> <dt>

<span data-ttu-id="6a334-288">**相對 PIDL**</span><span class="sxs-lookup"><span data-stu-id="6a334-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-289">相對於 [桌面] 資料夾以外的 shell 命名空間中某個根物件的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="6a334-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="6a334-290">這通常是專案的父資料夾。</span><span class="sxs-lookup"><span data-stu-id="6a334-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="6a334-291">S</span><span class="sxs-lookup"><span data-stu-id="6a334-291">S</span></span>

<dl> <dt>

<span data-ttu-id="6a334-292">**Shell 資料來源**</span><span class="sxs-lookup"><span data-stu-id="6a334-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-293">用來擴充 Shell 命名空間和公開資料存放區中專案的元件。</span><span class="sxs-lookup"><span data-stu-id="6a334-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="6a334-294">在過去，Shell 資料來源稱為 Shell 命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6a334-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="6a334-295">另請參閱：容器、處理常式、Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-296">**Shell 延伸模組**</span><span class="sxs-lookup"><span data-stu-id="6a334-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-297">這個詞彙有時候是用來表示檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6a334-298">請參閱的定義：檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-299">**Shell 擴充處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-300">這個詞彙有時候是用來表示檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6a334-301">請參閱的定義：檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-302">**Shell 處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-303">這個詞彙有時候是用來表示檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6a334-304">請參閱的定義：檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-305">**Shell 專案**</span><span class="sxs-lookup"><span data-stu-id="6a334-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-306">單一內容片段。</span><span class="sxs-lookup"><span data-stu-id="6a334-306">A single piece of content.</span></span> <span data-ttu-id="6a334-307">某些 Shell 專案為內容來源，有些則不是。</span><span class="sxs-lookup"><span data-stu-id="6a334-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="6a334-308">例如，一個資料夾是一個內容來源，但是 .jpg 檔案並不是。</span><span class="sxs-lookup"><span data-stu-id="6a334-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="6a334-309">檔案類型處理常式會公開 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="6a334-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="6a334-310">在某些內容中，會使用「專案」來區別容器與 noncontainers。</span><span class="sxs-lookup"><span data-stu-id="6a334-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="6a334-311">另請參閱：容器、內容來源、檔案類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-312">**Shell 命名空間延伸模組**</span><span class="sxs-lookup"><span data-stu-id="6a334-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-313">這個詞彙有時候是用來表示 Shell 資料來源。</span><span class="sxs-lookup"><span data-stu-id="6a334-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="6a334-314">請參閱： Shell 資料來源的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-315">**快速鍵功能表**</span><span class="sxs-lookup"><span data-stu-id="6a334-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-316">使用者介面，用來顯示與使用者介面專案（例如檔案或資料夾）相關聯的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="6a334-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-317">**快速鍵功能表處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-318">為專案或專案加入動詞的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="6a334-319">這些動詞通常會顯示在快捷方式功能表中。</span><span class="sxs-lookup"><span data-stu-id="6a334-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="6a334-320">另請參閱：快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="6a334-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-321">**簡單 PIDL**</span><span class="sxs-lookup"><span data-stu-id="6a334-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-322">經過剖析而沒有磁片驗證的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="6a334-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-323">**靜態動詞**</span><span class="sxs-lookup"><span data-stu-id="6a334-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-324">適用于 Shell 專案的動詞，不需要檢查項目或系統的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6a334-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="6a334-325">靜態動詞命令是以專案之相關專案的靜態註冊為基礎，而且不會變更。</span><span class="sxs-lookup"><span data-stu-id="6a334-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="6a334-326">T</span><span class="sxs-lookup"><span data-stu-id="6a334-326">T</span></span>

<dl> <dt>

<span data-ttu-id="6a334-327">**縮圖處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-328">提供靜態影像以表示 Shell 專案的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-329">**縮圖提供者**</span><span class="sxs-lookup"><span data-stu-id="6a334-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-330">這個詞彙有時候是用來表示縮圖處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="6a334-331">請參閱：縮圖處理常式的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="6a334-332">U</span><span class="sxs-lookup"><span data-stu-id="6a334-332">U</span></span>

<dl> <dt>

<span data-ttu-id="6a334-333">**使用者易記種類名稱**</span><span class="sxs-lookup"><span data-stu-id="6a334-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-334">請參閱：種類的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="6a334-335">V</span><span class="sxs-lookup"><span data-stu-id="6a334-335">V</span></span>

<dl> <dt>

<span data-ttu-id="6a334-336">**動詞命令**</span><span class="sxs-lookup"><span data-stu-id="6a334-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-337">可由 Shell 專案呼叫的個別動作。</span><span class="sxs-lookup"><span data-stu-id="6a334-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="6a334-338">範例包括 [開啟] 和 [列印]。</span><span class="sxs-lookup"><span data-stu-id="6a334-338">Examples include open and print.</span></span> <span data-ttu-id="6a334-339">動詞有時也稱為命令或 task。</span><span class="sxs-lookup"><span data-stu-id="6a334-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="6a334-340">另請參閱：動態動詞、快捷方式功能表處理常式、靜態動詞。</span><span class="sxs-lookup"><span data-stu-id="6a334-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="6a334-341">**動詞處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a334-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="6a334-342">這個詞彙有時候是用來表示快速鍵功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a334-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="6a334-343">請參閱：快捷方式功能表處理常式的定義。</span><span class="sxs-lookup"><span data-stu-id="6a334-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



