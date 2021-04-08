---
description: 深入瞭解：可擴充儲存引擎管理的參考
title: 可擴充儲存引擎管理的參考
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026404"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="5e181-103">可擴充儲存引擎管理的參考</span><span class="sxs-lookup"><span data-stu-id="5e181-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="5e181-104">尋找 ManagedESENT 程式庫的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="5e181-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="5e181-105">ManagedESENT 程式庫提供對 ESENT 的 managed 存取，也就是 Windows 原生的可內嵌資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="5e181-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="5e181-106">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5e181-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5e181-107">**本文內容**</span><span class="sxs-lookup"><span data-stu-id="5e181-107">**In this article**</span></span>  
<span data-ttu-id="5e181-108">ManagedESENT 程式庫與 ESENT 有何不同？</span><span class="sxs-lookup"><span data-stu-id="5e181-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="5e181-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e181-109">Requirements</span></span>  
<span data-ttu-id="5e181-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="5e181-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="5e181-111">ManagedESENT 程式庫與 ESENT 有何不同？</span><span class="sxs-lookup"><span data-stu-id="5e181-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="5e181-112">ESENT 是可內嵌的交易式資料庫引擎，可讓您建立需要可靠、高效能、低額外儲存資料的自訂應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e181-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="5e181-113">ESENT 引擎可協助資料需要的範圍，從簡單到太大而無法儲存在記憶體中的雜湊表，到更複雜的資料，例如具有資料表、資料行和索引的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e181-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="5e181-114">若要建立具有 ESENT 的應用程式，您可以使用屬於 Windows 作業系統的 esent.dll DLL，並使用 C/c + + 撰寫程式碼。</span><span class="sxs-lookup"><span data-stu-id="5e181-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="5e181-115">如需 ESENT 的詳細資訊，請參閱 [可擴充儲存引擎參考](./extensible-storage-engine-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5e181-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="5e181-116">ManagedESENT 是以 esent.dll 為基礎，這是 Windows 的一部分，因此沒有額外的非受控二進位檔可供下載和安裝。</span><span class="sxs-lookup"><span data-stu-id="5e181-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="5e181-117">使用 ManagedESENT 程式庫，您可以使用 managed 語言（例如 C）來建立應用程式， \# 而不是使用 c/c + +。</span><span class="sxs-lookup"><span data-stu-id="5e181-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="5e181-118">程式庫會使用相同的類型和成員名稱來公開 ESE API，因此如果您已經熟悉此 API 的結構，就可以輕鬆地轉換至此 managed 程式庫。</span><span class="sxs-lookup"><span data-stu-id="5e181-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e181-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e181-119">Requirements</span></span>

<span data-ttu-id="5e181-120">此 managed 程式庫需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="5e181-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="5e181-121">從 Windows Vista 開始執行 Windows 版本的電腦</span><span class="sxs-lookup"><span data-stu-id="5e181-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="5e181-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="5e181-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="5e181-123">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="5e181-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e181-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="5e181-124">In this section</span></span>

  - [<span data-ttu-id="5e181-125">Microsoft. Esent</span><span class="sxs-lookup"><span data-stu-id="5e181-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="5e181-126">Microsoft. Isam. Interop</span><span class="sxs-lookup"><span data-stu-id="5e181-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="5e181-127">Server2003 （.）</span><span class="sxs-lookup"><span data-stu-id="5e181-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="5e181-128">Microsoft.Isam.Esent.Interop.Vista</span><span class="sxs-lookup"><span data-stu-id="5e181-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="5e181-129">最為理想（.）</span><span class="sxs-lookup"><span data-stu-id="5e181-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="5e181-130">Windows8 （.）</span><span class="sxs-lookup"><span data-stu-id="5e181-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
