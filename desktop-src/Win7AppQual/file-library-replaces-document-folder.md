---
description: 檔案庫取代檔資料夾
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: 檔案庫取代檔資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088376"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="c3a73-103">檔案庫取代檔資料夾</span><span class="sxs-lookup"><span data-stu-id="c3a73-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c3a73-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="c3a73-104">Affected Platforms</span></span>

<span data-ttu-id="c3a73-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3a73-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="c3a73-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3a73-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="c3a73-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="c3a73-107">Feature Impact</span></span>

<span data-ttu-id="c3a73-108">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="c3a73-108">**Severity** - Medium</span></span>  
<span data-ttu-id="c3a73-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="c3a73-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="c3a73-110">Description</span><span class="sxs-lookup"><span data-stu-id="c3a73-110">Description</span></span>

<span data-ttu-id="c3a73-111">程式庫提供集中的類似資料夾體驗，可跨多個位置（本機和遠端）進行檔案儲存、搜尋和存取。</span><span class="sxs-lookup"><span data-stu-id="c3a73-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="c3a73-112">一般檔案對話方塊所使用的預設位置 (例如，[開啟] 和 [儲存) ] 已從 [檔] 資料夾變更為 [文件庫]。</span><span class="sxs-lookup"><span data-stu-id="c3a73-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="c3a73-113">消費者介面不會變更，但使用者現在可以使用各種排列檢視來查看、流覽和搜尋程式庫。</span><span class="sxs-lookup"><span data-stu-id="c3a73-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="c3a73-114">檔案將會儲存到程式庫預設儲存位置，除非使用者變更預設儲存位置或選擇不同的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c3a73-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="c3a73-115">開發人員可以建立自己的程式庫，或使用 IShellLibrary 介面將位置新增至現有的程式庫。</span><span class="sxs-lookup"><span data-stu-id="c3a73-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="c3a73-116">使用者可以使用已知的資料夾系統來尋找程式庫 (例如 FOLDERID \_ DocumentsLibrary) 。</span><span class="sxs-lookup"><span data-stu-id="c3a73-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="c3a73-117">影響的表現</span><span class="sxs-lookup"><span data-stu-id="c3a73-117">Manifestation of Impact</span></span>

<span data-ttu-id="c3a73-118">程式庫本身就是檔案，而不是資料夾。</span><span class="sxs-lookup"><span data-stu-id="c3a73-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="c3a73-119">因此，因為應用程式嘗試將檔案串連至檔案，所以路徑操作可能會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3a73-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="c3a73-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="c3a73-120">Solution</span></span>

<span data-ttu-id="c3a73-121">使用 IFileDialog 時，您必須使用 GetResult 方法，而不是 GetFolder 和 GetFilename 的組合，如同您在先前的作業系統版本中所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="c3a73-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="c3a73-122">盡可能使用 Shell Api 來與 Shell 命名空間中的專案互動和操作 (例如，IShellItem) 。</span><span class="sxs-lookup"><span data-stu-id="c3a73-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="c3a73-123">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="c3a73-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="c3a73-124">如果您想要建立自己的程式庫，或將位置新增至現有的程式庫，您必須使用 IShellLibrary API。</span><span class="sxs-lookup"><span data-stu-id="c3a73-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="c3a73-125">程式庫本身就是 Shell 資料夾，因此您可以像任何其他 Shell 資料夾一樣來列舉它們。</span><span class="sxs-lookup"><span data-stu-id="c3a73-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="c3a73-126">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="c3a73-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="c3a73-127">使用 [一般檔案] 對話方塊可確保使用者可以直接儲存在其程式庫中。</span><span class="sxs-lookup"><span data-stu-id="c3a73-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c3a73-128">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="c3a73-128">Links to Other Resources</span></span>

-   <span data-ttu-id="c3a73-129">**Windows 程式庫：**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="c3a73-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="c3a73-130">**與程式庫保持同步：**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="c3a73-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



