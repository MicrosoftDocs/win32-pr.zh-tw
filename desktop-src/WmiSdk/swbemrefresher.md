---
description: SWbemRefresher 物件是容器物件，可重新整理所有新增至該物件之物件的資料。 新增的物件集合，SWbemRefreshableItem 實例所代表的每個專案都可以被視為集合和列舉。
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: 'SWbemRefresher 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945673"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="9a4c2-104">SWbemRefresher 物件</span><span class="sxs-lookup"><span data-stu-id="9a4c2-104">SWbemRefresher object</span></span>

<span data-ttu-id="9a4c2-105">**SWbemRefresher** 物件是一個容器物件，可重新整理所有新增至該物件之物件的資料。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="9a4c2-106">可以在容器中新增或移除單一實例和實例枚舉器。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="9a4c2-107">新增的物件集合、 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 實例所代表的每個專案都可以被視為集合和列舉。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="9a4c2-108">來自任何類別的 WMI 實例都可以加入至 **SWbemRefresher** 物件。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="9a4c2-109">即使實例資料的提供者不是高效能的提供者，重新整理程式物件仍可以更新重新 [**整理呼叫上的資料**](swbemrefresher-refresh.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="9a4c2-110">如果資料是透過高效能提供者所提供，而且 [**AutoReconnect**](swbemrefresher-autoreconnect.md) 屬性為 **TRUE**，則 **SWbemRefresher** 物件會嘗試重新建立與資料提供者的連接中斷。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="9a4c2-111">這個物件可以由 VBScript **CreateObject** 呼叫建立。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="9a4c2-112">您可以呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md)或 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)方法來執行重新整理作業。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="9a4c2-113">成員</span><span class="sxs-lookup"><span data-stu-id="9a4c2-113">Members</span></span>

<span data-ttu-id="9a4c2-114">**SWbemRefresher** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9a4c2-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="9a4c2-115">方法</span><span class="sxs-lookup"><span data-stu-id="9a4c2-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="9a4c2-116">屬性</span><span class="sxs-lookup"><span data-stu-id="9a4c2-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9a4c2-117">方法</span><span class="sxs-lookup"><span data-stu-id="9a4c2-117">Methods</span></span>

<span data-ttu-id="9a4c2-118">**SWbemRefresher** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="9a4c2-119">方法</span><span class="sxs-lookup"><span data-stu-id="9a4c2-119">Method</span></span>                                        | <span data-ttu-id="9a4c2-120">描述</span><span class="sxs-lookup"><span data-stu-id="9a4c2-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a4c2-121">**添加**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="9a4c2-122">將新的可重新整理物件加入至重新整理器物件中的集合。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="9a4c2-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="9a4c2-124">將新的枚舉器加入至複習物件。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="9a4c2-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="9a4c2-126">從複習物件中的集合移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="9a4c2-127">**項目**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="9a4c2-128">從集合傳回指定的複習專案。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="9a4c2-129">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="9a4c2-130">更新複習物件中包含的所有專案。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="9a4c2-131">**移除**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="9a4c2-132">從複習中移除重新整理者專案物件或具有指定索引的物件集。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9a4c2-133">屬性</span><span class="sxs-lookup"><span data-stu-id="9a4c2-133">Properties</span></span>

<span data-ttu-id="9a4c2-134">**SWbemRefresher** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="9a4c2-135">屬性</span><span class="sxs-lookup"><span data-stu-id="9a4c2-135">Property</span></span>                                                         | <span data-ttu-id="9a4c2-136">存取類型</span><span class="sxs-lookup"><span data-stu-id="9a4c2-136">Access type</span></span>          | <span data-ttu-id="9a4c2-137">Description</span><span class="sxs-lookup"><span data-stu-id="9a4c2-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a4c2-138">**AutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="9a4c2-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="9a4c2-139">Read-only</span></span><br/> | <span data-ttu-id="9a4c2-140">指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="9a4c2-141">**計數**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="9a4c2-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="9a4c2-142">Read-only</span></span><br/> | <span data-ttu-id="9a4c2-143">包含複習物件中的專案數。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="9a4c2-144">範例</span><span class="sxs-lookup"><span data-stu-id="9a4c2-144">Examples</span></span>

<span data-ttu-id="9a4c2-145">下列範例說明如何建立 **SWbemRefresher** 物件，並使用 [**Add**](swbemrefresher-add.md) 和 [**AddEnum**](swbemrefresher-addenum.md) 方法來儲存單一實例和列舉實例、重新整理資料，以及使用 Item 屬性來取得 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9a4c2-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="9a4c2-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a4c2-146">Requirements</span></span>



| <span data-ttu-id="9a4c2-147">需求</span><span class="sxs-lookup"><span data-stu-id="9a4c2-147">Requirement</span></span> | <span data-ttu-id="9a4c2-148">值</span><span class="sxs-lookup"><span data-stu-id="9a4c2-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4c2-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a4c2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4c2-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a4c2-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a4c2-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a4c2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4c2-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a4c2-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a4c2-153">標頭</span><span class="sxs-lookup"><span data-stu-id="9a4c2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4c2-154"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4c2-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a4c2-155">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9a4c2-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a4c2-156"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a4c2-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a4c2-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9a4c2-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a4c2-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a4c2-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a4c2-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="9a4c2-159">CLSID</span></span><br/>                    | <span data-ttu-id="9a4c2-160">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="9a4c2-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="9a4c2-161">IID</span><span class="sxs-lookup"><span data-stu-id="9a4c2-161">IID</span></span><br/>                      | <span data-ttu-id="9a4c2-162">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="9a4c2-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="9a4c2-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a4c2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4c2-164">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="9a4c2-165">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="9a4c2-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="9a4c2-166">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="9a4c2-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




