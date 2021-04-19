---
title: 屬性儲存體考慮
description: IPropertyStorage ReadMultiple 會讀取 rgpspec 陣列中所指定的多個屬性，如同在屬性集中找到的屬性。
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad6aabf8b22a7c01f91a090136e6cc8156c791
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967899"
---
# <a name="property-storage-considerations"></a>屬性儲存體考慮

[**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 會讀取 *rgpspec* 陣列中所指定的多個屬性，如同在屬性集中找到的屬性。 只要讀取要求的任何屬性，取得不存在之屬性的要求就不會是錯誤。 相反地，這必須在傳回時，將 \_ 該屬性的 VT 空白寫入 *rgvar* \[ \] 陣列。 當沒有任何要求的屬性存在時，此方法應該會傳回 \_ FALSE，並 \_ 在每個 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)中設定 VT 空白。 如果傳回任何其他錯誤，則不會抓取任何屬性值，而且呼叫端不需要擔心釋放它們。

*Rgpspec* 參數是 [**PROPSPEC**](/windows/win32/api/propidlbase/ns-propidlbase-propspec)結構的陣列，可指定每個屬性的屬性識別碼，或指派給一個字串識別碼的屬性。 您可以藉由呼叫 [**IPropertyStorage：： WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)，將字串對應至屬性識別碼。 不過，使用屬性識別碼可能會比使用字串更有效率。

字串名稱 (PRSPEC LPWSTR) 所要求的屬性 \_ 會對應至屬性識別碼 (識別碼) ，因為它們是在目前的屬性集 (中指定，而且根據目前的系統地區設定) 。

當屬性型別為 VT \_ LPSTR，而且從 ANSI 屬性集讀取屬性時（亦即，屬性集的字碼頁設定為 Unicode 以外的值），屬性的值會使用與屬性集相同的字碼頁。 \_從 Unicode 屬性集讀取 VT LPSTR 屬性時，屬性值會使用系統目前的預設 ANSI 字碼頁，也就是從 **GetACP** 函數傳回的字碼頁。

除了做為資料流程和儲存體指標的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)以外，它也稱為簡單 **PROPVARIANT**。 這些簡單的 **PROPVARIANT** 會以傳值方式接收資料，因此呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 會提供呼叫端所擁有的資料複本。 若要建立或更新這些屬性，請呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)。

相反地，variant 型別會將 VT \_ 資料流程、vt 資料流程 \_ \_ 物件、VT \_ 儲存和 vt \_ 儲存 \_ 的物件視為非簡單的屬性，因為這種方法不會提供值，而是會抓取指向介面的指標，然後從該介面讀取資料。 這些類型允許透過單一屬性儲存大量資訊。 使用簡單屬性時，會發生數個問題。

若要建立這些屬性，請呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)，做為其他屬性。 不過，您可以更有效率地先呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 來取得資料流程或儲存體的介面指標，然後使用 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 或 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 方法來寫入資料，而不是呼叫相同的方法進行更新。 透過屬性開啟的資料流程或儲存體一律會以直接模式開啟，因此不會引進額外的嵌套交易層級。 但是，根據 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的開啟或建立方式而定，可能仍會在屬性上設定為整體的交易。 此外，當屬性集開啟或建立時，指定的存取和共用模式標記會傳遞給以屬性為基礎的資料流程或儲存體。

以屬性為基礎的資料流程或儲存體指標的存留期，雖然理論上與其相關聯的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 指標無關，但實際上卻依賴它們。 透過資料流程或儲存體可見的資料，與從中抓取的屬性儲存體物件上的交易有關，就如同儲存物件 (使用包含的資料流程和儲存子物件支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) 。 如果父物件的交易中止，則無法再存取該物件的現有 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 和 **IStorage** 指標。 因為 **IPropertyStorage** 是屬性儲存物件上的唯一介面，所以包含的 **IStream** 和 **IStorage** 指標的有用存留期是由 **IPropertyStorage** 介面的存留期所限制。

執行也必須處理相同的資料流程或儲存體值屬性透過相同的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面實例多次要求的情況。 例如，在 COM 複合檔案執行中，開啟會成功或失敗，取決於屬性是否已開啟。

