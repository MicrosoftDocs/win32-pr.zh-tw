---
description: 請一律先設定資料庫的字碼頁，再加入任何當地語系化資訊。
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: 設定資料庫的字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691180"
---
# <a name="setting-the-code-page-of-a-database"></a><span data-ttu-id="3f99c-103">設定資料庫的字碼頁</span><span class="sxs-lookup"><span data-stu-id="3f99c-103">Setting the Code Page of a Database</span></span>

<span data-ttu-id="3f99c-104">請一律先設定資料庫的字碼頁，再加入任何當地語系化資訊。</span><span class="sxs-lookup"><span data-stu-id="3f99c-104">Always set the code page of a database prior to adding any localization information.</span></span> <span data-ttu-id="3f99c-105">因為這可能會損毀擴充字元，所以不建議在將資料輸入至資料庫之後嘗試設定字碼頁。</span><span class="sxs-lookup"><span data-stu-id="3f99c-105">Attempting to set the code page after entering data into the database is not recommended because this could corrupt extended characters.</span></span> <span data-ttu-id="3f99c-106">從以字碼頁中立的資料庫開始，可以大幅地促進當地語系化。</span><span class="sxs-lookup"><span data-stu-id="3f99c-106">Localization can be greatly facilitated by starting with a database that is code page neutral.</span></span> <span data-ttu-id="3f99c-107">如需詳細資訊，請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。</span><span class="sxs-lookup"><span data-stu-id="3f99c-107">For details, see [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="3f99c-108">您可以依照 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)所述，判斷資料庫目前的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="3f99c-108">You may determine the current code page of a database as described in [Determining an installation database's code page](determining-an-installation-database-s-code-page.md).</span></span> <span data-ttu-id="3f99c-109">請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) ，以取得數值字碼頁的清單。</span><span class="sxs-lookup"><span data-stu-id="3f99c-109">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of numeric code pages.</span></span>

<span data-ttu-id="3f99c-110">您可以藉由匯入具有非中性字碼頁與 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)的文字保存檔案，來設定空白資料庫的字碼頁，或具有中性字碼頁的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3f99c-110">You may set the code page of a blank database, or a database with a neutral code page, by importing a text archive file having a non-neutral code page with [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="3f99c-111">這會將資料庫的字碼頁設定為匯入檔案的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="3f99c-111">This sets the code page of the database to the imported file's code page.</span></span> <span data-ttu-id="3f99c-112">之後匯入資料庫的所有封存檔案，都必須與第一個檔案具有相同的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="3f99c-112">All archive files subsequently imported into the database must then have the same code page as the first file.</span></span> <span data-ttu-id="3f99c-113">如果是從資料庫匯出文字保存檔案，則封存檔案的字碼頁與父資料庫相同。</span><span class="sxs-lookup"><span data-stu-id="3f99c-113">If a text archive file is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="3f99c-114">請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="3f99c-114">See [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="3f99c-115">任何資料庫的字碼頁都可以設定為指定的數值字碼頁，方法是使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 匯入具有下列格式的文字封存檔案：兩行空白;後面接著包含數值字碼頁的行、索引標籤分隔符號，以及確切的字串： \_ ForceCodepage。</span><span class="sxs-lookup"><span data-stu-id="3f99c-115">The code page of any database may be set to a specified numeric code page by using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) to import a text archive file with the following format: Two blank lines; followed by a line containing the numeric code page, a tab delimiter, and the exact string: \_ForceCodepage.</span></span> <span data-ttu-id="3f99c-116">請注意，在 Windows 2000 中，這會將資料庫中的所有字串轉譯為 ForceCodepage 的字碼頁 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3f99c-116">Note that with Windows 2000, this translates all of the strings in the database to the code page of \_ForceCodepage.</span></span> <span data-ttu-id="3f99c-117">這可能是在當地語系化現有的資料庫，並將所有非中性的字串轉譯成新字碼頁時所設計。</span><span class="sxs-lookup"><span data-stu-id="3f99c-117">This may be intended when localizing an existing database and translating all non-neutral strings to the new code page.</span></span> <span data-ttu-id="3f99c-118">但是，如果資料庫包含不會轉譯的非中性字元串，這會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f99c-118">However, this causes an error if the database contains non-neutral strings that are not to be translated.</span></span>

<span data-ttu-id="3f99c-119">公用程式 WiLangId.vbs 提供如何使用匯 [**入方法**](database-import.md)來設定封裝字碼頁的範例。</span><span class="sxs-lookup"><span data-stu-id="3f99c-119">The utility WiLangId.vbs provides an example of how to set the code page of a package using the [**Import method**](database-import.md).</span></span> <span data-ttu-id="3f99c-120">Windows Installer SDK 中提供了 WiLangId.vbs 的複本。</span><span class="sxs-lookup"><span data-stu-id="3f99c-120">A copy of WiLangId.vbs is provided in the Windows Installer SDK.</span></span> <span data-ttu-id="3f99c-121">您可以使用這個公用程式來判斷資料庫 (封裝) 所支援的語言版本、安裝程式用於使用者介面中未撰寫至資料庫 (產品) 之任何字串的語言版本，或字串集區的單一 ANSI 字碼頁 (程式碼片段) 。</span><span class="sxs-lookup"><span data-stu-id="3f99c-121">You can use this utility to determine the language versions that are supported by the database (Package), the language the installer uses for any strings in the user interface that are not authored into the database (Product), or the single ANSI code page for the string pool (Codepage).</span></span> <span data-ttu-id="3f99c-122">如需使用 WiLangId.vbs 的詳細資訊，請參閱說明頁面： [管理語言和字碼頁](manage-language-and-codepage.md)。</span><span class="sxs-lookup"><span data-stu-id="3f99c-122">For information on using WiLangId.vbs see the help page: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

<span data-ttu-id="3f99c-123">若要判斷 Product、Package 和字碼頁的值，請執行 WiLangId.vbs，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3f99c-123">To determine the values of Product, Package, and Codepage, run WiLangId.vbs as follows.</span></span>

<span data-ttu-id="3f99c-124">**cscript wilangid.vbs** *\[ 資料庫 \] 路徑*</span><span class="sxs-lookup"><span data-stu-id="3f99c-124">**cscript wilangid.vbs** *\[path to database\]*</span></span>

<span data-ttu-id="3f99c-125">若要設定封裝的字碼頁，請執行下列命令列。</span><span class="sxs-lookup"><span data-stu-id="3f99c-125">To set the Codepage of the package run the following command line.</span></span>

<span data-ttu-id="3f99c-126">**cscript wilangid.vbs** *\[ 資料庫 \]* **字碼頁** 的路徑 *\[ 值 \]*</span><span class="sxs-lookup"><span data-stu-id="3f99c-126">**cscript wilangid.vbs** *\[path to database\]* **Codepage** *\[value\]*</span></span>

<span data-ttu-id="3f99c-127">例如，若要將 test.msi 的字碼頁設定為數值 ANSI 字碼頁值1252，請執行下列命令列。</span><span class="sxs-lookup"><span data-stu-id="3f99c-127">For example, to set the Codepage of test.msi to the numeric ANSI code page value 1252, run the following command line.</span></span>

<span data-ttu-id="3f99c-128">**cscript wilangid.vbs c： \\ temp \\test.msi 字碼頁1252**</span><span class="sxs-lookup"><span data-stu-id="3f99c-128">**cscript wilangid.vbs c:\\temp\\test.msi Codepage 1252**</span></span>

 

 



