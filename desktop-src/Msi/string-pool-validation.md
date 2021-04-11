---
description: Windows Installer 會將所有資料庫字串儲存在單一的共用字串集區中，以減少資料庫的大小並改善效能。
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114161"
---
# <a name="string-pool-validation"></a><span data-ttu-id="a246d-103">String-Pool 驗證</span><span class="sxs-lookup"><span data-stu-id="a246d-103">String-Pool Validation</span></span>

<span data-ttu-id="a246d-104">Windows Installer 會將所有資料庫字串儲存在單一的共用字串集區中，以減少資料庫的大小並改善效能。</span><span class="sxs-lookup"><span data-stu-id="a246d-104">The Windows Installer stores all database strings in a single shared string pool to reduce the size of the database and to improve performance.</span></span> <span data-ttu-id="a246d-105">驗證字串集區的唯一方法是使用 Windows Installer SDK 中找到的 MsiInfo 工具。</span><span class="sxs-lookup"><span data-stu-id="a246d-105">The only means of validating the string pool is to use the MsiInfo tool found in the Windows Installer SDK.</span></span>

<span data-ttu-id="a246d-106">字串集區驗證由兩個主要檢查組成：</span><span class="sxs-lookup"><span data-stu-id="a246d-106">String pool verification consists of two main checks:</span></span>

-   [<span data-ttu-id="a246d-107">DBCS 字串測試</span><span class="sxs-lookup"><span data-stu-id="a246d-107">DBCS string tests</span></span>](#dbcs-string-tests)
-   [<span data-ttu-id="a246d-108">參考計數驗證</span><span class="sxs-lookup"><span data-stu-id="a246d-108">Reference count verification</span></span>](#reference-count-verification)

## <a name="dbcs-string-tests"></a><span data-ttu-id="a246d-109">DBCS 字串測試</span><span class="sxs-lookup"><span data-stu-id="a246d-109">DBCS String Tests</span></span>

<span data-ttu-id="a246d-110">DBCS 字串測試會掃描資料庫中的每個字串是否有兩個準則：適用于標記為中性字碼頁的封裝，如果有任何字元是擴充字元 (大於 127) ，則會標示字串並顯示訊息，指出資料庫的字碼頁是不正確，因為這些字元需要在所有系統上一致地呈現特定的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="a246d-110">The DBCS string tests scan each string in the database for two criteria: For packages with a neutral code page marked, if any character is an extended character (greater than 127), the string is flagged and a message is displayed saying that the code page of the database is invalid because these characters require a specific code page to be rendered consistently on all systems.</span></span>

<span data-ttu-id="a246d-111">如果資料庫具有字碼頁，就會掃描每個字串中是否有不正確 DBCS 指標。</span><span class="sxs-lookup"><span data-stu-id="a246d-111">If the database has a code page, each string is scanned for an invalid DBCS indicator.</span></span> <span data-ttu-id="a246d-112">如果非中性字元串標示錯誤，字元將無法正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="a246d-112">If a non-neutral string has been improperly marked, the characters will not render correctly.</span></span> <span data-ttu-id="a246d-113"> (這種情況最常見的原因，是使用 \_ 資料庫中已有非中性字元串的 ForceCodepage 資料表，強制字碼頁使用特定的值。 ) 請注意，這項檢查要求系統上必須安裝資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="a246d-113">(This is most commonly caused by forcing the code page to a particular value using the \_ForceCodepage table with non-neutral strings already in the database.) Note that this check requires that the code page of the database be installed on the system.</span></span>

<span data-ttu-id="a246d-114">如果有字碼頁問題，使用者可以使用 \_ ForceCodepage 資料表來強制執行資料庫的字碼頁，使其成為適當的值，以修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="a246d-114">If there is a code page problem, the user may fix the error by using the \_ForceCodepage table to force the code page of the database to the appropriate value.</span></span> <span data-ttu-id="a246d-115">如需詳細資訊，請參閱 [字碼頁處理](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="a246d-115">For more information, see [Code Page Handling](code-page-handling-windows-installer-.md).</span></span>

## <a name="reference-count-verification"></a><span data-ttu-id="a246d-116">參考計數驗證</span><span class="sxs-lookup"><span data-stu-id="a246d-116">Reference Count Verification</span></span>

<span data-ttu-id="a246d-117">為了確認所有字串的參考計數，會掃描每個資料表中的字串值，並保留每個相異字串的計數，並將結果與資料庫字串集區中的預存參考計數進行比較。</span><span class="sxs-lookup"><span data-stu-id="a246d-117">To verify the reference counts of all strings, every table is scanned for string values, a count of each distinct string is kept, and the result is compared to the stored reference count in the database string pool.</span></span>

<span data-ttu-id="a246d-118">如果有字串參考計數問題，使用者應該立即使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)來匯出資料庫的每個資料表、建立新的資料庫，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)將資料表匯入到新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a246d-118">If there is a string reference count problem, the user should immediately export each table of the database using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), create a new database, and import the tables into the new database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="a246d-119">然後，新的資料庫會有與舊資料庫相同的內容，但字串參考計數是正確的。</span><span class="sxs-lookup"><span data-stu-id="a246d-119">The new database then has the same content as the old database, but the string reference counts are correct.</span></span> <span data-ttu-id="a246d-120">從具有損毀字串集區的資料庫中新增或刪除資料可能會導致資料庫損毀和資料遺失，因此，快速採取這些步驟是為了避免資料遺失的問題。</span><span class="sxs-lookup"><span data-stu-id="a246d-120">Adding or deleting data from a database with a corrupt string pool can increase corruption of the database and loss of data, so taking these steps quickly is important to prevent further data loss.</span></span>

<span data-ttu-id="a246d-121">重建資料庫時，請記得在新的資料庫中內嵌任何必要的儲存體和資料流程 (查看[ \_ 串流資料表](-streams-table.md)和[ \_ 儲存體資料表](-storages-table.md)) 並留意程式字碼頁面問題。</span><span class="sxs-lookup"><span data-stu-id="a246d-121">When rebuilding databases, remember to embed any necessary storages and streams in the new database (see [\_Streams Table](-streams-table.md) and [\_Storages Table](-storages-table.md)) and be aware of code page issues.</span></span> <span data-ttu-id="a246d-122">也請記得設定每個必要的 [摘要資訊資料流程](summary-information-stream.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a246d-122">Also remember to set each of the necessary [Summary Information Stream](summary-information-stream.md) properties.</span></span>

 

 



