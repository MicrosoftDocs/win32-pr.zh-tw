---
description: 若要從一個 Windows Installer 套件安裝產品的多個實例，您必須撰寫產品的基底安裝套件，以及要安裝的每個實例的實例轉換，以及基底實例。
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: 使用實例轉換撰寫多個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977873"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a><span data-ttu-id="c3e6b-103">使用實例轉換撰寫多個實例</span><span class="sxs-lookup"><span data-stu-id="c3e6b-103">Authoring Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="c3e6b-104">若要從一個 Windows Installer 套件安裝產品的多個實例，您必須撰寫產品的基底安裝套件，以及要安裝的每個實例的實例轉換，以及基底實例。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-104">To install multiple instances of a product from one Windows Installer package, you need to author a base installation package for the product and an instance transform for each instance to be installed in addition to the base instance.</span></span> <span data-ttu-id="c3e6b-105">撰寫基底套件和轉換時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="c3e6b-105">Use the following guidelines when authoring your base package and transforms:</span></span>

-   <span data-ttu-id="c3e6b-106">您的安裝應用程式可以檢查 Windows Vista、Windows Server 2003、Windows XP Service Pack 1 (SP1) 和 Windows Installer 3.0 可轉散發套件上執行的安裝程式是否存在。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-106">Your setup application can check for the presence of the installer running on a version of Windows Vista, Windows Server 2003, Windows XP with Service Pack 1 (SP1), and the Windows Installer 3.0 redistributable.</span></span> <span data-ttu-id="c3e6b-107"> (或更新版本) 的任何安裝程式版本都必須使用產品程式碼-變更轉換，從單一套件安裝多個實例。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-107">Any of these installer versions (or later) are required to install multiple instances from a single package using a product code–changing transform.</span></span>
-   <span data-ttu-id="c3e6b-108">每個實例都必須有唯一的產品代碼和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-108">Each instance must have a unique product code and instance identifier.</span></span> <span data-ttu-id="c3e6b-109">您可以在基底封裝中定義屬性，其值可以設定為實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-109">You may define a property in the base package, the value of which can be set to the instance identifier.</span></span>
-   <span data-ttu-id="c3e6b-110">為了讓每個實例的檔案保持隔離，基底封裝應該將檔案安裝到相依于實例識別碼的目錄位置。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-110">To keep the files of each instance isolated, the base package should install files into a directory location that depends on the instance identifier.</span></span>
-   <span data-ttu-id="c3e6b-111">為了讓每個實例的非資料保持隔離，基底封裝應該將非資料的資料收集到每個實例的元件集合中。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-111">To keep the nonfile data of each instance isolated, the base package should collect nonfile data into sets of components for each instance.</span></span> <span data-ttu-id="c3e6b-112">接著應根據相依于實例識別碼的條件陳述式來安裝適當的元件。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-112">The appropriate components should then be installed based on conditional statements that depend on the instance identifier.</span></span>
-   <span data-ttu-id="c3e6b-113">除了基底實例之外，還會針對每個要安裝的實例撰寫實例轉換。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-113">Author an instance transform for each instance being installed in addition to the base instance.</span></span> <span data-ttu-id="c3e6b-114">基底套件可能會安裝自己的實例。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-114">The base package may install its own instance.</span></span>
-   <span data-ttu-id="c3e6b-115">實例轉換必須變更每個實例的產品代碼和識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-115">The instance transform must change the product code and identifier for each instance.</span></span>
-   <span data-ttu-id="c3e6b-116">建議產品轉換也會變更產品名稱，以便透過主控台在 [新增/移除程式] 中輕鬆分辨實例。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-116">It is recommended that the product transform also change the product name so that the instance is readily distinguished in Add/Remove Programs through Control Panel.</span></span>
-   <span data-ttu-id="c3e6b-117">如果實例轉換會安裝檔案，它們應該安裝在相依于實例識別碼的目錄中。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-117">If the instance transform installs files, they should be installed in a directory that depends on the instance identifier.</span></span>
-   <span data-ttu-id="c3e6b-118">所有非資料（例如登錄機碼）都應該在其路徑中包含實例名稱，以避免發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-118">All nonfile data, such as registry keys, should include the instance name in their path to prevent collisions.</span></span> <span data-ttu-id="c3e6b-119">您可以使用其值為路徑中實例識別碼的屬性來完成這項作業，如下列登錄 [表](registry-table.md)範例所示。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-119">This can be accomplished by using the property whose value is the instance identifier in the path as shown by the following example of a [Registry Table](registry-table.md).</span></span>



| <span data-ttu-id="c3e6b-120">登錄</span><span class="sxs-lookup"><span data-stu-id="c3e6b-120">Registry</span></span> | <span data-ttu-id="c3e6b-121">Root</span><span class="sxs-lookup"><span data-stu-id="c3e6b-121">Root</span></span> | <span data-ttu-id="c3e6b-122">按鍵</span><span class="sxs-lookup"><span data-stu-id="c3e6b-122">Key</span></span>                                            | <span data-ttu-id="c3e6b-123">名稱</span><span class="sxs-lookup"><span data-stu-id="c3e6b-123">Name</span></span>         | <span data-ttu-id="c3e6b-124">值</span><span class="sxs-lookup"><span data-stu-id="c3e6b-124">Value</span></span>           | <span data-ttu-id="c3e6b-125">元件\_</span><span class="sxs-lookup"><span data-stu-id="c3e6b-125">Component\_</span></span>      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| <span data-ttu-id="c3e6b-126">Reg1</span><span class="sxs-lookup"><span data-stu-id="c3e6b-126">Reg1</span></span>     | <span data-ttu-id="c3e6b-127">1</span><span class="sxs-lookup"><span data-stu-id="c3e6b-127">1</span></span>    | <span data-ttu-id="c3e6b-128">Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\]</span><span class="sxs-lookup"><span data-stu-id="c3e6b-128">Software\\Microsoft\\MyProduct\\\[InstanceId\]</span></span> | <span data-ttu-id="c3e6b-129">InstanceGuid</span><span class="sxs-lookup"><span data-stu-id="c3e6b-129">InstanceGuid</span></span> | <span data-ttu-id="c3e6b-130">\[ProductCode\]</span><span class="sxs-lookup"><span data-stu-id="c3e6b-130">\[ProductCode\]</span></span> | <span data-ttu-id="c3e6b-131">NonFileDataComp1</span><span class="sxs-lookup"><span data-stu-id="c3e6b-131">NonFileDataComp1</span></span> |



 

<span data-ttu-id="c3e6b-132">如需詳細資訊，請參閱 [安裝多個產品的實例和修補程式](installing-multiple-instances-of-products-and-patches.md) ，以及 [使用實例轉換來安裝多個實例](installing-multiple-instances-with-instance-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="c3e6b-132">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Installing Multiple Instances with Instance Transforms](installing-multiple-instances-with-instance-transforms.md).</span></span>

 

 



