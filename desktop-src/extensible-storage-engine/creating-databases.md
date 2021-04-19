---
description: 深入瞭解：建立資料庫
title: 建立資料庫
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973894"
---
# <a name="creating-databases"></a><span data-ttu-id="d75c6-103">建立資料庫</span><span class="sxs-lookup"><span data-stu-id="d75c6-103">Creating Databases</span></span>


<span data-ttu-id="d75c6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d75c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="creating-databases"></a><span data-ttu-id="d75c6-105">建立資料庫</span><span class="sxs-lookup"><span data-stu-id="d75c6-105">Creating Databases</span></span>

<span data-ttu-id="d75c6-106">ESE 資料庫包含一個或多個資料表，這些資料表會依資料行和資料列來組織資料。</span><span class="sxs-lookup"><span data-stu-id="d75c6-106">The ESE database comprises one or more tables that organize data by columns and rows.</span></span> <span data-ttu-id="d75c6-107">ESE 資料庫是以名稱和資料庫識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="d75c6-107">The ESE database is identified by name and database ID.</span></span> <span data-ttu-id="d75c6-108">ESE 資料庫看起來像是 Microsoft Windows 作業系統的單一檔案;不過，在內部，資料庫會儲存為頁面的集合。</span><span class="sxs-lookup"><span data-stu-id="d75c6-108">An ESE database looks like a single file to the Microsoft Windows operating system; however, internally the database is stored as a collection of pages.</span></span> <span data-ttu-id="d75c6-109">這些頁面包含的中繼資料會描述資料庫中的資料、資料本身，以及儲存不同資料順序的一或多個索引。</span><span class="sxs-lookup"><span data-stu-id="d75c6-109">These pages contain metadata that describe the data in the database, the data itself, and one or more indices that store different orders of the data.</span></span> <span data-ttu-id="d75c6-110">資料庫最多可以包含 2 ^ 31 個頁面，或包含 8 KB 頁面之資料庫的 16 Tb 資料。</span><span class="sxs-lookup"><span data-stu-id="d75c6-110">The database may contain up to 2^31 pages, or 16 Terabytes of data for a database with 8 KB pages.</span></span>

