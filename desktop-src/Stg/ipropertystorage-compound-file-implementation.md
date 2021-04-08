---
title: IPropertyStorage-Compound 檔案的執行
description: 結構化儲存體架構的 COM 實作為所謂的複合檔案。
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd Stg.、執行、複合檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842423"
---
# <a name="ipropertystorage-compound-file-implementation"></a>IPropertyStorage-Compound 檔案的執行

結構化儲存體架構的 COM 實作為所謂的 [複合檔案](istorage-compound-file-implementation.md)。 在複合檔案中執行的儲存物件包括兩個 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的實作為：管理單一持續性屬性集的介面，以及管理持續性屬性集群組的介面 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)。 如需 **IPropertyStorage** 介面的詳細資訊，請參閱 **IPropertyStorage** 和 [屬性儲存體考慮](property-storage-considerations.md)。

若要取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行指標，請呼叫 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 來建立新的複合檔案物件或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ，以開啟先前建立的複合檔案物件。 在 **StgCreateStorageEx** 的案例中， *stgfmt* 參數應設為 stgfmt \_ 儲存體。 在 **StgOpenStorageEx** 的案例中， *stgfmt* 參數應設定為 stgfmt \_ 儲存體或 stgfmt \_ ANY。 在這兩種情況下，會將 *riid* 參數設定為 IID \_ IPropertySetStorage。 這兩個函數都會提供物件 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的指標。 藉由呼叫該介面的 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 或 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 方法，您將會取得 **IPropertyStorage** 介面的指標，您可以用它來呼叫其任何方法。

若要取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的複合檔案執行指標，另一種方式是呼叫較舊的 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 和 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) 函式，或將 IID IStorage 的 *riid* 參數指定 \_ 至 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函數。 在任一種情況下，都會傳回物件之 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的指標。 使用持續性屬性集，呼叫 **IPropertySetStorage** 介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，指定介面識別碼的標頭定義名稱 (iid) iid \_ IPropertySetStorage。

## <a name="when-to-use"></a>使用時機

使用 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 來管理單一屬性集內的屬性。 其方法支援讀取、寫入和刪除屬性，以及可與屬性識別碼相關聯的選擇性字串名稱。 其他方法支援標準認可和還原儲存體作業。 另外還有一種方法，可讓您設定與屬性儲存相關聯的時間，另一種方法則允許指派可以用來將其他程式碼（例如使用者介面程式碼）與屬性集相關聯的 CLSID。 呼叫 [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 方法會提供 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的複合檔案執行指標，可讓您列舉集合中的屬性。

> [!Note]  
> 如果您在簡單模式的屬性集儲存體上呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)、 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)、 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)來取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的指標， **IPropertyStorage** 方法會遵守簡單模式資料流程的規則。 如果是針對以 STGM simple 旗標建立或開啟的檔案取得該檔案，則該屬性集會儲存為簡單模式 \_ 。 在此情況下，不一定能讓基礎資料流程變得更大，也無法以較大的屬性取代現有的屬性。 如需詳細資訊，請參閱 [IPropertySetStorage 複合檔案執行](ipropertysetstorage-compound-file-implementation.md)。

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage 和快取

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行會將開啟的屬性集快取在記憶體中，以改善效能。 如此一來，就不會將屬性集的變更寫入至複合檔案，直到呼叫) 方法的 [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 或 **Release** (最後一個參考為止。

## <a name="simple-mode-property-sets"></a>簡單模式屬性集

如果屬性儲存物件是從簡單模式屬性集儲存物件建立，則為簡單模式。 例如，如果從 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函式取得屬性集的儲存物件，並在 \_ *GRFMODE* 參數中設定 STGM 簡單旗標，則會處於簡單模式。 請注意，「簡單模式」與「簡單屬性集」無關。 如果透過呼叫 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 和 \_ *grfFlags* 參數中所設定的 PROPSETFLAG 簡單旗標，來建立屬性集，則會很簡單。 如需簡單和簡單屬性集的詳細資訊，請參閱 [屬性集的儲存和資料流程物件](storage-vs--stream-for-a-property-set.md)。

當您建立簡單模式屬性儲存物件時，它的使用沒有任何限制。 開啟現有的簡單模式屬性儲存物件時，無法成長儲存屬性集的基礎資料流程物件。 因此，如果變更需要較大的資料流程，就不一定能夠修改這類的屬性儲存物件。

## <a name="property-set-formats"></a>屬性集格式

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行同時支援 version 0 和 version 1 property set 序列化格式。 在 Windows 2000 上執行的電腦上支援第1版的格式。 如需詳細資訊，請參閱 [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)。 除非要求新功能，否則會以 version 0 格式建立屬性集，並保留該格式。 發生這種情況時，格式會更新為第1版。

例如，如果使用 PROPSETFLAG 預設旗標建立屬性集 \_ ，其格式為0版。 只要符合版本0格式的屬性類型會寫入至該屬性集並從該屬性集讀取，屬性集會維持為版本0格式。 如果第1版屬性類型寫入屬性集，屬性集會自動更新為第1版。 之後，只能辨識版本0的執行程式無法再讀取該屬性集。

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage 和 Variant 類型

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行不支援在 \_ \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **vt** 成員中，以 vt 未知或 vt 的 variant 類型。

下表列出 SafeArray 內支援的 variant 類型。也就是說，這些值可以與 \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的 vt 陣列合併。



IPropertyStorage 的複合檔案執行在 SafeArray 內支援的 Variant 類型

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

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行支援下列方法：

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

讀取 *rgpspec* 陣列中所指定的屬性，並在 PROPVARIANTs 的 *rgvar* 陣列中提供所有有效屬性的值。 在 COM 複合檔案執行中，參考資料流或儲存體類型的重複屬性識別碼會導致多個對 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 或 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 的呼叫，而 **ReadMultiple** 的成功或失敗取決於基礎儲存體實作為共用開啟作業的能力。 因為在複合檔案 STGM 中 \_ ，會強制執行共用 \_ 獨佔，所以多次開啟嘗試將會失敗。 不支援從相同的父儲存體多次開啟相同的儲存物件。 \_ \_ 必須指定 STGM 共用專屬旗標。

此外，為了確保安全線程作業，如果相同的資料流程或儲存值屬性是透過 COM 複合檔案執行中的相同 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 指標來要求數次，則開啟作業將會成功或失敗，取決於屬性是否已開啟，以及基礎檔案系統是否處理資料流程或儲存體的多重進入。 因此，在資料流程或儲存值屬性上的 **ReadMultiple** 作業一律會導致呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)或 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)，此呼叫會將 access (STGM \_ READWRITE，依此類推，) 和共用旗標 (STGM \_ 共用 \_ 獨佔，以及在原始屬性集開啟或建立時所指定的) 。

