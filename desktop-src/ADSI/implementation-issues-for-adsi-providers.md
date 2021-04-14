---
title: ADSI 提供者的執行問題
description: ADSI 提供者的執行問題
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- ADSI 提供者 ADSI 的執行問題
- 提供者 ADSI、執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382877"
---
# <a name="implementation-issues-for-adsi-providers"></a>ADSI 提供者的執行問題

若要執行 ADSI 介面，請先執行 COM 介面 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)。 藉由將此介面提供為最少量的額外負荷層級，您可以提供用戶端應用程式直接從目錄存取目錄物件所需的控制項，而不是透過 ADSI 快取來優化網路效能。 使用這個介面也會提供您自己的實作為彈性。

其次，請執行基本的 ADSI 介面、 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)、 [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)、 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)、 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) 屬性快取介面。 [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) 和 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) 也是系統管理軟體經常需要的介面。

第三，如果您的目錄服務具有基礎架構，請執行架構管理介面： [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)、 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)。 如果沒有基礎架構，請使用這些介面來抽象化目錄服務所使用的類別和屬性。 架構可以用來將目錄服務的功能發行至 ADSI 用戶端。

## <a name="collections"></a>集合

ADSI 提供者元件可以遵循三個模型中的其中一個來快取列舉期間的集合。 當集合中的物件從 ADSI 的外部基礎目錄服務中刪除時，快取模型的選擇會決定 ADSI 的行為。

快取模型包括：

-   預先快取的集合。 當呼叫 [**IADsCollection：： get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum)來建立新的枚舉器物件時，會從基礎目錄服務完整地取出物件實例的集合。 如果從基礎目錄服務中刪除已抓取集合中 Active Directory 物件實例的來源物件，用戶端就無法辨識刪除，直到 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 或 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 嘗試存取集合為止。
-   以累加方式快取的集合。 當呼叫 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 時，會從基礎目錄服務一次取出一個物件的集合。 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) 將會回到快取中集合的開頭，而 **IEnumVARIANT：： Next** 會傳回快取的物件，直到到達快取的結尾為止，此時會從基礎存放區加入新的物件。 當 Active Directory 物件實例位於快取中時，用戶端將不會察覺其從基礎目錄服務刪除，直到 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 或 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 嘗試存取物件為止。
-   未快取的集合。 當呼叫 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 時，會從基礎目錄服務一次取出一個物件的集合。 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) 將會回到基礎存放區中集合的開頭。 **IEnumVARIANT：： Next** 和 **IEnumVARIANT：： Reset** 作業無法抓取刪除的物件，因為物件是從基礎目錄服務依需求抓取。 只會快取目前的物件;如果刪除目前的物件，用戶端就不會察覺其從基礎目錄服務刪除，直到 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 或 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 嘗試存取該物件為止。

無論快取模型為何，請注意 ADSI 列舉會將 Active Directory 的服務介面傳回給呼叫者。 為了避免取得新介面指標的額外負荷，ADSI 應用程式應該快取所要操作物件的傳回介面指標。 例如，列舉容器的 Visual Basic 應用程式，並以名稱填入清單方塊，可以快取與名稱相關聯的介面指標，以供稍後使用。 當使用者進行選取時，這個方法會提供比在列舉期間填入清單方塊，以及取得新介面指標的效能更高的效能。

## <a name="about-dispatch-ids"></a>關於分派識別碼

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) 是 com 針對未直接使用 com 介面的控制器定義的自動化介面。 透過 **IDispatch** 存取物件稱為「名稱系結」或「晚期繫結」存取，因為它會在執行時間發生 ( 「晚期」 ) 並使用屬性和方法的字串名稱來解析 ( "name" ) 的參考。 在執行時間，用戶端會將其想要呼叫之屬性或方法的字串名稱傳遞給 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) () 方法。 如果物件上有屬性或方法，則會取出對應函式 (dispID) 的分派識別碼。 接著會使用 dispID 透過 [**IDispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) () 來執行函數。 使用 **IDispatch**，單一物件所公開介面上的屬性和方法會顯示為一般清單。 由於名稱系結存取需要兩個函式呼叫，因此它的效率不如直接使用 COM 介面。 當效能是考慮時，建議用戶端在物件上使用 ADSI COM 介面。 如果介面符合資料類型和參數傳遞的自動化條件約束，則 Advanced Automation 控制器（例如 Visual Basic 4.0）可以呼叫其他 COM 介面和 **IDispatch**。

ADSI 提供者會動態產生每個 Active Directory 物件的 Dispid。 針對給定物件，透過 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 抓取的 dispid 為產生的值，但不是物件的 IDL 中的值。 [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) 使用者必須呼叫 **GetIDsOfNames** ，才能在執行時間取得有效的 dispid。

## <a name="type-information-and-type-libraries"></a>類型資訊和型別程式庫

ADSI SDK 提供的類型程式庫（Activeds），可記錄 ADSI 所支援的所有標準介面。 提供者必須針對在 Activeds 中找到的所有介面提供類似的類型程式庫，以及提供者元件內所執行介面的任何其他類型資料。

以下是 IDL 程式碼範例。

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>執行緒安全性

元件物件模型 (COM) 描述下列三種執行緒模型。 COM 應用程式會指出使用 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 和 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函式初始化 COM 程式庫時，所使用的模型：

-   單一線程。 單一執行緒模型假設進程中的單一執行緒執行，進一步假設進程中的 COM 資料結構不需要存取序列化。
-   單元執行緒。 COM 物件與建立它的執行緒相關聯。 呼叫另一個執行緒上的物件時，必須由建立該物件的執行緒執行。 為了達成此目的，來源執行緒會叫用用戶端 proxy 來排列方法呼叫，並透過與目的地線程相關聯的 Win32 訊息佇列，將它傳遞至目的地線程中的伺服器 stub 函數。
-   自由執行緒。 COM 物件會假設為安全線程。 允許多個執行緒存取進程中的任何物件，而不會強加任何序列化。

ADSI 並非採用任何特定的執行緒模型。 提供者元件的寫入器應該採用自由執行緒模型，並保證其內部資料結構的一致性，方法是藉由使用同步處理物件（例如重要區段或信號）來保護它們免于安全線程的安全，也就是不協調的更新。

## <a name="object-locking"></a>物件鎖定

ADSI 不會強加或定義物件鎖定配置。 使用鎖定來支援存取序列化的命名空間提供者，可以透過 ADSI 的提供者專屬延伸來公開基礎鎖定配置。

## <a name="property-names-within-a-schema"></a>架構中的屬性名稱

ADSI 會將屬性工作表示為 ADSI 架構容器內的屬性物件。 這需要在每個架構容器內都有唯一的屬性名稱。 提供者必須確定沒有名稱衝突。

## <a name="primary-interface"></a>主要介面

當提供者無法識別應以主要介面傳回的介面時，應傳回 **IID \_ IADs** 。 這會透過 [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) 提供物件之所有屬性的名稱系結存取，以及 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get)、 [**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)、 [**IADs：:P**](/windows/desktop/api/Iads/nf-iads-iads-put)，以及 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法。

 

 