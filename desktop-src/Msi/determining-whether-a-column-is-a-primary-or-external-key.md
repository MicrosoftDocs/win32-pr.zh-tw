---
description: 您可以參考資料表的 [參考] 頁面，判斷特定資料行是資料表的主鍵或外部索引鍵。
ms.assetid: 47ed59f7-914a-40a6-b982-59779a003a1c
title: 判斷資料行是否為主要或外部索引鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877f8a90ca7cb6121005e7eb694ab057722d11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978021"
---
# <a name="determining-whether-a-column-is-a-primary-or-external-key"></a><span data-ttu-id="0ab18-103">判斷資料行是否為主要或外部索引鍵</span><span class="sxs-lookup"><span data-stu-id="0ab18-103">Determining Whether a Column is a Primary or External Key</span></span>

<span data-ttu-id="0ab18-104">您可以參考資料表的 [參考] 頁面，判斷特定資料行是資料表的主鍵或外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0ab18-104">You can determine whether a specific column is a primary key or external key of the table by consulting the reference page of the table.</span></span> <span data-ttu-id="0ab18-105">所有安裝資料庫資料表之參考頁面的連結清單，都位於 [ [資料庫資料表]](database-tables.md)下。</span><span class="sxs-lookup"><span data-stu-id="0ab18-105">A list of links to the reference pages of all the installation database tables is located under [Database Tables](database-tables.md).</span></span> <span data-ttu-id="0ab18-106">每個參考頁面都會識別屬於主鍵或外部索引鍵的資料行。</span><span class="sxs-lookup"><span data-stu-id="0ab18-106">Each of the reference pages identifies columns that are a primary key or an external key.</span></span>

<span data-ttu-id="0ab18-107">外部索引鍵的資料庫資料行採用主鍵資料行的名稱，加上底線字元。</span><span class="sxs-lookup"><span data-stu-id="0ab18-107">Database columns that are external keys take the name of the primary key column with an added underscore character.</span></span> <span data-ttu-id="0ab18-108">例如，檔案資料表之 File 資料行的外部索引鍵一律為 File \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ab18-108">For example, an external key to the File column of the File table is always named File\_.</span></span>

<span data-ttu-id="0ab18-109">若要查看說明資料表關聯性的實體關聯性圖表，請參閱 [核心資料表群組](core-tables-group.md)、檔案 [資料表群組](file-tables-group.md)、登錄 [資料表群組](registry-tables-group.md)、 [系統資料表群組](system-tables-group.md)或 [消費者介面架構](user-interface-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="0ab18-109">To view entity relationship diagrams that illustrate table relationships, see [Core Tables Group](core-tables-group.md), [File Tables Group](file-tables-group.md), [Registry Tables Group](registry-tables-group.md), [System Tables Group](system-tables-group.md), or [User Interface Schema](user-interface-schema.md).</span></span>

 

 