另一個問題是交易模式中有多重開啟。 結果取決於透過呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 方法所指定的隔離等級， ([**開啟**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 或 [**建立**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 方法，方法是透過 STGM 旗標在開啟屬性儲存時) 。

如果開啟屬性集的呼叫指定讀寫存取， [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)值屬性一律會以讀寫存取來開啟。 然後可以透過這些介面寫入資料，變更屬性的值，這是更新這些屬性最有效率的方式。 屬性值本身沒有額外的交易嵌套層級，因此，如果屬性儲存物件上有任何) ，則變更會限定在交易 (。

## <a name="storage-and-stream-properties"></a>儲存體和資料流程屬性

若要將資料流程或儲存物件寫入屬性集，屬性集必須建立為簡單。 如需簡單和簡單屬性集的詳細資訊，請參閱標題為「 [儲存」和「資料流程物件」的屬性集](storage-vs--stream-for-a-property-set.md)區段。 下列屬性類型（如 *rgvar* 陣列元素的 *vt* 欄位中所指定）為數據流或儲存類型： vt \_ 資料流程、vt \_ 儲存、vt \_ 資料流程 \_ 物件、vt 儲存的 \_ \_ 物件。

若要以非簡單屬性集中的屬性來寫入資料流程或儲存物件，請呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)。 雖然您也會呼叫這個方法來更新簡單的屬性，但它並不是在屬性集中更新資料流程和儲存物件的有效方式。 這是因為透過呼叫 **WriteMultiple** 來更新其中一個屬性會在屬性儲存物件中建立傳入資料的複本，而 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 指標不會在此呼叫的持續時間內保留。 通常會先呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 來取得資料流程或儲存體的介面指標，然後透過 **IStream** 或 **IStorage** 方法寫入資料，以更有效率的方式直接更新資料流程或儲存物件。

例如，您可以呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 來寫入 **Null** 資料流程或儲存物件。 然後，此實作為會在屬性集中建立空的物件。 然後，您可以藉由呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)來取得此物件的存取權。 當您完成更新這個物件時，您不需要將它寫入屬性集，因為您的更新會直接進入屬性集。

透過屬性開啟的資料流程或儲存體一律會以直接模式開啟，因此不會引進額外的嵌套交易層級。 屬性（property）上的屬性（property）仍可能會設定為整體的交易。 (For example, if the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) was obtained by calling [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) with the STGM\_TRANSACTED flag set in the *grfmode* parameter.) Further, a property-based stream or storage is opened in read-write mode, if possible, given the mode on the property set; otherwise, read mode is used.

如先前所述，當資料流程或儲存物件寫入具有 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 方法的屬性集時，會建立物件的複本。 當資料流程物件上進行這類複製時，複製作業會從來源的目前搜尋位置開始。 失敗時，搜尋位置未定義，但在成功時，是在資料流程的結尾;搜尋指標不會還原至其原始位置。

如果已從具有 [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)的屬性集讀取資料流程或儲存屬性，仍會保持開啟狀態，而且會針對相同的屬性進行後續的 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 呼叫， **WriteMultiple** 作業將會成功。 先前開啟的資料流程或儲存體屬性會處於還原狀態， (對它的所有呼叫都會傳回 STG. \_ E 已 \_ 還原的錯誤) 。

如果 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 方法在寫入屬性的陣列時傳回錯誤，或甚至是個別的非簡單屬性，則實際寫入的資料量是未定義的。

## <a name="reference-properties"></a>參考屬性

如果指定的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構 \_ 在其 **VT** 成員中包含 vt BYREF 旗標，則相關聯的屬性會是參考屬性。 在將值寫入屬性集之前，會自動取值參考屬性。 例如，如果 **PROPVARIANT** 結構的 **vt** 成員指定了型別 vt \_ BYREF vt I4 的值 \| \_ ，則實際寫入的值是 vt \_ I4 型別。 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)方法的後續呼叫會以 VT I4 的形式傳回值 \_ 。 使用參考屬性類似于呼叫 [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) 函數。 如果將來源指定為 VT BYREF， [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind)就會釋出目的地變異，並複製來源 VARIANTARG，執行必要的間接取值 \_ 。 當需要變異的複本，並確保它不是 VT \_ BYREF 時（例如，在處理 [**IDispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)的函式中處理引數）時，這個函式會很有用。

## <a name="notes-to-callers"></a>給呼叫者的注意事項

建議您 \_ 在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *GRFFLAGS* 參數中設定 PROPSETFLAG ANSI 旗標，以將屬性集建立為 Unicode。 此外，也建議您避免使用 VT \_ LPSTR 值，並改為使用 vt \_ LPWSTR 值。 當屬性集字碼頁是 Unicode 時，VT \_ LPSTR 字串值會在儲存時轉換成 unicode，並在抓取時轉換回多位元組字元串值。 當屬性集的字碼頁不是 Unicode 時，屬性名稱、VT \_ BSTR 字串和非簡單的屬性值會在儲存時轉換成多位元組字元串，並且在抓取時轉換回 Unicode，全都使用目前的系統 ANSI 字碼頁。

## <a name="notes-to-implementers"></a>給實施者的注意事項

配置屬性識別碼時，實作為屬性識別碼的屬性（property）識別碼（property）的屬性（property）（property）不會在屬性（property）識別碼中使用任何目前使用中的值，只要它不是0或1或大於0x80000000 （這些都是保留值）。 *PropidNameFirst* 參數會在集合內建立屬性識別碼的最小值，而且必須大於1且小於0x80000000。 請參閱上述的備註一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPropertyStorage-複合檔案執行](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage-NTFS 檔案系統執行](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[IPropertyStorage-獨立執行](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 