---
title: Active Directory 服務介面架構
description: 許多目錄服務都是階層式的，因此會成為階層式物件模型。 本節使用 COM 物件表示來說明各種 ADSI 功能。
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory 服務介面架構 ADSI
- ADSI ADSI，關於，架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671196"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="16010-106">Active Directory 服務介面架構</span><span class="sxs-lookup"><span data-stu-id="16010-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="16010-107">許多目錄服務都是階層式的，因此會成為階層式物件模型。</span><span class="sxs-lookup"><span data-stu-id="16010-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="16010-108">本節使用 COM 物件表示來說明各種 ADSI 功能。</span><span class="sxs-lookup"><span data-stu-id="16010-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="16010-109">在下列物件模型圖中，最上層系統物件會針對每個已安裝的 ADSI 提供者，各包含一個命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="16010-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![命名空間容器物件](images/ds2top.png)

<span data-ttu-id="16010-111">每個命名空間物件本身都是一個容器，其中包含每個伺服器、網域的最上層根節點，或任何其他類型的目錄系統物件在每個目錄服務中定義為根目錄。</span><span class="sxs-lookup"><span data-stu-id="16010-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="16010-112">ADSI 提供一組預先定義的物件和介面，讓用戶端應用程式可以使用一組統一的方法與目錄服務互動。</span><span class="sxs-lookup"><span data-stu-id="16010-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="16010-113">不過，ADSI 可能無法提供目錄服務的所有功能存取權。</span><span class="sxs-lookup"><span data-stu-id="16010-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="16010-114">為了更妥善地使用每個目錄服務的完整功能集，ADSI 提供了一種架構模型，可讓目錄服務提供者和協力廠商軟體廠商用來擴充 ADSI 中所提供之介面以外的功能。</span><span class="sxs-lookup"><span data-stu-id="16010-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="16010-115">根節點容器物件（位於每個提供者命名空間物件內）包含 ADSI 架構容器物件。</span><span class="sxs-lookup"><span data-stu-id="16010-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="16010-116">此物件包含該提供者之所有功能的定義。</span><span class="sxs-lookup"><span data-stu-id="16010-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="16010-117">如需詳細資訊，請參閱 [ADSI 架構模型](adsi-schema-model.md)。</span><span class="sxs-lookup"><span data-stu-id="16010-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="16010-118">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="16010-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="16010-119">Active Directory 服務介面物件</span><span class="sxs-lookup"><span data-stu-id="16010-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="16010-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="16010-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="16010-121">Active Directory 服務介面提供者</span><span class="sxs-lookup"><span data-stu-id="16010-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="16010-122">ADSI 架構模型</span><span class="sxs-lookup"><span data-stu-id="16010-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




