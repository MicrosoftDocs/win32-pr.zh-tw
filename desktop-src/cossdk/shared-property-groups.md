---
description: 為了避免不同物件所建立的屬性發生名稱衝突，共用屬性管理員 (SPM) 使用共用屬性群組。
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: 共用屬性群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "103696032"
---
# <a name="shared-property-groups"></a><span data-ttu-id="106ca-103">共用屬性群組</span><span class="sxs-lookup"><span data-stu-id="106ca-103">Shared Property Groups</span></span>

<span data-ttu-id="106ca-104">為了避免不同物件所建立的屬性發生名稱衝突，共用屬性管理員 (SPM) 使用共用屬性群組。</span><span class="sxs-lookup"><span data-stu-id="106ca-104">To prevent name collisions among properties created by different objects, the shared property manager (SPM) uses shared property groups.</span></span> <span data-ttu-id="106ca-105">共用屬性群組只是一組共用屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="106ca-105">A shared property group is simply a namespace for a set of shared properties.</span></span> <span data-ttu-id="106ca-106">共用屬性群組中的每個屬性都包含名稱、值和共用屬性群組內的位置。</span><span class="sxs-lookup"><span data-stu-id="106ca-106">Each property within a shared property group consists of a name, a value, and a position within the shared property group.</span></span> <span data-ttu-id="106ca-107">您可以使用名稱或位置來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="106ca-107">Either the name or the position can be used to retrieve the property value.</span></span> <span data-ttu-id="106ca-108">您可以透過共用屬性群組管理員來存取和建立共用屬性群組。</span><span class="sxs-lookup"><span data-stu-id="106ca-108">You can access and create shared property groups through the shared property group manager.</span></span>

<span data-ttu-id="106ca-109">下圖顯示 SPM 物件模型。</span><span class="sxs-lookup"><span data-stu-id="106ca-109">The SPM object model is shown in the following illustration.</span></span>

![顯示 SPM 物件模型的圖表： ISharedPropertyGroupManager、ISharedPropertyGroup 到 ISharedProperty。](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

<span data-ttu-id="106ca-111">以下是共用屬性管理員的介面：</span><span class="sxs-lookup"><span data-stu-id="106ca-111">The following are interfaces of the shared property manager:</span></span>

-   <span data-ttu-id="106ca-112">[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) 可用來建立共用屬性群組，以及取得現有共用屬性群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="106ca-112">[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) is used to create shared property groups and to obtain access to existing shared property groups.</span></span> <span data-ttu-id="106ca-113">您可以使用 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)或 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)物件的實例，以存取 **ISharedPropertyGroupManager** 介面。</span><span class="sxs-lookup"><span data-stu-id="106ca-113">You can access the **ISharedPropertyGroupManager** interface by creating an instance of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object by using either [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) or [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

-   <span data-ttu-id="106ca-114">[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) 是用來建立及存取共用屬性群組中的共用屬性。</span><span class="sxs-lookup"><span data-stu-id="106ca-114">[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) is used to create and access the shared properties in a shared property group.</span></span> <span data-ttu-id="106ca-115">您可以使用 [**ISharedPropertyGroupManager：： CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup)方法來建立 [**SharedPropertyGroup**](sharedpropertygroup.md)物件，以存取 **ISharedPropertyGroup** 介面。</span><span class="sxs-lookup"><span data-stu-id="106ca-115">You can access the **ISharedPropertyGroup** interface by creating a [**SharedPropertyGroup**](sharedpropertygroup.md) object with the [**ISharedPropertyGroupManager::CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method.</span></span> <span data-ttu-id="106ca-116">如同任何 COM 物件一樣，您必須在使用完 **SharedPropertyGroup** 物件之後，再加以釋放。</span><span class="sxs-lookup"><span data-stu-id="106ca-116">As with any COM object, you must release a **SharedPropertyGroup** object when you have finished using it.</span></span>

-   <span data-ttu-id="106ca-117">[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) 可用來設定或抓取共用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="106ca-117">[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) is used to set or retrieve the value of a shared property.</span></span> <span data-ttu-id="106ca-118">共用屬性可包含任何可由 Variant 表示的資料類型。</span><span class="sxs-lookup"><span data-stu-id="106ca-118">A shared property can contain any data type that can be represented by a Variant.</span></span> <span data-ttu-id="106ca-119">您可以使用 [**ISharedPropertyGroup：： CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)方法或 [**ISharedPropertyGroup：： CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立 [**SharedProperty**](sharedproperty.md)物件，以存取 **ISharedProperty** 介面。</span><span class="sxs-lookup"><span data-stu-id="106ca-119">You can access the **ISharedProperty** interface by creating a [**SharedProperty**](sharedproperty.md) object with the [**ISharedPropertyGroup::CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) method or the [**ISharedPropertyGroup::CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) method.</span></span> <span data-ttu-id="106ca-120">只能從 [**SharedPropertyGroup**](sharedpropertygroup.md)物件內建立或存取 **SharedProperty** 物件。</span><span class="sxs-lookup"><span data-stu-id="106ca-120">A **SharedProperty** object can be created or accessed only from within a [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span> <span data-ttu-id="106ca-121">同樣地，當您使用完 **SharedProperty** 物件時，必須釋放它。</span><span class="sxs-lookup"><span data-stu-id="106ca-121">Again, you must release a **SharedProperty** object when you have finished using it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="106ca-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="106ca-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106ca-123">COM + 共用屬性管理員</span><span class="sxs-lookup"><span data-stu-id="106ca-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> </dl>

 

 
