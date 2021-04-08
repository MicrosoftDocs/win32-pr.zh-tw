---
title: 使用 Active Directory 服務介面
description: " (ADSI) 的 Active Directory 服務介面，可讓目錄服務的用戶端應用程式使用一組介面，來與提供 ADSI 執行的任何命名空間進行通訊。"
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- 使用 Active Directory 服務介面 ADSI
- ADSI ADSI，使用
- Active Directory 服務介面 ADSI，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839119"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="f9113-106">使用 Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="f9113-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="f9113-107"> (ADSI) 的 Active Directory 服務介面，可讓目錄服務的用戶端應用程式使用一組介面，來與提供 ADSI 執行的任何命名空間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f9113-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="f9113-108">ADSI 用戶端會使用定義完善的 Active Directory 服務介面來取代網路專屬的 API 呼叫，以取得更簡單的命名空間服務存取權。</span><span class="sxs-lookup"><span data-stu-id="f9113-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="f9113-109">Active Directory 服務介面符合元件物件模型 (COM) 並支援標準 COM 功能。</span><span class="sxs-lookup"><span data-stu-id="f9113-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="f9113-110">ADSI 提供的介面符合與名稱系結控制器（例如 JAVA、Microsoft Visual Basic 開發系統和 Visual Basic Scripting Edition (VBScript) ）的自動化。</span><span class="sxs-lookup"><span data-stu-id="f9113-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="f9113-111">ADSI 也可以提供介面，以將不符合自動化規範的介面效能優化，以與 C 和 c + + 等語言環境搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f9113-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="f9113-112">ADSI 也提供非自動化介面 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)，以支援目錄物件管理和查詢。</span><span class="sxs-lookup"><span data-stu-id="f9113-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="f9113-113">此外，ADSI 也提供自己的 OLE DB 提供者，因此任何已使用 OLE DB 的用戶端（包括使用 ActiveX Data Objects 的用戶端）都可以直接查詢目錄服務。</span><span class="sxs-lookup"><span data-stu-id="f9113-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="f9113-114">使用 Active Server Pages 的 Web 應用程式也可以透過 ADSI 來設計目錄服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="f9113-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="f9113-115">ADSI 用戶端可以用程式設計方式探索網站上的所有 ADSI 提供者，並使用相同的介面來與每個命名空間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f9113-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="f9113-116">當安裝其他提供者時，ADSI 用戶端也可以透過新的命名空間進行通訊，而不需要重新編譯。</span><span class="sxs-lookup"><span data-stu-id="f9113-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="f9113-117">此程式設計指南說明 ADSI 的運作方式，並提供在 ADSI 中執行特定工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="f9113-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="f9113-118">我們將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="f9113-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="f9113-119">系結至 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="f9113-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="f9113-120">建立和刪除物件</span><span class="sxs-lookup"><span data-stu-id="f9113-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="f9113-121">使用 ADSI 存取及運算元據</span><span class="sxs-lookup"><span data-stu-id="f9113-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="f9113-122">使用 ADSI 架構</span><span class="sxs-lookup"><span data-stu-id="f9113-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="f9113-123">集合和群組</span><span class="sxs-lookup"><span data-stu-id="f9113-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="f9113-124">列舉 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="f9113-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="f9113-125">搜尋 Active Directory</span><span class="sxs-lookup"><span data-stu-id="f9113-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="f9113-126">ADSI 安全性模型</span><span class="sxs-lookup"><span data-stu-id="f9113-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="f9113-127">ADSI 擴充功能</span><span class="sxs-lookup"><span data-stu-id="f9113-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="f9113-128">搭配 Exchange 使用 ADSI</span><span class="sxs-lookup"><span data-stu-id="f9113-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="f9113-129">ADSI 公用程式介面</span><span class="sxs-lookup"><span data-stu-id="f9113-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="f9113-130">使用 JAVA/COM 編寫 ADSI 程式設計</span><span class="sxs-lookup"><span data-stu-id="f9113-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




