---
description: Windows 7 引進了程式庫，即使這些檔案儲存在不同的位置，也能為使用者提供單一且一致的檔案查看。
title: Windows 媒體櫃
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973840"
---
# <a name="windows-libraries"></a><span data-ttu-id="8c6a3-103">Windows 媒體櫃</span><span class="sxs-lookup"><span data-stu-id="8c6a3-103">Windows Libraries</span></span>

<span data-ttu-id="8c6a3-104">Windows 7 引進了程式庫，即使這些檔案儲存在不同的位置，也能為使用者提供單一且一致的檔案查看。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="8c6a3-105">程式庫可以由使用者進行設定和組織，而程式庫可以包含在使用者電腦上找到的資料夾，以及透過網路共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="8c6a3-106">程式庫會呈現更簡單的基礎儲存系統，因為對使用者而言，程式庫中的檔案和資料夾會顯示在單一視圖中，不論其實際儲存位置為何。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="8c6a3-107">建議在 Windows 7 中撰寫新程式的開發人員使用程式庫做為使用者與程式所使用之檔案進行互動的方法。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="8c6a3-108">在您的程式中使用程式庫，可讓使用者在 Windows 7 中有更簡潔、更簡單且更一致的體驗。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="8c6a3-109">開發人員也應該檢查其現有的程式，並視需要進行更新，以使用程式庫。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="8c6a3-110">因為程式庫不是檔案系統的一部分，所以以檔案系統為基礎的 Api 將無法存取使用者可能已設定的任何程式庫。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="8c6a3-111">目前允許使用者將其內容儲存在不同資料夾或不同電腦上的程式，在新增程式庫支援時，最能發揮最大效益。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="8c6a3-112">程式庫可簡化開發人員和使用者各種儲存位置中的內容管理。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="8c6a3-113">本指南將詳細說明程式庫是什麼、如何進行程式來處理程式庫，以及一些程式可以使用程式庫來改善使用者體驗的方法。</span><span class="sxs-lookup"><span data-stu-id="8c6a3-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c6a3-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c6a3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c6a3-115">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="8c6a3-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="8c6a3-116">在您的程式中使用程式庫</span><span class="sxs-lookup"><span data-stu-id="8c6a3-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="8c6a3-117">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="8c6a3-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="8c6a3-118">Shell 連結</span><span class="sxs-lookup"><span data-stu-id="8c6a3-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="8c6a3-119">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="8c6a3-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="8c6a3-120">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="8c6a3-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
