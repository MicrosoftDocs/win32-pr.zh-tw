---
title: 管理檔案和資料
description: 使用者可以更輕鬆地存取 Windows 7 中的檔案和資料。
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933393"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="1db7f-103">管理檔案和資料</span><span class="sxs-lookup"><span data-stu-id="1db7f-103">Managing Files and Data</span></span>

<span data-ttu-id="1db7f-104">使用者可以更輕鬆地存取 Windows 7 中的檔案和資料。</span><span class="sxs-lookup"><span data-stu-id="1db7f-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="1db7f-105">新的 Api 讓檔案和視圖更具資訊性，讓應用程式能夠將相關且特殊的資訊提供給 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="1db7f-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="1db7f-106">此外，應用程式也受益于新的連結 *庫* 模型、比資料夾更抽象的使用者儲存空間概念，也可以參與不同應用程式共用的類似檔案類型的通用程式庫。</span><span class="sxs-lookup"><span data-stu-id="1db7f-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="1db7f-107">程式庫</span><span class="sxs-lookup"><span data-stu-id="1db7f-107">Libraries</span></span>

<span data-ttu-id="1db7f-108">Windows 7 引進了連結 *庫* 作為目的地的概念，讓開發人員和終端使用者可以在本機電腦和遠端電腦上的多個位置，將其資料當作專案集合來尋找和組織。</span><span class="sxs-lookup"><span data-stu-id="1db7f-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="1db7f-109">連結 *庫* api 提供簡單的方式，讓開發人員建立應用程式，以在應用程式內建立、互動和支援連結 *庫* 做為第一級專案。</span><span class="sxs-lookup"><span data-stu-id="1db7f-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="1db7f-110">也可以使用 [資料夾選擇器] 對話方塊來選取連結 *庫*。</span><span class="sxs-lookup"><span data-stu-id="1db7f-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="1db7f-111">應用程式可以列舉相關的程式庫範圍，也可以直接使用程式庫做為資料夾。</span><span class="sxs-lookup"><span data-stu-id="1db7f-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="1db7f-112"> (參閱 [windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) 程式庫和 [Windows 7 程式庫：開發人員資源](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)) 。</span><span class="sxs-lookup"><span data-stu-id="1db7f-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![windows 7 圖片庫](images/windows7-10.jpg)

<span data-ttu-id="1db7f-114">*圖片媒體* 櫃會顯示您的圖片，無論其儲存位置為何</span><span class="sxs-lookup"><span data-stu-id="1db7f-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="1db7f-115">檔案格式和資料存放區</span><span class="sxs-lookup"><span data-stu-id="1db7f-115">File Formats and Data Stores</span></span>

<span data-ttu-id="1db7f-116">在 Windows 7 中，Windows 檔案總管可讓使用者以數種方式更輕鬆地進行檔案管理和操作：</span><span class="sxs-lookup"><span data-stu-id="1db7f-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="1db7f-117">您可以使用新的按鈕，讓使用者顯示及隱藏預覽窗格，以存取應用程式檔案類型的預覽。</span><span class="sxs-lookup"><span data-stu-id="1db7f-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="1db7f-118">沉浸式視覺效果堆疊會匯總視圖中檔案類型的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="1db7f-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="1db7f-119">Windows 檔案總管 views 會根據以屬性處理常式撰寫的屬性來顯示有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="1db7f-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="1db7f-120">檔程式碼片段和搜尋結果醒目提示會使用您的 **IFilter** 介面執行，讓搜尋和尋找檔案變得更容易。</span><span class="sxs-lookup"><span data-stu-id="1db7f-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="1db7f-121">內容功能表動詞和命令比以往更容易執行。</span><span class="sxs-lookup"><span data-stu-id="1db7f-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="1db7f-122">藉由為您的通訊協定處理常式所傳回的專案，執行所有適當的格式處理常式，來自自訂資料存放區的搜尋結果可能會與檔案中的搜尋結果一樣豐富。</span><span class="sxs-lookup"><span data-stu-id="1db7f-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="1db7f-123">系統會自動為您的通訊協定處理常式建立連結 *庫*，讓使用者可以輕鬆地範圍搜尋。</span><span class="sxs-lookup"><span data-stu-id="1db7f-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="1db7f-124">您可以透過登錄輕鬆地自訂建立連結 *庫* 的邏輯。</span><span class="sxs-lookup"><span data-stu-id="1db7f-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="1db7f-125"> (請參閱 [開發 Windows Search 的篩選](../search/-search-3x-wds-extidx-filters.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="1db7f-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![windows 7 文件庫](images/windows7-11.jpg)

<span data-ttu-id="1db7f-127">在 Windows 7 中，Windows 檔案總管可讓檔案管理和操作變得更容易</span><span class="sxs-lookup"><span data-stu-id="1db7f-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 