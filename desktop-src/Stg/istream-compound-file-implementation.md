---
title: IStream 複合檔案執行
description: IStream 介面支援對資料流程物件讀取和寫入資料。 在結構化儲存物件中，資料流程物件包含資料和儲存體提供結構。
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106974743"
---
# <a name="istream---compound-file-implementation"></a>IStream 複合檔案執行

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)介面支援對資料流程物件讀取和寫入資料。 在結構化儲存物件中，資料流程物件包含資料和儲存體提供結構。 簡單的資料可以直接寫入資料流程，但更頻繁的是，資料流程是在儲存物件中嵌套的元素。 它們類似于標準檔案。

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的規格定義了比 COM 執行所支援的功能更多的功能。 例如， **IStream** 介面會定義最多2個⁶⁴位元組的資料流程，而其長度需要64位的 seek 指標。 不過，COM 執行只支援最多2個³²位元組的資料流程， (4 GB) ，而且讀取和寫入作業一次一律會限制為2個³²位元組。 COM 執行也不支援資料流程 transactioning 或區域鎖定。

若要根據全域記憶體建立簡單的資料流程，請呼叫 API 函數 [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)來取得 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)指標。 若要取得複合檔案物件內的 **IStream** 指標，請呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 或 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)。 這些函式會 [**取出 IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)指標，您接著可以針對 **IStream** 指標呼叫 [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)或 [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 。 在任一種情況下，都會使用相同的 **IStream** 執行程式碼。

> [!Note]  
> 結構化儲存區的複合檔案執行不會在 [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法上成功，但它包含透過 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)介面指標的 [**讀取**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)和 [**寫入**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)方法。

 

## <a name="when-to-use"></a>使用時機

呼叫 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 的方法以讀取資料，並將資料寫入資料流程。

由於資料流程物件可以封送處理至其他進程，因此應用程式可以共用儲存物件中的資料，而不需要使用全域記憶體。 在資料流程物件的 COM 複合檔案執行中，當兩個進程具有共用記憶體存取權時，COM 中的自訂封送處理功能會在新的進程中建立原始物件的遠端版本。 因此，遠端版本不需要與原始進程通訊來執行其功能。

資料流程物件的遠端版本與原始資料流程共用相同的 seek 指標。 如果您不想要共用搜尋指標，請使用 [**IStream：： Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) 方法為遠端進程提供資料流程物件的複本。

> [!Note]
> 如果您在電腦的記憶體中建立大於堆積的資料流程物件，並使用全域記憶體物件的 **HGLOBAL** 控制碼，資料流程物件就會在內部呼叫 [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) 方法當它需要更多的記憶體。 由於 **GlobalRealloc** 一律會將資料從來源複製到目的地，因此將資料流程物件從 20 mb 增加至 25 mb 會需要很長的時間。 這是因為複製的增量大小，如果電腦上的記憶體少於 45 MB，而且因為磁片交換，則會惡化。
>
> 慣用的解決方法是使用 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) （而非 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)）所配置的記憶體，來執行 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)方法。 這可以保留大量的虛擬位址空間，然後視需要在該位址空間內認可記憶體。 不會進行資料複製，而且只有在需要時才會認可記憶體。
>
> [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)的替代方法是在資料流程物件上呼叫 [**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)方法，以預先增加記憶體配置。 不過，這並不是像使用 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)一樣有效率，如上面所述。

 

## <a name="methods"></a>方法

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream：： Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

從資料流物件中將指定的位元組數目讀入記憶體中目前搜尋指標開始處。 \_如果在讀取期間到達資料流程的結尾，則此實作為「確定」。  (這與在 MS-DOS FAT 檔案系統中找到的「檔案結尾」行為相同。 ) 

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream：： Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

從目前的 seek 指標開始，將指定的數位從位元組寫入資料流程物件。 在這個執行中，資料流程物件不是稀疏的。 任何填滿的位元組最後都會配置在磁片上，並指派給串流。

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream：： Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

將搜尋指標變更為相對於資料流開頭、資料流結尾或目前搜尋指標的新位置。

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

變更資料流物件的大小。 在這種情況下，並不保證配置的空間將會是連續的。

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

從資料流中目前的搜尋指標將指定的位元組數目複製到另一個資料流中目前的搜尋指標。

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行僅支援在直接模式下開啟資料流程，而不支援交易模式。 因此，除了將所有記憶體緩衝區排清至下一個儲存層級以外，方法不會有任何作用。

在這種情況下，如果您將變更認可至資料流程，就不需要認可儲存物件的變更。

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

此執行不支援交易資料流程，因此呼叫這個方法不會有任何作用。

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

此執行不支援範圍鎖定，因此呼叫這個方法不會有任何作用。

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream：： UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

移除先前以 [**IStream：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)限制之位元組範圍的存取限制。

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

抓取此資料流程的 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) 結構

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream：： Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

建立新的資料流物件，其搜尋指標會參考與原始資料流相同的位元組。

</dd> </dl>

簡單模式的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 受限於下列條件約束。

-   如果資料流程是在簡單模式的儲存體中建立或開啟，則為簡單模式。 如果使用 \_ *grfMode* 參數中所設定的 STGM simple 旗標來建立或開啟儲存體，則儲存體是簡單模式。
-   不支援 [**複製**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) 和 [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) 方法。
-   支援 [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法，但 \_ 必須指定 STATFLAG NONAME 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 