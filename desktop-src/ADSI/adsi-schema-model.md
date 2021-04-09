---
title: ADSI 架構模型
description: 架構類似于字典，因為它會保留目錄服務已知之每個物件類型的定義。
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI 架構模型 ADSI
- ADSI ADSI、about、schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eec9264ae2692952106802cc06cbad937a42a9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933607"
---
# <a name="adsi-schema-model"></a><span data-ttu-id="851d9-105">ADSI 架構模型</span><span class="sxs-lookup"><span data-stu-id="851d9-105">ADSI Schema Model</span></span>

<span data-ttu-id="851d9-106">架構類似于字典，因為它會保留目錄服務已知之每個物件類型的定義。</span><span class="sxs-lookup"><span data-stu-id="851d9-106">A schema is similar to a dictionary in that it holds the definition of every type of object known to a directory service.</span></span> <span data-ttu-id="851d9-107">ADSI 用戶端應用程式可以流覽架構，以探索任何指定 ADSI 執行的功能。</span><span class="sxs-lookup"><span data-stu-id="851d9-107">ADSI client applications can browse through a schema to discover the features of any given ADSI implementation.</span></span> <span data-ttu-id="851d9-108">此外，ADSI 也提供架構管理介面，可用來與目錄服務的基礎架構進行通訊。</span><span class="sxs-lookup"><span data-stu-id="851d9-108">In addition, ADSI supplies schema management interfaces that can be used to communicate with a directory service's underlying schema.</span></span>

<span data-ttu-id="851d9-109">某些架構是可擴充的，且 ADSI 提供者或協力廠商可能會選擇為現有介面發佈新的介面或其他屬性。</span><span class="sxs-lookup"><span data-stu-id="851d9-109">Some schemas are extensible and ADSI providers or third-party suppliers may choose to publish new interfaces or additional properties for existing interfaces there.</span></span> <span data-ttu-id="851d9-110">ADSI 用戶端會使用此資料來判斷每個目錄服務所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="851d9-110">ADSI clients use this data to determine what features are supported for each directory service.</span></span>

<span data-ttu-id="851d9-111">有三種類型的架構物件：類別、屬性和語法，分別支援架構管理介面 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)和 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)。</span><span class="sxs-lookup"><span data-stu-id="851d9-111">There are three kinds of schema objects: classes, properties, and syntaxes, each respectively supporting the schema management interfaces [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), and [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).</span></span>

> [!Note]  
> <span data-ttu-id="851d9-112">類別是多載的詞彙。</span><span class="sxs-lookup"><span data-stu-id="851d9-112">Class is an overloaded term.</span></span> <span data-ttu-id="851d9-113">有 c + + 類別、JAVA 類別、COM 類別和 ADSI 類別。</span><span class="sxs-lookup"><span data-stu-id="851d9-113">There are C++ classes, Java classes, COM classes, and ADSI classes.</span></span> <span data-ttu-id="851d9-114">在本檔中，除非另有限定，否則 word 類別會參考架構物件的類別或類型。</span><span class="sxs-lookup"><span data-stu-id="851d9-114">In this document, the word class, unless otherwise qualified, refers to a category or type of schema object.</span></span>

 

