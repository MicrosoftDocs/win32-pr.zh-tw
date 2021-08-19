---
description: 代表 COM + 目錄中的任何集合。 您可以使用它來列舉、新增、移除和取出集合中的專案，以及存取相關集合。
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: 'COMAdminCatalogCollection 類別 (ComAdmin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 3656e65b89ae02b0cfe8ea3b1dbe9784d679c5eb40e11edbfe2951e08893e1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029478"
---
# <a name="comadmincatalogcollection-class"></a>COMAdminCatalogCollection 類別

代表 COM + 目錄中的任何集合。 您可以使用它來列舉、新增、移除和取出集合中的專案，以及存取相關集合。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|--------------------------------------------------|
| 介面 | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>使用時機

當您想要以程式設計方式操作 COM + 目錄中的集合時，請使用從 **COMAdminCatalogCollection** 類別建立的物件。 這些集合會對應到 [元件服務] 系統管理工具中的資料夾。 資料夾內的專案會對應至集合中的專案，您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件來表示。

如需有關目錄及其屬性之集合的詳細資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。

如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

## <a name="remarks"></a>備註

您無法直接建立 **COMAdminCatalogCollection** 物件。 若要使用這個物件的方法，您必須建立 [**COMAdminCatalog**](comadmincatalog.md) 物件、取得 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)的參考，然後使用 [**ICOMAdminCatalog：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) 取得代表最上層集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考。 這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱。


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 com + 系統管理員類型程式庫。 您可以藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)來建立 COMAdminCatalogCollection 物件。 這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱。


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>ComAdmin。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ComAdmin .Idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




