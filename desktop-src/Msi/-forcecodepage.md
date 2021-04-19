---
description: '\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊資料表。 您可以藉由匯出或匯入名為 ForceCodepage. idt 的文字保存檔案，來判斷或設定字碼頁 \_ 。'
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971755"
---
# <a name="_forcecodepage"></a><span data-ttu-id="29676-104">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="29676-104">\_ForceCodepage</span></span>

<span data-ttu-id="29676-105">\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊資料表。</span><span class="sxs-lookup"><span data-stu-id="29676-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="29676-106">您可以藉由匯出或匯入名為 ForceCodepage. idt 的 [文字保存](text-archive-files.md) 盤案，來判斷或設定字碼頁 \_ 。</span><span class="sxs-lookup"><span data-stu-id="29676-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="29676-107">ForceCodepage 資料表的格式 \_ 為2個空白行，後面接著第三行表示數值字碼頁。</span><span class="sxs-lookup"><span data-stu-id="29676-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="29676-108">例如， \_ 日文資料庫的 ForceCodepage idt 檔案看起來會如下所示。</span><span class="sxs-lookup"><span data-stu-id="29676-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="29676-109">此案例中的數值字碼頁為932。</span><span class="sxs-lookup"><span data-stu-id="29676-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="29676-110">如需有關如何使用 \_ ForceCodepage 來取得或設定資料庫字碼頁的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="29676-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="29676-111">程式字碼頁處理 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="29676-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="29676-112">判斷安裝資料庫的字碼頁</span><span class="sxs-lookup"><span data-stu-id="29676-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="29676-113">設定資料庫的字碼頁</span><span class="sxs-lookup"><span data-stu-id="29676-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="29676-114">\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊虛擬資料表。</span><span class="sxs-lookup"><span data-stu-id="29676-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="29676-115">使用 \_ ForceCodepage 資料表無條件地將資料庫設定為字碼頁，而不會執行任何驗證，因為目前在資料庫中的資料是否可以轉譯成新的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="29676-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="29676-116">一律建議您以非語言相關資料庫開頭變更資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="29676-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



