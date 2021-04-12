---
title: 物件模型階層
description: '[SDO] 物件模型中的物件會排列在階層中。 這表示 SDO 中的物件可讓您存取 SDO 中的其他物件。'
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375876"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="2f8bb-104">物件模型階層</span><span class="sxs-lookup"><span data-stu-id="2f8bb-104">Object Model Hierarchy</span></span>

<span data-ttu-id="2f8bb-105">[SDO] 物件模型中的物件會排列在階層中。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="2f8bb-106">這表示 SDO 中的物件可讓您存取 SDO 中的其他物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="2f8bb-107">物件可讓您以兩種方式存取其他物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="2f8bb-108">其中一個方法是讓物件公開介面，以提供方法來取得其他物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="2f8bb-109">這種方法的範例是 Machine 物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="2f8bb-110">Machine 物件會公開 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) 介面。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="2f8bb-111">[**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)方法會捕獲服務物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="2f8bb-112">[**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)方法會捕獲使用者物件。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![公開 isdomachine 介面的電腦物件](images/sdo01.png)

<span data-ttu-id="2f8bb-114">如需詳細資訊，請參閱 [取得服務和使用者 SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos)。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="2f8bb-115">物件提供其他物件之存取權的第二種方式，是將物件集合表示為包含該物件的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="2f8bb-116">若要取出物件集合，請在代表集合之物件的屬性上呼叫 [**ISdo：： GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="2f8bb-117">例如，若要取出原則集合，請在 NPS 物件所公開的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)介面上呼叫 **ISdo：： GetProperty** 。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="2f8bb-118">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![正在抓取原則集合](images/sdo02.png)

<span data-ttu-id="2f8bb-120">如需抓取原則集合的範例程式碼，請參閱抓取 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection)。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="2f8bb-121">[**NPS 伺服器資料物件**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)具有代表集合的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="2f8bb-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="2f8bb-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>核 數 師</span><span class="sxs-lookup"><span data-stu-id="2f8bb-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-123">審計員集合中唯一的審計員是 [**NT 事件記錄**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties)檔。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>政策</span><span class="sxs-lookup"><span data-stu-id="2f8bb-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-125">每個 [**原則物件**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) 都有一個代表條件集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>配置 檔</span><span class="sxs-lookup"><span data-stu-id="2f8bb-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-127">設定檔集合中的每個 [**設定檔物件**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) 都有一個代表屬性集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="2f8bb-128">請參閱 [Sdo 支援的屬性](/windows/desktop/Nps/sdo-sdo-supported-attributes) ，以取得 sdo 所支援的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>協定</span><span class="sxs-lookup"><span data-stu-id="2f8bb-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-130">通訊協定集合包含 RADIUS 通訊協定物件，其中包含代表 RADIUS 用戶端的用戶端集合。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="2f8bb-131">請參閱 [加入用戶端](/windows/desktop/Nps/sdo-adding-a-client) 以取得範例程式碼，以示範如何取出用戶端集合。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy 原則</span><span class="sxs-lookup"><span data-stu-id="2f8bb-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-133">此集合包含用於連接要求處理的網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy 設定檔</span><span class="sxs-lookup"><span data-stu-id="2f8bb-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-135">這個集合包含用於連接要求處理的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS 伺服器群組</span><span class="sxs-lookup"><span data-stu-id="2f8bb-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-137">RADIUS 伺服器群組集合中的每個 [**radius 伺服器群組**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) 都有一個屬性，代表該伺服器群組中的伺服器集合。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="2f8bb-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>要求處理常式</span><span class="sxs-lookup"><span data-stu-id="2f8bb-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="2f8bb-139">此集合包含「Microsoft 領域評估工具」集合。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="2f8bb-140">您也可以在此集合中取得「Microsoft NT SAM 驗證」和「Microsoft 帳戶處理」設定。</span><span class="sxs-lookup"><span data-stu-id="2f8bb-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2f8bb-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f8bb-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f8bb-142">SDO 物件和屬性</span><span class="sxs-lookup"><span data-stu-id="2f8bb-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="2f8bb-143">SDO 支援的屬性</span><span class="sxs-lookup"><span data-stu-id="2f8bb-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 