<span data-ttu-id="d75c6-111">應用程式會建立資料庫引擎的實例，然後建立資料庫並將它附加至實例。</span><span class="sxs-lookup"><span data-stu-id="d75c6-111">The application creates an instance of the database engine, then creates a database and attaches it to the instance.</span></span> <span data-ttu-id="d75c6-112">最多可同時將6個資料庫附加至具有 [JetCreateDatabase](./jetcreatedatabase-function.md) 或 [JetAttachDatabase](./jetattachdatabase-function.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="d75c6-112">Up to 6 databases can be simultaneously attached to an instance with [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="d75c6-113">一個或多個會話應該在資料庫中啟動，因為所有後續的 ESE 作業都是在會話的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="d75c6-113">One or more sessions should be started within the database, because all subsequent ESE operations are performed in the context of a session.</span></span> <span data-ttu-id="d75c6-114">您應該針對每個使用 ESE 的執行緒開啟個別的會話。</span><span class="sxs-lookup"><span data-stu-id="d75c6-114">A separate session should be opened for each thread using ESE.</span></span>

<span data-ttu-id="d75c6-115">此程式會初始化 ESE 並建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="d75c6-115">This procedure will initialize ESE and create a database.</span></span>

### <a name="to-initialize-ese-and-create-a-database"></a><span data-ttu-id="d75c6-116">初始化 ESE 並建立資料庫</span><span class="sxs-lookup"><span data-stu-id="d75c6-116">To initialize ESE and create a database</span></span>

1.  <span data-ttu-id="d75c6-117">[JetCreateInstance](./jetcreateinstance-function.md)：建立 database engine 的實例。</span><span class="sxs-lookup"><span data-stu-id="d75c6-117">[JetCreateInstance](./jetcreateinstance-function.md): Creates an instance of the database engine.</span></span>
    
    <span data-ttu-id="d75c6-118">**WINDOWS XP 和更新版本：** 這項功能可在 Windows XP 及更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="d75c6-118">**Windows XP and later:** This function is available in Windows XP and later.</span></span> <span data-ttu-id="d75c6-119">在 Windows 2000 上，只支援一個實例，而該實例會以隱含方式建立</span><span class="sxs-lookup"><span data-stu-id="d75c6-119">On Windows 2000, only one instance is supported and that instance is created implicitly</span></span>

2.  <span data-ttu-id="d75c6-120">[JetSetSystemParameter](./jetsetsystemparameter-function.md)：在使用 [JetInit](./jetinit-function.md)初始化實例之前，必須先設定影響實體配置的系統參數，例如 JET_paramLogFilePath 和 JET_paramSystemPath。</span><span class="sxs-lookup"><span data-stu-id="d75c6-120">[JetSetSystemParameter](./jetsetsystemparameter-function.md): System parameters that the affect the physical layout such as the JET_paramLogFilePath and JET_paramSystemPath must be set before initializing the instance with [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="d75c6-121">在這個階段設定的參數會針對實例中建立的所有資料庫進行設定。</span><span class="sxs-lookup"><span data-stu-id="d75c6-121">The parameters set at this stage are set for all databases created in the instance.</span></span> <span data-ttu-id="d75c6-122">[JetSetSystemParameter](./jetsetsystemparameter-function.md) 是唯一可以使用實例的函式，它會使用 [JetInit](./jetinit-function.md)來初始化。</span><span class="sxs-lookup"><span data-stu-id="d75c6-122">[JetSetSystemParameter](./jetsetsystemparameter-function.md) is the only function that can use the instance before it is initialized with [JetInit](./jetinit-function.md).</span></span>

3.  <span data-ttu-id="d75c6-123">[JetInit](./jetinit-function.md)：初始化實例。</span><span class="sxs-lookup"><span data-stu-id="d75c6-123">[JetInit](./jetinit-function.md): Initializes the instance.</span></span> <span data-ttu-id="d75c6-124">實例必須使用 [JetInit](./jetinit-function.md) 初始化，才能搭配任何其他函式使用。</span><span class="sxs-lookup"><span data-stu-id="d75c6-124">Instance must be initialized with [JetInit](./jetinit-function.md) before it can be used with any other functions.</span></span>

4.  <span data-ttu-id="d75c6-125">[JetBeginSession](./jetbeginsession-function.md)：建立所有後續交易的會話。</span><span class="sxs-lookup"><span data-stu-id="d75c6-125">[JetBeginSession](./jetbeginsession-function.md): Creates the session for all subsequent transactions.</span></span> <span data-ttu-id="d75c6-126">所有資料庫交易都會發生在會話的內容中 ([JET_SESID](./jet-sesid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d75c6-126">All database transactions take place in the context of the session ([JET_SESID](./jet-sesid.md)).</span></span>

5.  <span data-ttu-id="d75c6-127">[JetCreateDatabase](./jetcreatedatabase-function.md)：建立資料庫，並將控制碼傳回 ([JET_DBID](./jet-dbid.md)) 的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d75c6-127">[JetCreateDatabase](./jetcreatedatabase-function.md): Creates the database and returns a handle to the database ID ([JET_DBID](./jet-dbid.md)).</span></span>
    
    <span data-ttu-id="d75c6-128">如果資料庫已經存在，則會以下列兩個步驟取代上述的步驟5：</span><span class="sxs-lookup"><span data-stu-id="d75c6-128">If the database already exists, step 5 above is replaced by the following two steps:</span></span>
    
    1.  <span data-ttu-id="d75c6-129">[JetAttachDatabase](./jetattachdatabase-function.md)：依名稱將資料庫附加至會話</span><span class="sxs-lookup"><span data-stu-id="d75c6-129">[JetAttachDatabase](./jetattachdatabase-function.md): Attaches the database by name to the session</span></span>
    
    2.  <span data-ttu-id="d75c6-130">[JetOpenDatabase](./jetopendatabase-function.md)：傳回後續資料庫作業中所使用的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d75c6-130">[JetOpenDatabase](./jetopendatabase-function.md): Returns the database ID that is used in subsequent database operations.</span></span>

<span data-ttu-id="d75c6-131">您可以使用 [JetDetachDatabase](./jetdetachdatabase-function.md) ，並在稍後附加至具有 [JetAttachDatabase](./jetattachdatabase-function.md)的另一個實例，將資料庫從一個 ESE 實例卸離。</span><span class="sxs-lookup"><span data-stu-id="d75c6-131">A database can be detached from one ESE instance using [JetDetachDatabase](./jetdetachdatabase-function.md) and later attached to another instance with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="d75c6-132">卸離資料庫後，就可以使用標準的 Windows 公用程式，將它複製成單一檔案。</span><span class="sxs-lookup"><span data-stu-id="d75c6-132">When the database is detached, it can be copied as a single file using standard Windows utilities.</span></span> <span data-ttu-id="d75c6-133">不過，當資料庫附加至 ESE 實例時，無法複製它，因為 ESE 會以獨佔方式開啟資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="d75c6-133">However, when the database is attached to an ESE instance it cannot be copied since ESE opens database files exclusively.</span></span> <span data-ttu-id="d75c6-134">此外，如果實例損毀，則無法單獨複製資料庫檔案，因為它需要與其相關聯的交易記錄檔，才能從該損毀中復原。</span><span class="sxs-lookup"><span data-stu-id="d75c6-134">Also, if the instance crashes then the database file cannot be copied alone because it needs the transaction log files associated with it to recover from that crash.</span></span>
