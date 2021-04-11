---
description: 資料夾深度述詞會指定路徑，以及是否要執行深層或淺層遍歷，來控制搜尋的範圍。
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: 範圍和目錄述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112432"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="da7b9-103">範圍和目錄述詞</span><span class="sxs-lookup"><span data-stu-id="da7b9-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="da7b9-104">資料夾深度述詞會指定路徑，以及是否要執行深層或淺層遍歷，來控制搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="da7b9-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="da7b9-105">以下顯示資料夾深度述詞的語法：</span><span class="sxs-lookup"><span data-stu-id="da7b9-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="da7b9-106">述詞後面接著等號。</span><span class="sxs-lookup"><span data-stu-id="da7b9-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="da7b9-107">路徑 exclosed 以單引號括住，且開頭必須是通訊協定和冒號 (例如，、 `file:` `mapi:` 或 `csc:`) 。</span><span class="sxs-lookup"><span data-stu-id="da7b9-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="da7b9-108">範圍述詞會執行路徑的深度遍歷（包括所有子資料夾），而目錄述詞只會執行指定之資料夾的淺層遍歷。</span><span class="sxs-lookup"><span data-stu-id="da7b9-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="da7b9-109">如同其他結構化查詢語言 (SQL)  (SQL) 限制，您可以在單一查詢中指定一個以上的資料夾深度限制。</span><span class="sxs-lookup"><span data-stu-id="da7b9-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="da7b9-110">若要查詢遠端電腦的本機目錄，請在類別目錄和目錄子句中的遠端電腦上，將電腦名稱稱包含在目錄之前，以及通用命名慣例 (UNC) 路徑。</span><span class="sxs-lookup"><span data-stu-id="da7b9-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="da7b9-111">範例</span><span class="sxs-lookup"><span data-stu-id="da7b9-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="da7b9-112">第一個範圍範例會搜尋 C： \\ Files \\ Reports 資料夾及其所有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="da7b9-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="da7b9-113">目錄範例只會搜尋根資料夾 C： \\ Files \\ 報表。</span><span class="sxs-lookup"><span data-stu-id="da7b9-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="da7b9-114">檔案系統反斜線 (\\) 會成為 URL 樣式的斜線， (有時也稱為正斜線)  (/) 。</span><span class="sxs-lookup"><span data-stu-id="da7b9-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da7b9-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="da7b9-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="da7b9-116">**參考**</span><span class="sxs-lookup"><span data-stu-id="da7b9-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da7b9-117">FROM 子句</span><span class="sxs-lookup"><span data-stu-id="da7b9-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="da7b9-118">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="da7b9-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



