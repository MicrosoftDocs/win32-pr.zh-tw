---
title: 執行 Active Directory 服務介面提供者
description: Active Directory 服務介面 (ADSI) 是可包裝目錄服務物件的 COM 介面，以便將它們公開給目錄服務的用戶端。 藉由提供 ADSI 的執行，您可以將用戶端的基礎擴展至一組 ADSI 用戶端應用程式。
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- 執行 Active Directory 服務介面提供者 ADSI
- 執行 ADSI 提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671143"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="541e3-106">執行 Active Directory 服務介面提供者</span><span class="sxs-lookup"><span data-stu-id="541e3-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="541e3-107">Active Directory 服務介面 (ADSI) 是可包裝目錄服務物件的 COM 介面，以便將它們公開給目錄服務的用戶端。</span><span class="sxs-lookup"><span data-stu-id="541e3-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="541e3-108">藉由提供 ADSI 的執行，您可以將用戶端的基礎擴展至一組 ADSI 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="541e3-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="541e3-109">如同任何 COM 的執行，您可以撰寫許多語言的 ADSI 提供者。</span><span class="sxs-lookup"><span data-stu-id="541e3-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="541e3-110">ADSI COM 介面定義為雙重介面，可同時允許執行時間和編譯時期的名稱解析，並可透過自動化相容的語言（例如 Visual Basic、Visual Basic Scripting Edition，以及 C 和 c + + 等更具效能和效率的語言）來呼叫。</span><span class="sxs-lookup"><span data-stu-id="541e3-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="541e3-111">ADSI 用戶端也包含透過 Microsoft Management Console 使用 Active Server 網頁和系統管理嵌入式管理單元的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="541e3-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="541e3-112">因為 ADSI 提供自己的 OLE DB 提供者，所以執行 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 所定義的搜尋功能也可讓 ADSI 用戶端查詢目錄服務中的資料。</span><span class="sxs-lookup"><span data-stu-id="541e3-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="541e3-113">所有目錄服務物件都可以透過支援 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)的一般 ADSI 物件來表示。</span><span class="sxs-lookup"><span data-stu-id="541e3-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="541e3-114">ADSI 提供所需的組建區塊，以代表任何目錄服務的功能和服務。</span><span class="sxs-lookup"><span data-stu-id="541e3-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="541e3-115">此外，ADSI 中繼介面代表目錄管理員所使用的一般物件。</span><span class="sxs-lookup"><span data-stu-id="541e3-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="541e3-116">您可以將中繼介面的屬性對應至您目錄服務所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="541e3-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="541e3-117">當安裝提供者並重新啟動系統時，ADSI 用戶端對 Active Directory 服務介面進行程式設計時，就能取得目錄服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="541e3-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="541e3-118">如果您的目錄服務支援架構標記法，則支援架構管理介面可讓您的命名空間直接存取目錄服務瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="541e3-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="541e3-119">藉由透過架構發佈您的功能，用戶端可以在線上查詢您的目錄服務，並利用您提供的服務。</span><span class="sxs-lookup"><span data-stu-id="541e3-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="541e3-120">由於線上架構的可用性和 COM 介面的優勢，您可以在支援舊版的用戶端軟體時，繼續提供新功能。</span><span class="sxs-lookup"><span data-stu-id="541e3-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




