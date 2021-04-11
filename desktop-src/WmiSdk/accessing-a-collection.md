---
description: 集合是標準的自動化概念，可提供一組物件的統一介面，讓您可以執行反復專案。
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: 存取 WMI 集合
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b875f50c1778a03c304f90c019da172be6ef5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194714"
---
# <a name="accessing-a-wmi-collection"></a><span data-ttu-id="e81bb-103">存取 WMI 集合</span><span class="sxs-lookup"><span data-stu-id="e81bb-103">Accessing a WMI Collection</span></span>

<span data-ttu-id="e81bb-104">集合是標準的自動化概念，可提供一組物件的統一介面，讓您可以執行反復專案。</span><span class="sxs-lookup"><span data-stu-id="e81bb-104">A collection is a standard automation concept that provides a uniform interface to a set of objects over which you can perform iteration.</span></span> <span data-ttu-id="e81bb-105">適用于 WMI 的腳本 API 會公開一些符合集合範例的介面。</span><span class="sxs-lookup"><span data-stu-id="e81bb-105">The Scripting API for WMI exposes a number of interfaces that conform to the collection paradigm.</span></span> <span data-ttu-id="e81bb-106">在每個案例中，使用 **Item** 方法來識別使用包含值之字串的元素。</span><span class="sxs-lookup"><span data-stu-id="e81bb-106">In each case, use the **Item** method to identify the elements using a string containing the value.</span></span>

<span data-ttu-id="e81bb-107">[**內含**](swbempropertyset.md)、 [**SWbemQualifierSet**](swbemqualifierset.md)和 [**SWbemMethodSet**](swbemmethodset.md)集合大多用來修改架構。</span><span class="sxs-lookup"><span data-stu-id="e81bb-107">The [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemMethodSet**](swbemmethodset.md) collections are mostly used to modify schema.</span></span> <span data-ttu-id="e81bb-108">[**Swbemobjectset 搭配使用**](swbemobjectset.md)物件包含透過呼叫（例如 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**\_ SWBEMOBJECT. associators of**](swbemobject-associators-.md)）取得的 WMI 物件，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例。</span><span class="sxs-lookup"><span data-stu-id="e81bb-108">An [**SWbemObjectSet**](swbemobjectset.md) object contains WMI objects, such as a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance, that have been obtained through calls, such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemObject.Associators\_**](swbemobject-associators-.md).</span></span> <span data-ttu-id="e81bb-109">[**SWbemRefresher**](swbemrefresher.md)物件只能包含 WMI 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e81bb-109">The [**SWbemRefresher**](swbemrefresher.md) object can only contain instances of WMI classes.</span></span> <span data-ttu-id="e81bb-110">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件可能包含 WMI 物件或提供者針對方法呼叫所需的任何其他類型的資料。</span><span class="sxs-lookup"><span data-stu-id="e81bb-110">The [**SWbemNamedValueSet**](swbemnamedvalueset.md) object may contain WMI objects or any other type of data that a provider requires for the method call.</span></span>

> [!Note]  
> <span data-ttu-id="e81bb-111">下列主題主要是針對 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="e81bb-111">The following topics were written primarily for VBScript.</span></span> <span data-ttu-id="e81bb-112">C # 使用標準 [IEnumerable](/dotnet/api/system.collections.ienumerable) 介面來 collate 和列舉物件。</span><span class="sxs-lookup"><span data-stu-id="e81bb-112">C# uses the standard [IEnumerable](/dotnet/api/system.collections.ienumerable) interface to collate and enumerate objects.</span></span> <span data-ttu-id="e81bb-113">相反地，每當傳回值包含一個以上的結果時，PowerShell 通常會使用隱含的物件集合。</span><span class="sxs-lookup"><span data-stu-id="e81bb-113">In contrast, PowerShell generally uses an implicit object collection whenever a return value contains more than one result.</span></span>

 

<span data-ttu-id="e81bb-114">下表列出適用于 WMI 的腳本 API 中的集合，以及每個集合的元素和參數。</span><span class="sxs-lookup"><span data-stu-id="e81bb-114">The following table lists the collections in the Scripting API for WMI and the elements and parameters for each collection.</span></span>



