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
# <a name="comadmincatalogobject-class"></a>COMAdminCatalogObject 類別

代表 COM + 目錄中集合內的專案。 您可以使用它來取得和修改集合中的專案所公開的屬性。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|------------------------------------------|
| 介面 | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>使用時機

使用從 **COMAdminCatalogObject** 類別建立的物件，來修改 com + 目錄中集合所包含之專案的屬性。 這些專案會對應至 [元件服務] 系統管理工具的主控台樹中，顯示在資料夾內的專案。 元件服務管理工具中的資料夾對應至目錄中的集合，您可以使用從 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 類別建立的物件來表示。

並非所有透過 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 和 **COMAdminCatalogObject** 公開的集合和專案都可在「元件服務」系統管理工具中使用。

如需特定集合及其屬性的相關資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。

如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

## <a name="remarks"></a>備註

您無法直接建立 **COMAdminCatalogObject** 物件。 若要使用這個物件的方法，您必須建立 [**COMAdminCatalog**](comadmincatalog.md) 物件、取得 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)的參考，然後使用 [**ICOMAdminCatalog：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) 取得代表最上層集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考，或使用 [**ICatalogCollection：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) 來存取非最上層集合。

當您有興趣之集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考之後，請呼叫 [**ICatalogCollection：:P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) ，以將其所有專案填入集合中。 藉由呼叫 [**ICatalogCollection：： get \_ 專案**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) 來逐一查看集合中的每個專案，以取得每個 [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) 介面的參考。 當您找到感興趣的專案時，您可以修改專案的屬性，並結束反復專案。 如果您對集合中的任何專案進行任何變更，您必須呼叫 [**ICatalogCollection：： SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 以將變更儲存至 com + 類別目錄。

這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱;「專案名稱」必須取代為您感興趣的專案名稱;"PropertyName" 必須取代為您要在專案中修改的屬性名稱;和 varNewProp 必須由包含屬性之新值的 VARIANT 取代。


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



若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 COM + 系統管理員類型程式庫。 您可以藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)或 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)來建立 COMAdminCatalogCollection 物件。

呼叫 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)方法，以填入集合中的所有專案。 逐一查看集合中的每個專案。 當您找到感興趣的專案時，您可以修改專案的屬性，並結束反復專案。 如果您對集合中的任何專案進行任何變更，您必須呼叫 **COMAdminCatalogCollection** 物件的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)方法，以將變更儲存至 com + 類別目錄。

這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱;「專案名稱」必須取代為您感興趣的專案名稱;"PropertyName" 必須取代為您要在專案中修改的屬性名稱;和 NewPropValue 必須由屬性的新值取代。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>ComAdmin。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin .Idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




