---
description: 您可以使用資料庫資料表編輯器（例如 Windows Installer SDK 提供的 Orca）或從應用程式呼叫資料庫函式，將當地語系化資訊新增至安裝資料庫。
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: 參數字串的字碼頁處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191607"
---
# <a name="code-page-handling-of-parameter-strings"></a><span data-ttu-id="05b61-103">參數字串的字碼頁處理</span><span class="sxs-lookup"><span data-stu-id="05b61-103">Code Page Handling of Parameter Strings</span></span>

<span data-ttu-id="05b61-104">您可以使用資料庫資料表編輯器（例如 Windows Installer SDK 提供的 Orca）或從應用程式呼叫 [資料庫](database-functions.md) 函式，將當地語系化資訊新增至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="05b61-104">You can add localization information to an installation database by using a database table editor such as Orca that is provided with the Windows Installer SDK, or by calling the [Database Functions](database-functions.md) from an application.</span></span> <span data-ttu-id="05b61-105">請小心只傳遞使用正在當地語系化的資料庫字碼頁的字串參數。</span><span class="sxs-lookup"><span data-stu-id="05b61-105">Be careful to only pass string parameters that use the code page of the database that is being localized.</span></span> <span data-ttu-id="05b61-106">如果字串參數包含的字元無法由資料庫的字碼頁表示，則在呼叫 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)時，安裝程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="05b61-106">If a string parameter contains characters that cannot be represented by the code page of the database, the Installer returns an error when calling [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="05b61-107">如需數值字碼頁的清單，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="05b61-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

<span data-ttu-id="05b61-108">如需詳細資訊，請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。</span><span class="sxs-lookup"><span data-stu-id="05b61-108">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>

## <a name="adding-localization-information-to-a-database"></a><span data-ttu-id="05b61-109">將當地語系化資訊新增至資料庫</span><span class="sxs-lookup"><span data-stu-id="05b61-109">Adding Localization Information to a Database</span></span>

<span data-ttu-id="05b61-110">當您將當地語系化資訊加入至資料庫時，作業系統必須支援資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="05b61-110">When you add localization information to a database, the code page of the database must be supported by the operating system.</span></span> <span data-ttu-id="05b61-111">它不一定要是系統目前的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="05b61-111">It does not have to be the current code page of the system.</span></span> <span data-ttu-id="05b61-112">[**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) 必須針對資料庫字碼頁傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="05b61-112">[**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) must return **TRUE** for the database code page.</span></span> <span data-ttu-id="05b61-113">由於系統會將 ANSI 字串轉換為 Unicode，因此如果目前使用者字碼頁與資料庫字碼頁不同，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="05b61-113">Because the system converts ANSI strings to Unicode, there is an error if the current user code page is not the same as the database code page.</span></span>

<span data-ttu-id="05b61-114">呼叫 ANSI 版本的 Windows Installer API 會使用目前的系統字碼頁，將當地語系化的字串轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="05b61-114">Calling the ANSI version of the Windows Installer API converts the localized string to Unicode by using the current system code page.</span></span> <span data-ttu-id="05b61-115">認可資料庫時，會使用資料庫的字碼頁，將 Unicode 字串轉換為 ANSI。</span><span class="sxs-lookup"><span data-stu-id="05b61-115">When the database is committed, the Unicode string is converted to ANSI using the code page of the database.</span></span> <span data-ttu-id="05b61-116">如果目前的系統字碼頁與當地語系化字串的字碼頁不同，則結果可能會遺失資料和不正確的字串轉換。</span><span class="sxs-lookup"><span data-stu-id="05b61-116">If the current system code page differs from the code page of the localized string, the result can be a loss of data and incorrect string conversion.</span></span>

<span data-ttu-id="05b61-117">下列程式說明如何儲存當地語系化資料。</span><span class="sxs-lookup"><span data-stu-id="05b61-117">The following procedure shows you how to store the localization data.</span></span>

<span data-ttu-id="05b61-118">**若要儲存當地語系化資料**</span><span class="sxs-lookup"><span data-stu-id="05b61-118">**To store localization data**</span></span>

1.  <span data-ttu-id="05b61-119">將資料庫的字碼頁設定為當地語系化字串的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="05b61-119">Set the code page of the database to the code page of the localized string.</span></span>
2.  <span data-ttu-id="05b61-120">使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函式將 ANSI 字串轉換為 Unicode，並指定當地語系化資料的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="05b61-120">Convert the ANSI string to Unicode by using the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function, and specify the code page of the localized data.</span></span>
3.  <span data-ttu-id="05b61-121">使用 Unicode 字串來新增當地語系化資料，以呼叫 Windows Installer API 的 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="05b61-121">Call the Unicode version of the Windows Installer API by using the Unicode string to add the localized data.</span></span>
4.  <span data-ttu-id="05b61-122">使用 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)認可資料庫的當地語系化變更。</span><span class="sxs-lookup"><span data-stu-id="05b61-122">Commit the localization changes to the database by using [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="05b61-123">您也可以匯入和匯出 ASCII 文字保存檔案，以將當地語系化資訊新增至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="05b61-123">You can also add localization information to an installation database by importing and exporting ASCII text archive files.</span></span> <span data-ttu-id="05b61-124">如需詳細資訊，請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="05b61-124">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

 

 
