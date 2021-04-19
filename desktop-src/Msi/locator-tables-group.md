---
description: 定位器資料表群組是用來尋找檔案和應用程式。
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: 定位器資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975763"
---
# <a name="locator-tables-group"></a><span data-ttu-id="430d2-103">定位器資料表群組</span><span class="sxs-lookup"><span data-stu-id="430d2-103">Locator Tables Group</span></span>

<span data-ttu-id="430d2-104">定位器資料表群組是用來尋找檔案和應用程式。</span><span class="sxs-lookup"><span data-stu-id="430d2-104">The Locator Tables group is used to locate files and applications.</span></span> <span data-ttu-id="430d2-105">若要搜尋檔案，請先判斷檔案簽章，然後找出檔案。</span><span class="sxs-lookup"><span data-stu-id="430d2-105">To search for a file, first determine the file signature and then locate the file.</span></span> <span data-ttu-id="430d2-106">定位器資料表是用來搜尋登錄、安裝程式設定資料、樹狀目錄或 .ini 檔案，以取得檔案的唯一簽章。</span><span class="sxs-lookup"><span data-stu-id="430d2-106">The Locator tables are used to search the registry, installer configuration data, directory tree, or .ini files for the unique signature of a file.</span></span> <span data-ttu-id="430d2-107">然後，您可以在簽章 [資料表](signature-table.md) 中檢查檔案簽章，以確定特定檔案確實是正在搜尋的檔案，而不是另一個具有相同名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="430d2-107">The file signature can then be checked in the [Signature table](signature-table.md) to ascertain that a particular file is really the file being sought and not another file with the same name.</span></span> <span data-ttu-id="430d2-108">如果定位器資料表中的記錄未在簽章資料表中包含索引鍵，則記錄會參考目錄而不是檔案。</span><span class="sxs-lookup"><span data-stu-id="430d2-108">If a record in a locator table does not contain a key into the Signature table, then the record refers to a directory and not a file.</span></span>

<span data-ttu-id="430d2-109">您可以透過[元件資料表](component-table.md)的外部索引鍵，在檔案[資料表](file-table.md)中找到控制檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="430d2-109">The component controlling a file is found in the [File table](file-table.md) through the external key to the [Component table](component-table.md).</span></span> <span data-ttu-id="430d2-110">因為每個檔案都屬於一個元件，所以安裝程式會透過元件表格解析檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="430d2-110">The installer resolves the location of a file through the Component table because every file belongs to one component.</span></span> <span data-ttu-id="430d2-111">元件資料表中的外部索引鍵可透過 [目錄資料表](directory-table.md)找到元件的位置。</span><span class="sxs-lookup"><span data-stu-id="430d2-111">The location of a component is found through an external key in the Component table to the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="430d2-112">藉由搜尋組成應用程式的檔案，即可找到應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="430d2-112">The location of an application is found by searching for files that make up the application.</span></span> <span data-ttu-id="430d2-113">安裝程式也提供兩個數據表來搜尋舊版的應用程式： [AppSearch 資料表](appsearch-table.md) 和 [CCPSearch 資料表](ccpsearch-table.md)。</span><span class="sxs-lookup"><span data-stu-id="430d2-113">The installer also provides two tables for searching for previous versions of an application: the [AppSearch table](appsearch-table.md) and the [CCPSearch table](ccpsearch-table.md).</span></span>

<span data-ttu-id="430d2-114">下表構成定位器資料表群組，用來判斷檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="430d2-114">The following tables make up the Locator tables group and are used to determine the file signature.</span></span>

-   <span data-ttu-id="430d2-115">[RegLocator 資料表](reglocator-table.md)包含搜尋登錄中的檔案或目錄所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="430d2-115">The [RegLocator table](reglocator-table.md) holds the information needed to search for a file or directory in the registry.</span></span>
-   <span data-ttu-id="430d2-116">[IniLocator 資料表](inilocator-table.md)會保存搜尋 .ini 檔案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="430d2-116">The [IniLocator table](inilocator-table.md) holds the information needed to search for a .ini file.</span></span> <span data-ttu-id="430d2-117">.Ini 檔案必須存在於預設的 Microsoft Windows 目錄中。</span><span class="sxs-lookup"><span data-stu-id="430d2-117">The .ini file must be present in the default Microsoft Windows directory.</span></span>
-   <span data-ttu-id="430d2-118">[CompLocator 資料表](complocator-table.md)包含使用安裝程式的設定資料搜尋檔案或目錄所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="430d2-118">The [CompLocator table](complocator-table.md) holds the information needed to search for a file or a directory using the installer's configuration data.</span></span>
-   <span data-ttu-id="430d2-119">[DrLocator 資料表](drlocator-table.md)包含搜尋目錄樹狀目錄中的檔案或目錄所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="430d2-119">The [DrLocator table](drlocator-table.md) holds the information needed to search for a file or directory in the directory tree.</span></span>
-   <span data-ttu-id="430d2-120">[AppSearch 資料表](appsearch-table.md)包含必須設定為對應檔案簽章之搜尋結果的屬性。</span><span class="sxs-lookup"><span data-stu-id="430d2-120">The [AppSearch table](appsearch-table.md) contains the properties that must be set to the search result of a corresponding file signature.</span></span>
-   <span data-ttu-id="430d2-121">[CCPSearch 資料表](ccpsearch-table.md)包含檔案簽章的清單，其中至少有一個必須存在於使用者電腦上，才能進行合規性檢查程式 (CCP) 。</span><span class="sxs-lookup"><span data-stu-id="430d2-121">The [CCPSearch table](ccpsearch-table.md) contains the list of file signatures, at least one of which needs to be present on a user's computer for the Compliance Checking Program (CCP).</span></span>

 

 



