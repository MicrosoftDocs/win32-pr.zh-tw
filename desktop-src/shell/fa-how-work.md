---
description: 檔案關聯會定義 Shell 如何處理系統上的檔案類型。
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: 檔案關聯的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192705"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="3db21-103">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="3db21-103">How File Associations Work</span></span>

<span data-ttu-id="3db21-104">檔案關聯會定義 Shell 如何處理系統上的 [檔案類型](fa-file-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="3db21-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="3db21-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="3db21-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3db21-106">關於檔案關聯</span><span class="sxs-lookup"><span data-stu-id="3db21-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="3db21-107">當您應執行或修改檔案關聯時</span><span class="sxs-lookup"><span data-stu-id="3db21-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="3db21-108">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="3db21-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="3db21-109">其他資源</span><span class="sxs-lookup"><span data-stu-id="3db21-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3db21-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="3db21-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="3db21-111">關於檔案關聯</span><span class="sxs-lookup"><span data-stu-id="3db21-111">About File Associations</span></span>

<span data-ttu-id="3db21-112">檔案關聯控制下列功能：</span><span class="sxs-lookup"><span data-stu-id="3db21-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="3db21-113">當使用者按兩下檔案時，會啟動哪個應用程式。</span><span class="sxs-lookup"><span data-stu-id="3db21-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="3db21-114">預設會顯示檔案的圖示。</span><span class="sxs-lookup"><span data-stu-id="3db21-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="3db21-115">在 Windows 檔案總管中查看時，檔案類型的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="3db21-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="3db21-116">檔案的快捷方式功能表中會出現哪些命令。</span><span class="sxs-lookup"><span data-stu-id="3db21-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="3db21-117">其他 UI 功能，例如工具提示、磚資訊和詳細資料窗格。</span><span class="sxs-lookup"><span data-stu-id="3db21-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="3db21-118">應用程式開發人員可以使用檔案關聯來控制 Shell 處理自訂檔案類型的方式，或將應用程式與現有的檔案類型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="3db21-119">例如，安裝應用程式時，應用程式可以檢查現有的檔案關聯是否存在，並建立或覆寫這些檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="3db21-120">使用者可以控制檔案關聯的某些層面，以自訂 Shell 如何使用 [ **開啟** 檔案] UI 或編輯登錄來處理檔案類型。</span><span class="sxs-lookup"><span data-stu-id="3db21-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="3db21-121">在以下螢幕擷取畫面所示的 [Windows 檔案總管] 視窗中，Shell 會根據與檔案類型相關聯的圖示，為每個檔案顯示不同的圖示。</span><span class="sxs-lookup"><span data-stu-id="3db21-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="3db21-122">如果使用者按兩下檔案 **範例點陣圖影像**，則 Shell 會啟動油漆，並用它來開啟檔案，因為在這個系統上，油漆與 .bmp 檔案相關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="3db21-123">人們可以使用檔案關聯來控制這些動作。</span><span class="sxs-lookup"><span data-stu-id="3db21-123">People can control these actions using file associations.</span></span>

![檔案關聯在實務上的運作方式圖例](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="3db21-125">當您應執行或修改檔案關聯時</span><span class="sxs-lookup"><span data-stu-id="3db21-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="3db21-126">應用程式可基於各種用途使用檔案：某些檔案是由應用程式專用使用，而且通常不會由使用者存取，而其他檔案則由使用者建立，且通常會從 Shell 開啟、搜尋和查看。</span><span class="sxs-lookup"><span data-stu-id="3db21-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="3db21-127">除非您的自訂檔案類型是由應用程式獨佔使用，否則您應該為它執行檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="3db21-128">一般來說，如果您預期使用者會以任何方式直接與這些檔案互動，請針對您的自訂檔案類型來執行檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="3db21-129">這包括使用 Shell 來流覽和開啟檔案、搜尋檔案的內容或屬性，以及預覽檔案。</span><span class="sxs-lookup"><span data-stu-id="3db21-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="3db21-130">如果您的應用程式正在處理現有的檔案類型，除非您想要修改 Shell 處理此類型之所有檔案的方式，否則請勿修改檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="3db21-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="3db21-131">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="3db21-131">How File Associations Work</span></span>

<span data-ttu-id="3db21-132">檔案會在 Shell 中公開為 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="3db21-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="3db21-133">若要控制檔案關聯，應用程式開發人員可以在檔案類型與處理常式之間註冊對應， (COM 物件，這些物件會提供檔案類型之 Shell 專案) 的功能。</span><span class="sxs-lookup"><span data-stu-id="3db21-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="3db21-134">當 Shell 需要查詢檔案類型的檔案關聯時，它會建立包含檔案類型關聯的登錄機碼陣列，並檢查這些機碼是否有適當的檔案關聯可供使用。</span><span class="sxs-lookup"><span data-stu-id="3db21-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3db21-135">其他資源</span><span class="sxs-lookup"><span data-stu-id="3db21-135">Additional Resources</span></span>

-   <span data-ttu-id="3db21-136">如需檔案關聯的概念背景，請參閱 [動詞和檔案關聯的總覽](fa-verbs.md)。</span><span class="sxs-lookup"><span data-stu-id="3db21-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3db21-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="3db21-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db21-138">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="3db21-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="3db21-139">檔案類型</span><span class="sxs-lookup"><span data-stu-id="3db21-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="3db21-140">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="3db21-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="3db21-141">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="3db21-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="3db21-142">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="3db21-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="3db21-143">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="3db21-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="3db21-144">認知類型</span><span class="sxs-lookup"><span data-stu-id="3db21-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="3db21-145">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="3db21-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



