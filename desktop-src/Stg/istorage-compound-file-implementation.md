---
title: IStorage-Compound 檔案的執行
description: IStorage 的複合檔案執行可讓您建立和管理位於複合檔案物件中之儲存物件內的 substorages 和資料流程。
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992409"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound 檔案的執行

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的複合檔案執行可讓您建立和管理位於複合檔案物件中之儲存物件內的 substorages 和資料流程。 若要建立複合檔案物件並取得 **IStorage** 指標，請呼叫 API 函數 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)。 若要開啟現有的複合檔案物件並取得其根 **IStorage** 指標，請呼叫 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)。

使用複合儲存的應用程式應該在 HKEY \_ 類別 \_ 根 SystemFileAssociations 中註冊 \\ ，而且應該提供自己的屬性處理常式。 如需詳細資訊，請參閱 [應用程式註冊](/windows/desktop/shell/app-registration)的「註冊動詞和其他檔案關聯資訊」一節。

## <a name="when-to-use"></a>使用時機

大部分的應用程式都會使用此實作為來建立和管理儲存體和串流。

## <a name="methods"></a>方法

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

使用這個儲存物件中包含的指定名稱，建立並開啟資料流程物件。 名稱長度不得超過31個字元 (不包括字串結束字元) 。 000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。 這是複合檔案限制，而非結構化儲存體限制。 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法的 COM 提供的複合檔案執行不支援下列行為：

-   \_不支援 STGM DELETEONRELEASE 旗標。
-   \_資料流程物件不支援交易模式 (STGM 交易) 。
-   不支援從相同的儲存體多次開啟相同的資料流程。 \_ \_ *GrfMode* 參數中必須指定 STGM 共用獨佔共用模式旗標。

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

使用 *grfMode* 參數中指定的存取模式，在此儲存物件內開啟現有的資料流程物件。 000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。 這是複合檔案限制，而非結構化儲存體限制。 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)方法的 COM 提供的複合檔案執行不支援下列行為：

-   STGM \_ DELETEONRELEASE 旗標。
-   交易模式 (\_ 資料流程物件的交易式) STGM。
-   從相同的儲存體多次開啟相同的資料流程。 \_ \_ 必須指定 STGM 共用專屬旗標。

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

使用指定的存取模式，以指定的名稱建立並開啟新的儲存物件。 名稱長度不得超過31個字元 (不包括字串結束字元) 。 000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。 這是複合檔案限制，而非結構化儲存體限制。 [**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)方法的 COM 提供的複合檔案執行不支援下列行為：

-   \_非根儲存體的 STGM 優先權旗標。
-   從相同的父儲存體多次開啟相同的儲存物件。 \_ \_ 必須指定 STGM 共用專屬旗標。
-   STGM \_ DELETEONRELEASE 旗標。 如果指定此旗標，函數會傳回 STG. \_ E \_ INVALIDFLAG。

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

在指定的存取模式中，以指定的名稱開啟現有的儲存物件。 000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。 這是複合檔案限制，而非結構化儲存體限制。 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)方法的 COM 提供的複合檔案執行不支援下列行為：

-   \_非根儲存體的 STGM 優先權旗標。
-   從相同的父儲存體多次開啟相同的儲存物件。 \_ \_ 必須指定 STGM 共用專屬旗標。
-   STGM \_ DELETEONRELEASE 旗標。 如果指定此旗標，函數會傳回 STG. \_ E \_ INVALIDFUNCTION。

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

只將這個開啟的儲存物件的 substorages 和資料流程複製到另一個儲存物件。 *RgiidExclude* 參數可以設定為 iid \_ IStream 以只複製 substorages，或設定為僅複製 \_ 資料流程的 iid IStorage。

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage：： MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

將 substorage 或串流從此儲存物件複製或移動到另一個儲存物件。

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

確保對儲存物件所做的任何變更會在交易模式中開啟，並反映在父儲存體中;針對根儲存體，反映實際裝置中的變更;例如，磁片上的檔案。 若是以直接模式開啟的根儲存物件，除了將所有記憶體緩衝區排清到磁片之外，此方法不會有任何作用。 若是直接模式中的非根儲存物件，這個方法沒有任何作用。

除非 \_ *grfCommitFlags* 參數中指定了 STGC 覆寫，否則 COM 提供的複合檔案執行會使用兩個階段的認可進程。 這兩個階段的程式可確保資料的穩定性，以防認可作業失敗。 首先，所有新資料都會寫入基礎檔案中未使用的空間。 必要時，會設定檔案的新空間。 完成此步驟之後，檔案中的資料表會使用單一磁區寫入作業進行更新，以指出要使用新資料來取代舊的資料。 舊資料會變成可用空間，以便在下一次認可作業時使用。 因此，如果在認可變更時發生錯誤，就可以使用舊的資料，而且可以還原。 如果 \_ 指定了 STGC 覆寫，則會使用單一階段認可作業。 如需交易模式旗標的詳細資訊，請參閱 [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) 列舉。

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

捨棄自從上次認可作業之後對儲存物件所做的所有變更。

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage：： EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

建立並抓取列舉值物件的指標，該物件可用來列舉此儲存物件內所包含的儲存和資料流程物件。 COM 提供的複合檔案執行會取得該資訊的快照。 因此，在取得新的列舉值之前，對資料流程和儲存體的變更都不會反映在枚舉器中。

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage：:D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

從這個儲存物件 (substorage 或 stream) 移除指定的元素。

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage：： RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

重新命名這個儲存物件中指定的 substorage 或資料流程。 000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。 這是複合檔案限制，而非結構化儲存體限制。

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

設定指定之儲存元素的修改、存取和建立時間。 COM 提供的複合檔案執行會維護內部儲存物件的修改和變更時間。 根儲存物件支援基礎檔案系統 (或 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)) 所支援的任何內容。 複合檔案執行不會維護任何內部資料流程的時間戳記。 不支援的時間戳記會回報為零，讓呼叫端能夠測試支援。

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage：： SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

將指定的 CLSID 指派給這個儲存物件。

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage：： SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

在此儲存物件中儲存最多32位的狀態資訊。 這個方法所設定的狀態僅供外部使用。 COM 提供的複合檔案執行不會根據狀態執行任何動作。

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

抓取這個開啟的儲存物件的 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

如果以簡單模式開啟儲存物件，則會限制上述方法的使用方式。 如果以 \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函式的 *grfMode* 參數中指定的 STGM simple 元素開啟，則儲存體會處於簡單模式。 如需簡單模式儲存體的詳細資訊，請參閱 [**STGM 常數**](stgm-constants.md)。 如果已從 **StgCreateStorageEx** 函式取得簡單模式的儲存物件，則可以呼叫 [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 方法，但 [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 方法無法進行呼叫。 如果已從 **StgOpenStorageEx** 函式取得簡單模式儲存物件，則可以呼叫 **OpenStream** 方法，但 **CreateStream** 方法無法進行呼叫。

當使用簡單模式儲存物件來建立資料流程時，該資料流程的大小下限通常為4096個位元組。 如果將較少的資料寫入資料流程，則大小會四捨五入為4096個位元組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案執行限制](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 