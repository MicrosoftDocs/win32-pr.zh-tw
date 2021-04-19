---
description: 深入瞭解：使用可擴充儲存引擎
title: 使用可擴充儲存引擎
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969272"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="15570-103">使用可擴充儲存引擎</span><span class="sxs-lookup"><span data-stu-id="15570-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="15570-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="15570-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="15570-105">使用可擴充儲存引擎</span><span class="sxs-lookup"><span data-stu-id="15570-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="15570-106">本章節包含如何使用下列 ESE API 元件的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="15570-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="15570-107">資料行</span><span class="sxs-lookup"><span data-stu-id="15570-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="15570-108">資料表中的索引編制</span><span class="sxs-lookup"><span data-stu-id="15570-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="15570-109">建立資料庫</span><span class="sxs-lookup"><span data-stu-id="15570-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="15570-110">交易</span><span class="sxs-lookup"><span data-stu-id="15570-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="15570-111">ESE 錯誤</span><span class="sxs-lookup"><span data-stu-id="15570-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="15570-112">ESE 檔案</span><span class="sxs-lookup"><span data-stu-id="15570-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="15570-113">您的程式來源檔案應包含 esent 標頭檔，以存取可延伸儲存引擎 API 的函式原型和結構定義。</span><span class="sxs-lookup"><span data-stu-id="15570-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="15570-114">開發人員可使用 esent 程式庫檔案來建立使用可延伸儲存引擎 API 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="15570-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="15570-115">應用程式會在執行時間連結至 esent.dll。</span><span class="sxs-lookup"><span data-stu-id="15570-115">At runtime, applications link to the esent.dll.</span></span>
