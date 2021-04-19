---
title: 物件與屬性
description: 在 SDO 中，物件的特性取決於物件的屬性，以及與這些屬性相關聯的值。
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967907"
---
# <a name="objects-and-properties"></a><span data-ttu-id="75c9c-103">物件與屬性</span><span class="sxs-lookup"><span data-stu-id="75c9c-103">Objects and Properties</span></span>

<span data-ttu-id="75c9c-104">在 SDO 中，物件的特性取決於物件的屬性，以及與這些屬性相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="75c9c-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="75c9c-105">不同于其他的物件模型，SDO 物件本身沒有方法。</span><span class="sxs-lookup"><span data-stu-id="75c9c-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="75c9c-106">不過，SDO 物件確實會公開提供方法的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="75c9c-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="75c9c-107">SDO 中的物件會公開 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面，以提供處理物件屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="75c9c-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="75c9c-108">若要存取物件的屬性，請取得物件的 **ISdo** 介面，並使用 [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 和 [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) 介面方法來取得和設定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="75c9c-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="75c9c-109">抓取 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 的主題包含範例程式碼，示範如何取得使用者物件的 **ISdo** 介面。</span><span class="sxs-lookup"><span data-stu-id="75c9c-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="75c9c-110">對物件的屬性進行變更之後，請使用 [**ISdo：： Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) 方法，將變更寫入至物件的持續性儲存區。</span><span class="sxs-lookup"><span data-stu-id="75c9c-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="75c9c-111">您可以藉由呼叫 [**ISdo：： Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore)方法，在呼叫 **ISdo：： Apply** 之前，取消對物件屬性所做的變更。</span><span class="sxs-lookup"><span data-stu-id="75c9c-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="75c9c-112">這個方法會從持續性儲存體還原物件屬性的值。</span><span class="sxs-lookup"><span data-stu-id="75c9c-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="75c9c-113">下表顯示列舉 SDO 中某些物件屬性的列舉類型。</span><span class="sxs-lookup"><span data-stu-id="75c9c-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="75c9c-114">Object</span><span class="sxs-lookup"><span data-stu-id="75c9c-114">Object</span></span>                                 | <span data-ttu-id="75c9c-115">列舉類型</span><span class="sxs-lookup"><span data-stu-id="75c9c-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="75c9c-116">所有 SDO 物件</span><span class="sxs-lookup"><span data-stu-id="75c9c-116">All SDO objects</span></span>                        | [<span data-ttu-id="75c9c-117">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="75c9c-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="75c9c-118">User 物件</span><span class="sxs-lookup"><span data-stu-id="75c9c-118">User Object</span></span>                            | [<span data-ttu-id="75c9c-119">**USERPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="75c9c-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="75c9c-120"> (網路原則伺服器的服務物件) </span><span class="sxs-lookup"><span data-stu-id="75c9c-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="75c9c-121">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="75c9c-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="75c9c-122">Microsoft RADIUS 通訊協定物件</span><span class="sxs-lookup"><span data-stu-id="75c9c-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="75c9c-123">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="75c9c-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="75c9c-124">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="75c9c-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="75c9c-125">集合</span><span class="sxs-lookup"><span data-stu-id="75c9c-125">Collections</span></span>

<span data-ttu-id="75c9c-126">物件通常群組為集合。</span><span class="sxs-lookup"><span data-stu-id="75c9c-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="75c9c-127">SDO API 透過 [**ISdo 集合**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) 介面提供功能，以列舉集合中的物件，以及加入和刪除集合中的物件。</span><span class="sxs-lookup"><span data-stu-id="75c9c-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="75c9c-128">取得集合的存取權的方法是在包含集合的物件上取得集合屬性。</span><span class="sxs-lookup"><span data-stu-id="75c9c-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="75c9c-129">如需詳細資訊，請參閱 [物件模型](/windows/desktop/Nps/sdo-object-model-hierarchy)階層中的一節。</span><span class="sxs-lookup"><span data-stu-id="75c9c-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="75c9c-130">所有對應至集合之屬性的資料類型都是 VT \_ 分派。</span><span class="sxs-lookup"><span data-stu-id="75c9c-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c9c-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="75c9c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c9c-132">SDO 物件模型階層</span><span class="sxs-lookup"><span data-stu-id="75c9c-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="75c9c-133">SDO 支援的屬性</span><span class="sxs-lookup"><span data-stu-id="75c9c-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 