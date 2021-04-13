---
description: 使用資料庫之前，您必須先取得其控制碼。
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: 取得資料庫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114324"
---
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="170b6-103">取得資料庫控制碼</span><span class="sxs-lookup"><span data-stu-id="170b6-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="170b6-104">使用資料庫之前，您必須先取得其控制碼。</span><span class="sxs-lookup"><span data-stu-id="170b6-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="170b6-105">**存取安裝程式資料庫的相關資訊**</span><span class="sxs-lookup"><span data-stu-id="170b6-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="170b6-106">以下列兩種方式之一取得資料庫的控制碼：</span><span class="sxs-lookup"><span data-stu-id="170b6-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="170b6-107">如果安裝正在進行中，請呼叫 [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) 函數來取得使用中資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="170b6-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="170b6-108">如果安裝不在進行中，請呼叫 [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) 函數來開啟任何指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="170b6-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="170b6-109">開啟資料庫之後，您可以呼叫函式來取得資料庫的相關資訊，或運算元據庫。</span><span class="sxs-lookup"><span data-stu-id="170b6-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="170b6-110">藉由呼叫 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)函數，建立 **View** 物件並指定開放式資料庫的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="170b6-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="170b6-111">藉由呼叫 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) 函數，取得包含開啟資料庫中之指定資料表之所有主鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="170b6-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="170b6-112">藉由呼叫 [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) 函數，檢查開啟資料庫的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="170b6-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="170b6-113">您可以使用 **MsiGetDatabaseState** 函式來判斷資料庫的讀取/寫入狀態，或是控制碼是否有效。</span><span class="sxs-lookup"><span data-stu-id="170b6-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



