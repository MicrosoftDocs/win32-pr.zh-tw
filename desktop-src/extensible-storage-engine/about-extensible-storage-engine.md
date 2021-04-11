---
description: 深入瞭解：關於可擴充儲存引擎
title: 關於可擴充儲存引擎
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936574"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="60000-103">關於可擴充儲存引擎</span><span class="sxs-lookup"><span data-stu-id="60000-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="60000-104">_**適用于：** Exchange Server 2013 |Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60000-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="60000-105">關於可擴充儲存引擎</span><span class="sxs-lookup"><span data-stu-id="60000-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="60000-106">可延伸儲存引擎 (ESE) 是一種資料庫引擎，可將資訊儲存在邏輯順序中。</span><span class="sxs-lookup"><span data-stu-id="60000-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="60000-107">您可以依序或藉由存取定義的索引來抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="60000-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="60000-108">資料庫的更新會透過交易來執行，以確保安全的作業。</span><span class="sxs-lookup"><span data-stu-id="60000-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="60000-109">ESE 可同時存取多個資料庫，包括可用於系統復原的交易記錄檔資料庫。</span><span class="sxs-lookup"><span data-stu-id="60000-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="60000-110">ESE 可以擴充至大型或小型應用程式。</span><span class="sxs-lookup"><span data-stu-id="60000-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="60000-111">下列功能適用于 ESE 應用程式設計介面 (API) ：</span><span class="sxs-lookup"><span data-stu-id="60000-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="60000-112">備份與還原：應用程式可以在線上和主動修改資料狀態時，建立一致的資料狀態複本。</span><span class="sxs-lookup"><span data-stu-id="60000-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="60000-113">資料指標流覽：應用程式可以流覽資料指標，以順序或使用索引來存取資料。</span><span class="sxs-lookup"><span data-stu-id="60000-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="60000-114">資料庫：以單一單位備份和還原的資料表集合。</span><span class="sxs-lookup"><span data-stu-id="60000-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="60000-115">記錄和損毀復原： ESE API 可確保即使在系統損毀時，仍會接受應用程式定義的資料一致性。</span><span class="sxs-lookup"><span data-stu-id="60000-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="60000-116">資料表：用來儲存資料的 ESE 資料庫的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="60000-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="60000-117">交易： ESE 資料庫引擎提供不可部分完成的一致性隔離持久 (ACID) 交易，讓應用程式只從可靠的資料狀態取出資料，並在發生非預期的進程終止或系統關機時維持資料一致性。</span><span class="sxs-lookup"><span data-stu-id="60000-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="60000-118">可擴充：應用程式可以建立大小為 100 GB 或小至1MB 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="60000-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