<span data-ttu-id="851d9-115">ADSI 會摘要每個目錄服務的架構，並將它放在 **命名空間** 物件中的每個最上層根節點。</span><span class="sxs-lookup"><span data-stu-id="851d9-115">ADSI abstracts the schema of every directory service and places it in every top-level root node in the **Namespace** object.</span></span> <span data-ttu-id="851d9-116">若要識別目錄服務在給定根節點上支援哪些類別，您可以列舉架構物件，並取得類別物件、屬性物件和語法物件的清單。</span><span class="sxs-lookup"><span data-stu-id="851d9-116">To identify what classes a directory service supports on a given root-node, you enumerate the schema object and get a list of class objects, property objects, and syntax objects.</span></span> <span data-ttu-id="851d9-117">如需詳細資訊，請參閱 [使用 ADSI 架構](using-the-adsi-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="851d9-117">For more information, see [Using the ADSI Schema](using-the-adsi-schema.md).</span></span>

## <a name="adsi-ldap-provider-schema-cache"></a><span data-ttu-id="851d9-118">ADSI LDAP 提供者架構快取</span><span class="sxs-lookup"><span data-stu-id="851d9-118">ADSI LDAP Provider Schema Cache</span></span>

<span data-ttu-id="851d9-119">ADSI 的 LDAP 提供者會嘗試將架構資料快取到本機電腦。</span><span class="sxs-lookup"><span data-stu-id="851d9-119">The LDAP provider for ADSI attempts to cache schema data to the local computer.</span></span> <span data-ttu-id="851d9-120">Ubschema 是以 [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) 屬性中儲存的分辨名稱來識別，位於目錄服務 Enterprise (rootDSE) 的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="851d9-120">A subschema is identified by a distinguished name stored in the [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) attribute located in the root of the directory service enterprise (rootDSE).</span></span> <span data-ttu-id="851d9-121">除了提供 ubschema 資料之外，LDAP v3 伺服器也應該公開 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性，以用來判斷上次修改架構的時間。</span><span class="sxs-lookup"><span data-stu-id="851d9-121">In addition to providing the subschema data, LDAP v3 servers should expose a [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) attribute that is used to determine the last time the schema was modified.</span></span>

<span data-ttu-id="851d9-122">ADSI 初次系結至 LDAP 伺服器時，會使用 [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) 屬性來抓取 ubschema 的資料。</span><span class="sxs-lookup"><span data-stu-id="851d9-122">When ADSI first binds to the LDAP server, it retrieves the subschema data using the [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) attribute.</span></span> <span data-ttu-id="851d9-123">如果 ADSI 成功尋找 ubschema 物件，它會將資料指標儲存在連線到 LDAP 伺服器之電腦上的登錄中。</span><span class="sxs-lookup"><span data-stu-id="851d9-123">If ADSI succeeds in finding the subschema object, it stores a pointer to the data in the registry on the computer that is connecting to the LDAP server.</span></span> <span data-ttu-id="851d9-124">如需有關這些值儲存在登錄中的確切資訊，請參閱 [ADSI 和使用者帳戶控制](adsi-and-uac.md)。</span><span class="sxs-lookup"><span data-stu-id="851d9-124">For information on exactly where these values are stored in the registry, see [ADSI and User Account Control](adsi-and-uac.md).</span></span>

<span data-ttu-id="851d9-125">ADSI 接著會嘗試處理架構資料並讀取 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性。</span><span class="sxs-lookup"><span data-stu-id="851d9-125">ADSI then attempts to process the schema data and reads the [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) attribute.</span></span> <span data-ttu-id="851d9-126">如果 **modifyTimeStamp** 屬性存在且 adsi 成功處理架構，adsi 會將 ubschema 寫入磁片，並在機碼底下建立兩個下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="851d9-126">If the **modifyTimeStamp** attribute exists and ADSI successfully processes the schema, ADSI writes the subschema to disk and creates the two following registry values under the key.</span></span> <span data-ttu-id="851d9-127">如果 ubschema 資料存在，但無法處理，則不會建立這些登錄值：</span><span class="sxs-lookup"><span data-stu-id="851d9-127">If the subschema data exists, but cannot be processed, neither of these registry values is created:</span></span>

-   <span data-ttu-id="851d9-128">**時間** 值，包含 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp)屬性。</span><span class="sxs-lookup"><span data-stu-id="851d9-128">A **Time** value, which contains the [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) attribute.</span></span> <span data-ttu-id="851d9-129">這個值是用來確保架構資料是最新的，並防止架構資料的常數重載。</span><span class="sxs-lookup"><span data-stu-id="851d9-129">This value is used to ensure that the schema data is current and prevents the constant reloading of the schema data.</span></span>
-   <span data-ttu-id="851d9-130">檔案 **值，** 包含 ADSI 將架構資料儲存在檔案系統中的路徑。</span><span class="sxs-lookup"><span data-stu-id="851d9-130">A **File** value, which contains the path to where ADSI stores the schema data in the file system.</span></span> <span data-ttu-id="851d9-131">根據預設，ADSI 會將 ubschema 快取在 <systemroot> \\ SchCache 目錄中，並以對應至 LDAP 伺服器名稱的檔案名來快取。</span><span class="sxs-lookup"><span data-stu-id="851d9-131">By default, ADSI caches the subschema in the <systemroot>\\SchCache directory with a file name corresponding to the name of the LDAP server.</span></span>

<span data-ttu-id="851d9-132">如果可處理 ubschema 資料，但未公開 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性，則會將架構資料快取在記憶體中，但不會寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="851d9-132">If the subschema data can be processed, but no [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) attribute is exposed, the schema data is cached in memory, but not written to disk.</span></span> <span data-ttu-id="851d9-133">如果已透過本機電腦上的 ADSI 連接到 LDAP v3 伺服器，而且快取的 ubschema 不存在，最有可能是下列其中一個原因：</span><span class="sxs-lookup"><span data-stu-id="851d9-133">If an LDAP v3 server has been contacted through ADSI on the local computer and a cached subschema is not present, it is most likely for one of the following reasons:</span></span>

-   <span data-ttu-id="851d9-134">伺服器未公開正確的屬性。</span><span class="sxs-lookup"><span data-stu-id="851d9-134">The server did not expose the correct properties.</span></span>
-   <span data-ttu-id="851d9-135">ADSI 無法處理架構。</span><span class="sxs-lookup"><span data-stu-id="851d9-135">ADSI was unable to process the schema.</span></span>
-   <span data-ttu-id="851d9-136">ADSI 無法將檔案寫入檔案系統。</span><span class="sxs-lookup"><span data-stu-id="851d9-136">ADSI was unable to write the file to the file system.</span></span>

 

 