如果方法失敗，寫入 *rgvar* 的值 \[ \] 就不會定義。 如果已成功開啟部分資料流程或儲存值屬性，但執行完成之前發生錯誤，則應該在方法傳回之前釋放。

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

寫入 *rgpspec* 陣列中指定的屬性 \[ \] ，並將 *rgvar* 中指定的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)標記和值指派給它們 \[ \] 。 已存在的屬性會指派指定的 **PROPVARIANT** 值。 目前不存在的屬性會建立。

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

刪除 *rgpropid* 陣列中所指定屬性的屬性名稱 \[ \] 。

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

設定屬性集資料流程的 **CLSID** 。 在複合檔案執行中，在簡單屬性集上設定 CLSID (可以合法包含儲存區或資料流程值屬性（如 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) 中所述）也會在基礎 substorage 上設定 clsid，以便透過呼叫 [**IStorage：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)來取得它。

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

針對簡單和簡單的屬性集，將屬性集記憶體影像排清到基礎儲存體。 此外，對於簡單交易模式屬性集，這個方法會在包含屬性集的儲存體上執行 commit (as in [**IStorage：： commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) 。

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage：： Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

僅針對簡單屬性集，會呼叫基礎儲存體的 [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) 方法，並重新開啟「內容」資料流程。 針對簡單的屬性集，這個介面一律會傳回 S \_ OK。 簡單屬性集是使用 \_ [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 方法中的 PROPSETFLAG 簡單旗標所建立的屬性集。 如需詳細資訊，請參閱 [屬性集的儲存和資料流程物件](storage-vs--stream-for-a-property-set.md) 。

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

會建立 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的實例，您可以呼叫這些方法來列舉 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，以提供集合中每個屬性的相關資訊。 這項執行會建立一個陣列，以讀取整個屬性集，並在呼叫 **IEnumSTATPROPSTG：： Clone** 時共用。 屬性集的變更不會反映在開啟的 **IEnumSTATPROPSTG** 實例中。 若要查看這類變更，必須建立此列舉值的新實例。

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage：： Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

填入 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的成員，其中包含整個屬性集的相關資料。 傳回時，提供結構的指標。 若為簡單儲存集，此實作為會呼叫 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (或 [**IStream：： stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) 從基礎儲存體或資料流程取得時間。 針對簡單的儲存集，將不會保留任何時間。

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

僅針對簡單屬性集，設定基礎儲存體所支援的時間。 複合檔案儲存體的執行支援全部三種：修改、存取和建立。 這項 [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) 的執行會呼叫基礎儲存體的 [**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) 方法，以取得這些時間。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 