| <span data-ttu-id="e81bb-115">集合</span><span class="sxs-lookup"><span data-stu-id="e81bb-115">Collection</span></span>                                       | <span data-ttu-id="e81bb-116">元素</span><span class="sxs-lookup"><span data-stu-id="e81bb-116">Element</span></span>                                              | <span data-ttu-id="e81bb-117">Item () 參數</span><span class="sxs-lookup"><span data-stu-id="e81bb-117">Item() Parameter</span></span>                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="e81bb-118">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="e81bb-118">**SWbemObjectSet**</span></span>](swbemobjectset.md)         | [<span data-ttu-id="e81bb-119">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="e81bb-119">**SWbemObject**</span></span>](swbemobject.md)                   | <span data-ttu-id="e81bb-120">物件路徑</span><span class="sxs-lookup"><span data-stu-id="e81bb-120">Object path</span></span>                                                              |
| [<span data-ttu-id="e81bb-121">**內含**</span><span class="sxs-lookup"><span data-stu-id="e81bb-121">**SWbemPropertySet**</span></span>](swbempropertyset.md)     | [<span data-ttu-id="e81bb-122">**Swbempropertyset**</span><span class="sxs-lookup"><span data-stu-id="e81bb-122">**SWbemProperty**</span></span>](swbemproperty.md)               | <span data-ttu-id="e81bb-123">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="e81bb-123">Property name</span></span>                                                            |
| [<span data-ttu-id="e81bb-124">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="e81bb-124">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)   | [<span data-ttu-id="e81bb-125">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="e81bb-125">**SWbemQualifier**</span></span>](swbemqualifier.md)             | <span data-ttu-id="e81bb-126">限定詞名稱</span><span class="sxs-lookup"><span data-stu-id="e81bb-126">Qualifier name</span></span>                                                           |
| [<span data-ttu-id="e81bb-127">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="e81bb-127">**SWbemMethodSet**</span></span>](swbemmethodset.md)         | [<span data-ttu-id="e81bb-128">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="e81bb-128">**SWbemMethod**</span></span>](swbemmethod.md)                   | <span data-ttu-id="e81bb-129">方法名稱</span><span class="sxs-lookup"><span data-stu-id="e81bb-129">Method name</span></span>                                                              |
| [<span data-ttu-id="e81bb-130">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="e81bb-130">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | [<span data-ttu-id="e81bb-131">**SWbemNamedValue**</span><span class="sxs-lookup"><span data-stu-id="e81bb-131">**SWbemNamedValue**</span></span>](swbemnamedvalue.md)           | <span data-ttu-id="e81bb-132">值名稱</span><span class="sxs-lookup"><span data-stu-id="e81bb-132">Value name</span></span>                                                               |
| [<span data-ttu-id="e81bb-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="e81bb-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)   | [<span data-ttu-id="e81bb-134">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="e81bb-134">**SWbemPrivilege**</span></span>](swbemprivilege.md)             | <span data-ttu-id="e81bb-135">許可權名稱</span><span class="sxs-lookup"><span data-stu-id="e81bb-135">Privilege name</span></span>                                                           |
| [<span data-ttu-id="e81bb-136">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="e81bb-136">**SWbemRefresher**</span></span>](swbemrefresher.md)         | [<span data-ttu-id="e81bb-137">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="e81bb-137">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) | <span data-ttu-id="e81bb-138">[**SWbemRefresher**](swbemrefresher.md)物件中專案的索引</span><span class="sxs-lookup"><span data-stu-id="e81bb-138">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object</span></span> |



 

<span data-ttu-id="e81bb-139">如需有關在集合中加入和移除專案的詳細資訊和範例，請參閱從集合 [移除單一專案](removing-a-single-item-from-a-collection.md) ，以及 [從集合中移除多個專案](removing-multiple-items-from-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="e81bb-139">For more information about and examples of adding and removing items from a collection, see [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md) and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span> <span data-ttu-id="e81bb-140">如需使用類別的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="e81bb-140">For more information about working with classes, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
