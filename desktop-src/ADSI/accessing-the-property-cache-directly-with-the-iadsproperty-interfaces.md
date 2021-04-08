---
title: 存取具有 IADsProperty 介面的屬性快取
description: IADsProperty 介面包含 IADsPropertyList、IADsPropertyEntry 和 IADsPropertyValue。
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- 使用 IADsProperty 介面 ADSI 直接存取屬性快取
- 屬性快取 ADSI
- 屬性快取 ADSI，使用 IADsProperty 介面存取屬性快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2019
ms.locfileid: "103932843"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a><span data-ttu-id="a2b9d-106">存取具有 IADsProperty 介面的屬性快取</span><span class="sxs-lookup"><span data-stu-id="a2b9d-106">Accessing Property Cache with IADsProperty Interfaces</span></span>

<span data-ttu-id="a2b9d-107">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)介面包含 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)、 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-107">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interfaces consist of [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span></span> <span data-ttu-id="a2b9d-108">這些介面會提供方法來直接存取和操作物件快取的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-108">These interfaces provide methods to directly access and manipulate the properties of an object cache.</span></span> <span data-ttu-id="a2b9d-109">屬性（property）稱為屬性專案（property），並對應至架構中定義的屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-109">A property is known as a property entry and corresponds to an attribute defined in the schema.</span></span> <span data-ttu-id="a2b9d-110">屬性專案可以有一個或多個屬性值。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-110">A property entry can have one, or many, property values.</span></span> <span data-ttu-id="a2b9d-111">一組屬性專案會組織為屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-111">A set of property entries are organized as a property list.</span></span>

<span data-ttu-id="a2b9d-112">[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)介面會管理 ADSI 物件的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-112">The [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface manages the property list of an ADSI object.</span></span> <span data-ttu-id="a2b9d-113">[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)介面會為屬性專案執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-113">The [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface performs this operation for a property entry.</span></span> <span data-ttu-id="a2b9d-114">同樣地， [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 介面代表一個或多個屬性值。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-114">Similarly, the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface represents one, or more, property values.</span></span> <span data-ttu-id="a2b9d-115">它們一起提供一種機制，讓使用者能夠：</span><span class="sxs-lookup"><span data-stu-id="a2b9d-115">Together, they provide a mechanism for users to:</span></span>

-   <span data-ttu-id="a2b9d-116">直接使用屬性快取。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-116">Work directly with the property cache.</span></span>
-   <span data-ttu-id="a2b9d-117">使用不含架構的目錄，例如 LDAP 版本2伺服器。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-117">Work with directories that do not contain schemas, such as an LDAP version 2 server.</span></span>

<span data-ttu-id="a2b9d-118">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* 介面會嚴格地在屬性快取上運作，而且不會嘗試與伺服器互動，以取得或修改持續性存放區中的資料。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-118">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)\* interfaces operate strictly on the property cache and do not make any attempt to cooperate with the server to retrieve or modify the data in the persistent store.</span></span> <span data-ttu-id="a2b9d-119">因此，這些介面只能用來檢查及操作用戶端快取中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-119">As such, these interfaces are used only to examine and manipulate properties in the client cache.</span></span> <span data-ttu-id="a2b9d-120">在使用這些介面之前，您必須明確地呼叫 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法或 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 方法，以將物件屬性載入至快取中（如果快取尚未初始化）。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-120">Before using these interfaces, you must call the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method or the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method explicitly to load the object properties into the cache, if the cache has not been initialized.</span></span> <span data-ttu-id="a2b9d-121">呼叫這些介面的方法之後，您必須呼叫 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 來保存基礎目錄存放區的變更。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-121">After calling the methods of these interfaces, you must call [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) to persist the changes to the underlying directory store.</span></span>

<span data-ttu-id="a2b9d-122">如需可用來執行這些介面的詳細資訊和程式碼範例，請參閱 [使用 IADsProperty 介面存取屬性快取的範例程式碼](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)。</span><span class="sxs-lookup"><span data-stu-id="a2b9d-122">For more information and a code example that can used to implement these interfaces, see [Example Code for Using IADsProperty Interfaces to Access the Property Cache](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span></span>

 

 




