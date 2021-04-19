---
description: 用來建立分散式應用程式的其他 Microsoft 工具
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: 用來建立分散式應用程式的其他 Microsoft 工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972786"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="13f23-103">用來建立分散式應用程式的其他 Microsoft 工具</span><span class="sxs-lookup"><span data-stu-id="13f23-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="13f23-104">除了 COM + 中的工具之外，Microsoft 還提供下列工具來協助開發人員建立分散式應用程式：</span><span class="sxs-lookup"><span data-stu-id="13f23-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="13f23-105">Microsoft Data Access Components (MDAC) 。</span><span class="sxs-lookup"><span data-stu-id="13f23-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="13f23-106">Microsoft 提供數個可從無數來源抓取資料的途徑。</span><span class="sxs-lookup"><span data-stu-id="13f23-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="13f23-107">例如，OLE DB 提供一組用於建立資料庫元件的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="13f23-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="13f23-108">系統會定義介面，讓資料提供者可以根據基礎資料存放區的功能來執行不同層級的支援。</span><span class="sxs-lookup"><span data-stu-id="13f23-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="13f23-109">由於 OLE DB 是以 COM 為基礎，因此可以輕鬆擴充，並將擴充功能實作為新的介面。</span><span class="sxs-lookup"><span data-stu-id="13f23-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="13f23-110">OLE DB 也包含應用層級的程式設計介面，稱為 ActiveX Data Objects (ADO) 。</span><span class="sxs-lookup"><span data-stu-id="13f23-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="13f23-111">ADO 會公開雙重介面，因此可以輕鬆地從指令碼語言使用，以及 Microsoft Visual C++、Visual Basic 和其他開發人員工具。</span><span class="sxs-lookup"><span data-stu-id="13f23-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="13f23-112">開發人員也可以選擇使用泛型、廠商中立的 API，例如 Microsoft 開放式資料庫連接 (ODBC) 應用程式開發介面 (API) 。</span><span class="sxs-lookup"><span data-stu-id="13f23-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="13f23-113">ODBC API 是一種 C 語言介面，可讓您使用結構化查詢語言 (SQL)  (SQL) 來存取 DBMS 中的資料。</span><span class="sxs-lookup"><span data-stu-id="13f23-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="13f23-114">ODBC 驅動程式管理員會提供程式設計介面和執行時間元件，以找出 DBMS 特定的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="13f23-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="13f23-115">ODBC 驅動程式通常是由 DBMS 廠商提供，可將 ODBC 驅動程式管理員的一般呼叫轉譯成原生資料存取方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="13f23-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="13f23-116">使用 ODBC API 的主要優點是，您只需要學習一個 API 來存取廣泛的 Dbms。</span><span class="sxs-lookup"><span data-stu-id="13f23-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="13f23-117">Microsoft SQL Server。</span><span class="sxs-lookup"><span data-stu-id="13f23-117">Microsoft SQL Server.</span></span> <span data-ttu-id="13f23-118">除了提供穩固且 eloquent 的關係資料庫系統之外，Microsoft SQL Server 可以提供具有連接共用和安全性的分散式應用程式，而該應用程式可以與 Windows 安全性模型整合。</span><span class="sxs-lookup"><span data-stu-id="13f23-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="13f23-119">COM 交易整合 (COMTI) 。</span><span class="sxs-lookup"><span data-stu-id="13f23-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="13f23-120">COMTI 可以用來將大型主機系統整合到 Windows 系統，包括 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="13f23-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="13f23-121">COMTI 使用標準通訊 (協定，例如，在 Windows 電腦和大型主機與 minicomputers 之間通訊的 LU 6.2) 。</span><span class="sxs-lookup"><span data-stu-id="13f23-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13f23-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="13f23-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f23-123">COM + 設計假設和原則</span><span class="sxs-lookup"><span data-stu-id="13f23-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="13f23-124">使用 UML 設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="13f23-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="13f23-125">使用 COM + 的一般設計秘訣</span><span class="sxs-lookup"><span data-stu-id="13f23-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="13f23-126">優化與 COM + 商務邏輯層的互動</span><span class="sxs-lookup"><span data-stu-id="13f23-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



