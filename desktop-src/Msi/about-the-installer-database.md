---
description: Windows Installer 資料庫是由許多相關的資料表組成，其中包含安裝一組應用程式所需資訊的關係資料庫。
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: 關於安裝程式資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848999"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="28282-103">關於安裝程式資料庫</span><span class="sxs-lookup"><span data-stu-id="28282-103">About the Installer Database</span></span>

<span data-ttu-id="28282-104">Windows Installer 資料庫是由許多相關的資料表組成，其中包含安裝一組應用程式所需資訊的關係資料庫。</span><span class="sxs-lookup"><span data-stu-id="28282-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="28282-105">因為資料庫是關聯式的，所以資料表會透過主鍵和外鍵值中的資料進行連結。</span><span class="sxs-lookup"><span data-stu-id="28282-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="28282-106">這提供了一種有效的方法來變更安裝程式，並表示使用者可以更輕鬆地自訂大型應用程式或應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="28282-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="28282-107">資料庫資料表會反映整個應用程式群組的一般版面配置，包括：</span><span class="sxs-lookup"><span data-stu-id="28282-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="28282-108">可用的功能</span><span class="sxs-lookup"><span data-stu-id="28282-108">Available features</span></span>
-   <span data-ttu-id="28282-109">單元</span><span class="sxs-lookup"><span data-stu-id="28282-109">Components</span></span>
-   <span data-ttu-id="28282-110">功能與元件之間的關聯性</span><span class="sxs-lookup"><span data-stu-id="28282-110">Relationship between features and components</span></span>
-   <span data-ttu-id="28282-111">必要的登錄設定</span><span class="sxs-lookup"><span data-stu-id="28282-111">Necessary registry settings</span></span>
-   <span data-ttu-id="28282-112">應用程式的使用者介面</span><span class="sxs-lookup"><span data-stu-id="28282-112">User interface for the application</span></span>

<span data-ttu-id="28282-113">若要建立安裝資料庫，您必須在資料表中填入應用程式和安裝程式的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="28282-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="28282-114">即使是中等大小的安裝，手動編寫所有這些資料表都會變成大型工作;因此，有一些協力廠商工具可協助您建立安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="28282-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="28282-115">下列各節說明相關資料庫資料表的群組。</span><span class="sxs-lookup"><span data-stu-id="28282-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="28282-116">核心資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="28282-117">檔案資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="28282-118">登錄資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="28282-119">系統資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="28282-120">定位器資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="28282-121">程式資訊資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="28282-122">安裝程式資料表群組</span><span class="sxs-lookup"><span data-stu-id="28282-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="28282-123">實體關聯性圖表圖例</span><span class="sxs-lookup"><span data-stu-id="28282-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="28282-124">壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="28282-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="28282-125">如需安裝資料庫中所有資料表的完整清單，請參閱 [資料庫資料表](database-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="28282-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28282-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="28282-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28282-127">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="28282-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



