---
description: 安裝資料庫的開發人員必須留意 Win32 OLE 結構化儲存體實作為資料流程處理的兩項限制。
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: 資料流程的 OLE 限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191696"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="48d64-103">資料流程的 OLE 限制</span><span class="sxs-lookup"><span data-stu-id="48d64-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="48d64-104">安裝資料庫的開發人員必須留意 Win32 OLE 結構化儲存體實作為資料流程處理的兩項限制。</span><span class="sxs-lookup"><span data-stu-id="48d64-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="48d64-105">這些限制可能會透過轉換和其他可能儲存在資料庫中做為資料流程的資料，間接影響安裝程式函數。</span><span class="sxs-lookup"><span data-stu-id="48d64-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="48d64-106">有兩個相關的限制：</span><span class="sxs-lookup"><span data-stu-id="48d64-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="48d64-107">使用句號分隔符號來串連資料表名稱和記錄主鍵的值，以建立的索引名稱會儲存二進位資料。</span><span class="sxs-lookup"><span data-stu-id="48d64-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="48d64-108">OLE 會將資料流程名稱限制為32個字元 (31 + null 結束字元) 。</span><span class="sxs-lookup"><span data-stu-id="48d64-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="48d64-109">Windows Installer 使用可根據字元將限制擴展為62個字元的壓縮演算法。</span><span class="sxs-lookup"><span data-stu-id="48d64-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="48d64-110">請注意，雙位元組字元計數為2。</span><span class="sxs-lookup"><span data-stu-id="48d64-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="48d64-111">雖然您可以一次開啟多個資料流程，但您無法在第一次參考關閉之前再次開啟資料流程。</span><span class="sxs-lookup"><span data-stu-id="48d64-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="48d64-112">這表示您無法選取要同時在多個記錄中開啟的相同二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="48d64-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="48d64-113">嘗試從第二筆記錄讀取二進位資料失敗。</span><span class="sxs-lookup"><span data-stu-id="48d64-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="48d64-114">此外，當該記錄中的二進位資料流程已開啟時，您也無法重新命名記錄的主鍵。</span><span class="sxs-lookup"><span data-stu-id="48d64-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



