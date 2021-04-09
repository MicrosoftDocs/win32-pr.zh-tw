---
description: 代表 COM + 目錄中集合內的專案。 您可以使用它來取得和修改集合中的專案所公開的屬性。
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: 'COMAdminCatalogObject 類別 (ComAdmin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110645"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="47e2b-104">COMAdminCatalogObject 類別</span><span class="sxs-lookup"><span data-stu-id="47e2b-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="47e2b-105">代表 COM + 目錄中集合內的專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="47e2b-106">您可以使用它來取得和修改集合中的專案所公開的屬性。</span><span class="sxs-lookup"><span data-stu-id="47e2b-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="47e2b-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="47e2b-107">When to implement</span></span>

<span data-ttu-id="47e2b-108">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="47e2b-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="47e2b-109">需求</span><span class="sxs-lookup"><span data-stu-id="47e2b-109">Requirement</span></span> | <span data-ttu-id="47e2b-110">值</span><span class="sxs-lookup"><span data-stu-id="47e2b-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="47e2b-111">介面</span><span class="sxs-lookup"><span data-stu-id="47e2b-111">Interfaces</span></span> | [<span data-ttu-id="47e2b-112">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="47e2b-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="47e2b-113">使用時機</span><span class="sxs-lookup"><span data-stu-id="47e2b-113">When to use</span></span>

<span data-ttu-id="47e2b-114">使用從 **COMAdminCatalogObject** 類別建立的物件，來修改 com + 目錄中集合所包含之專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="47e2b-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="47e2b-115">這些專案會對應至 [元件服務] 系統管理工具的主控台樹中，顯示在資料夾內的專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="47e2b-116">元件服務管理工具中的資料夾對應至目錄中的集合，您可以使用從 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 類別建立的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="47e2b-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="47e2b-117">並非所有透過 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 和 **COMAdminCatalogObject** 公開的集合和專案都可在「元件服務」系統管理工具中使用。</span><span class="sxs-lookup"><span data-stu-id="47e2b-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="47e2b-118">如需特定集合及其屬性的相關資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="47e2b-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="47e2b-119">如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。</span><span class="sxs-lookup"><span data-stu-id="47e2b-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47e2b-120">備註</span><span class="sxs-lookup"><span data-stu-id="47e2b-120">Remarks</span></span>

<span data-ttu-id="47e2b-121">您無法直接建立 **COMAdminCatalogObject** 物件。</span><span class="sxs-lookup"><span data-stu-id="47e2b-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="47e2b-122">若要使用這個物件的方法，您必須建立 [**COMAdminCatalog**](comadmincatalog.md) 物件、取得 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)的參考，然後使用 [**ICOMAdminCatalog：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) 取得代表最上層集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考，或使用 [**ICatalogCollection：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) 來存取非最上層集合。</span><span class="sxs-lookup"><span data-stu-id="47e2b-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="47e2b-123">當您有興趣之集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考之後，請呼叫 [**ICatalogCollection：:P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) ，以將其所有專案填入集合中。</span><span class="sxs-lookup"><span data-stu-id="47e2b-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="47e2b-124">藉由呼叫 [**ICatalogCollection：： get \_ 專案**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) 來逐一查看集合中的每個專案，以取得每個 [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="47e2b-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="47e2b-125">當您找到感興趣的專案時，您可以修改專案的屬性，並結束反復專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="47e2b-126">如果您對集合中的任何專案進行任何變更，您必須呼叫 [**ICatalogCollection：： SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 以將變更儲存至 com + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="47e2b-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="47e2b-127">這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱;「專案名稱」必須取代為您感興趣的專案名稱;"PropertyName" 必須取代為您要在專案中修改的屬性名稱;和 varNewProp 必須由包含屬性之新值的 VARIANT 取代。</span><span class="sxs-lookup"><span data-stu-id="47e2b-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="47e2b-128">若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="47e2b-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="47e2b-129">您可以藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)或 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)來建立 COMAdminCatalogCollection 物件。</span><span class="sxs-lookup"><span data-stu-id="47e2b-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="47e2b-130">呼叫 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)方法，以填入集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="47e2b-131">逐一查看集合中的每個專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="47e2b-132">當您找到感興趣的專案時，您可以修改專案的屬性，並結束反復專案。</span><span class="sxs-lookup"><span data-stu-id="47e2b-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="47e2b-133">如果您對集合中的任何專案進行任何變更，您必須呼叫 **COMAdminCatalogCollection** 物件的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)方法，以將變更儲存至 com + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="47e2b-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="47e2b-134">這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱;「專案名稱」必須取代為您感興趣的專案名稱;"PropertyName" 必須取代為您要在專案中修改的屬性名稱;和 NewPropValue 必須由屬性的新值取代。</span><span class="sxs-lookup"><span data-stu-id="47e2b-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="47e2b-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="47e2b-135">Requirements</span></span>



| <span data-ttu-id="47e2b-136">需求</span><span class="sxs-lookup"><span data-stu-id="47e2b-136">Requirement</span></span> | <span data-ttu-id="47e2b-137">值</span><span class="sxs-lookup"><span data-stu-id="47e2b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47e2b-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47e2b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="47e2b-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47e2b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47e2b-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47e2b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="47e2b-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47e2b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47e2b-142">標頭</span><span class="sxs-lookup"><span data-stu-id="47e2b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e2b-143"><dt>ComAdmin。h</dt></span><span class="sxs-lookup"><span data-stu-id="47e2b-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="47e2b-144">Idl</span><span class="sxs-lookup"><span data-stu-id="47e2b-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47e2b-145"><dt>ComAdmin .Idl</dt></span><span class="sxs-lookup"><span data-stu-id="47e2b-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e2b-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47e2b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e2b-147">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="47e2b-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="47e2b-148">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="47e2b-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="47e2b-149">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="47e2b-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




