---
title: IPropertyStorage-獨立執行
description: 系統提供的 IPropertySetStorage 獨立實作為 IPropertyStorage 的執行，此介面會在屬性集儲存體中讀取和寫入屬性。
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-獨立執行
- IPropertyStorage Strctd Stg.，獨立部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375653"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>IPropertyStorage-獨立執行

系統提供的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 獨立實作為 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的執行，此介面會在屬性集儲存體中讀取和寫入屬性。 **IPropertySetStorage** 介面會在儲存體中建立並開啟屬性集。 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)和 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面也會在獨立的執行中提供。

若要取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)之獨立執行的指標，請呼叫 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)函式來建立新的屬性集或 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) ，以取得現有屬性集的介面指標 (或呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)獨立執行) 的 [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)或 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法。

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行會在任何儲存或資料流程物件上建立屬性集，而不只是在複合檔案儲存和資料流程上。 獨立的執行不相依于複合檔案，並且可搭配任何結構化儲存體的執行使用。 如需此介面之複合檔案執行的詳細資訊，請參閱 [IPropertyStorage 複合檔案執行](ipropertystorage-compound-file-implementation.md)。

## <a name="when-to-use"></a>使用時機

使用 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 來管理單一屬性集內的屬性。 其方法支援讀取、寫入和刪除屬性，以及可與屬性識別碼相關聯的選擇性字串名稱。 其他方法支援標準認可和還原儲存體作業。 另外還有一種方法可設定與屬性儲存體相關聯的時間，另一種方法則允許指派 CLSID 來將其他程式碼（例如使用者介面程式碼）與屬性集建立關聯。 [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)方法會提供 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)之獨立執行的指標，它會列舉集合中的屬性。

## <a name="version-0-and-version-1-property-set-formats"></a>版本0和第1版屬性集格式

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行同時支援 version 0 和 version 1 property set 序列化格式。 如需詳細資訊，請參閱 [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)。 除非要求新功能，否則會以 version 0 格式建立屬性集，並保留該格式。 屆時，格式會更新為第1版。

例如，如果使用 PROPSETFLAG 預設旗標建立屬性集 \_ ，其格式為0版。 只要符合版本0格式的屬性類型會寫入至該屬性集並從該屬性集讀取，屬性集會維持為版本0格式。 如果第1版屬性類型寫入屬性集，屬性集會自動更新為第1版。 之後，只有瞭解0版的執行，就無法再讀取該屬性集。

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage 和 Variant 類型

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行不支援在 \_ \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **vt** 成員中，以 vt 未知或 vt 的 variant 類型。

SafeArray 內支援下列 variant 類型：也就是說，這些值可以與 \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的 vt 陣列合併。



IPropertyStorage 的複合檔案執行在 SafeArray 內支援的 Variant 類型[ ](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ INT

VT \_ UINT

VT \_ R4

VT \_ R8

VT \_ CY

VT \_ 日期

VT \_ BSTR

VT \_ BOOL

VT \_ DECIMAL

VT \_ 錯誤

VT \_ 變異

 



 

當 VT \_ VARIANT 與 vt 陣列合併時 \_ ，SafeArray 本身會保存 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。 不過，這些元素的類型必須取自上述清單，不能是 VT \_ 變異，也不能包含 vt \_ 向量、vt \_ 陣列或 vt \_ BYREF 指標。

## <a name="ipropertystorage-methods"></a>IPropertyStorage 方法

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行支援下列方法：

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

讀取 *rgpspec* 陣列中所指定的屬性，並在 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)元素的 *rgvar* 陣列中提供所有有效屬性的值。

在系統提供的獨立執行中，參考資料流或儲存類型的重複屬性識別碼會導致多個對 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 或 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 的呼叫，而 [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 的成功或失敗取決於基礎儲存體實作為共用開啟儲存體的能力。

此外，若要確保安全線程作業，如果相同的資料流程或儲存值屬性透過相同的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 指標多次要求，則會根據屬性是否已開啟，以及基礎檔案系統是否處理多個資料流程或儲存區的開啟而定，開啟會成功或失敗。 因此，在資料流程或儲存值屬性上的 [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 作業一律會導致呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)或 [**IStorage：： OPENSTORAGE**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)，傳遞存取 (STGM \_ READWRITE，例如) 和共用值 (STGM \_ 共用 \_ 獨佔，例如在最初開啟或建立屬性集時所指定) 。

如果方法失敗，寫入 *rgvar* 的值 \[ \] 就不會定義。 如果已成功開啟部分資料流程或儲存值屬性，但執行完成之前發生錯誤，則應該在方法傳回之前釋放這些屬性。

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

寫入 *rgpspec* 陣列中指定的屬性 \[ \] ，並將 *rgvar* 中指定的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)標記和值指派給它們 \[ \] 。 已存在的屬性會指派指定的 **PROPVARIANT** 值，而且不會建立目前存在的屬性。

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage：:D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

刪除在 *rgpspec* 中指定的屬性 \[ \] 。

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

讀取與 *rgpropid* 陣列中所指定屬性識別碼相關聯的現有字串名稱 \[ \] 。

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

將 *rglpwstrName* 陣列中指定的字串名稱指派給 *rgpropid* 陣列中所指定的屬性識別碼。

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage：:D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

藉由將 **Null** 寫入屬性名稱，來刪除 *rgpropid* 陣列中所指定之屬性識別碼的字串名稱。

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

設定屬性集資料流程的 **CLSID** 。 在獨立的執行中，在簡單屬性集上設定 CLSID (其中一個可以包含儲存或資料流程值屬性（如 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) 中所述）也會在基礎 substorage 上設定 clsid，以便透過呼叫 [**IStorage：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)來取得它。

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

針對簡單和簡單的屬性集，將記憶體映射排清到磁片子系統。 此外，針對簡單交易模式屬性集，這個方法會在屬性集上呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 。

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage：： Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

僅針對簡單屬性集，會呼叫基礎儲存體的 [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) 方法，並重新開啟「內容」資料流程。 針對簡單的屬性集，只會傳回 E \_ OK。

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

建立會執行 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的列舉值物件，您可以呼叫這些方法來列舉 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，以提供集合中每個屬性的相關資訊。

這項執行會建立一個陣列，以讀取整個屬性集，並在呼叫 [**IEnumSTATPROPSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 時共用。

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage：： Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

填入 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的成員，其中包含整個屬性集的相關資訊。 傳回時，提供結構的指標。

針對簡單儲存集，此實作為呼叫 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (或 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) ，以從基礎儲存體或資料流程取得資訊。

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

僅針對簡單屬性集，設定基礎儲存體所支援的時間。 這項 [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) 的執行會呼叫基礎儲存體的 [**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) 方法，以修改時間。 它支援基礎方法支援的時間，可能是修改時間、存取時間或建立時間。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPropertySetStorage-獨立執行](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 