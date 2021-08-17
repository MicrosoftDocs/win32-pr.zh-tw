---
title: IPropertySetStorage-Compound 檔案的執行
description: COM 複合檔案儲存體物件的執行包含兩個 IPropertyStorage 的實部：管理單一持續性屬性集的介面，以及管理持續性屬性集群組的介面 IPropertySetStorage。
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd Stg.、執行、複合檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662658"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound 檔案的執行

[COM 複合檔案儲存體物件的執行](ipropertystorage-compound-file-implementation.md)包含兩個 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的實部：管理單一持續性屬性集的介面，以及管理持續性屬性集群組的介面 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)。

若要取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案執行指標，請將識別碼 IID IStorage 的標頭定義名稱指定 \_ 為 *riid* 參數，或使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函數。 在這兩種情況下，請 \_ 將 STGFMT 儲存體指定為 *STGFMT* 參數。  (STGFMT \_ ，也可以在 **StgOpenStorageEx** 的情況下指定任何。 ) 此外，也請將介面識別碼 (iid) iid IPropertySetStorage 的標頭定義名稱指定 \_ 為 *riid* 參數。 這兩個函數都會提供物件 **IPropertySetStorage** 介面的指標。

另一種取得複合檔案執行指標的方式，就是將識別碼 IID IStorage 的標頭定義名稱指定 \_ 為 *riid* 參數，或使用 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 或 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) 函數。 這會提供物件 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的指標。 當您想要處理持續性屬性集時，請呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面的 [**IStorage：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

## <a name="when-to-use-ipropertysetstorage"></a>使用 IPropertySetStorage 的時機

呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的方法，以建立、開啟或刪除目前複合檔案屬性集儲存區中的屬性集。 另外還有一個方法 [**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)，它會提供列舉值的指標，可用來列舉儲存區中的屬性集。

## <a name="methods"></a>方法

[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

在目前的複合檔案儲存體中建立新的屬性集，並在傳回時提供介面指標給 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的複合檔案執行。 在這個執行中，只有在指定 PROPSETFLAG 簡單時，才可以交易屬性集 \_ 。 這個方法要求 *grfMode* 參數中指定的共用模式必須是 STGM \_ 共用 \_ 專屬，而且存取模式是 STGM \_ READ 或 STGM \_ READWRITE (STGM \_ 寫入模式不支援) 。

[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

開啟目前屬性儲存區中的現有屬性集。 傳回時，它會提供 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的複合檔案執行介面指標。 這個方法需要在 *grfMode* 參數中指定的共用模式必須是 STGM \_ 共用 \_ 專屬的，而且存取模式是 STGM \_ READ 或 STGM \_ READWRITE (STGM \_ WRITE 不支援) 。

[**IPropertySetStorage：:D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

刪除這個屬性儲存體中設定的屬性。

[**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

建立用來列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的物件。 每個 **STATPROPSETSTG** 結構都會提供單一屬性集的相關資料。

## <a name="remarks"></a>備註

從 Windows 2000 開始， [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案執行支援簡單模式。 藉由為 \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 和 [**STGOPENSTORAGEEX**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函式指定 STGM simple 旗標，即可指出簡單模式。 如果複合檔案是在簡單模式中開啟，則相關聯的 **IPropertySetStorage** 執行會受到限制，如下所示：

-   只能建立簡單的屬性集。 也就是說， \_ 在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)方法的 *GRFFLAGS* 參數中指定 PROPSETFLAG 簡單值會導致錯誤。
-   使用 STGM SIMPLE 和 query for IPropertySetStorage 介面建立具有 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)的複合檔案之後 \_ ，您只能呼叫 [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) [**IPropertySetStorage：： create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)一次。 然後，您必須先釋放 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面，再呼叫 **Create** 方法。 如需簡單模式的詳細資訊，請參閱 [**STGM 常數**](stgm-constants.md)。
-   使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)建立儲存物件之後，就無法使用 [**IPropertySetStorage：： open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法來開啟屬性集。 相反地，您必須先使用 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ，然後再查詢 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和呼叫 **Open** 方法。
-   當您使用 STGM SIMPLE 旗標並查詢 IPropertySetStorage 介面開啟具有 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)的複合檔案之後 \_ ，您可以使用 [**IPropertySetStorage：： open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)，一次開啟一個屬性集。 [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 此外，當屬性集開啟時，屬性集的總大小可能不會增加。

無法交易簡單的屬性集。 \_除非您同時在 [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) \_ *grfFlags* 參數中指定 PROPSETFLAG 簡單，否則無法在 Create 和 Open 方法的 grfmode 參數中指定 STGM 交易。 請注意，簡單且非簡單的屬性集與上述的簡單模式屬性集無關。 如需簡單和簡單屬性集的詳細資訊，請參閱[儲存體和資料流程物件以取得屬性集](storage-vs--stream-for-a-property-set.md)。

> [!Note]  
> DocumentSummaryInformation 和使用者配置的屬性集會是唯一的，因為它們可能會有兩個屬性集區段。 如需詳細資訊，請參閱 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPropertyStorage-複合檔案執行](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage：： EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**PROPSETFLAG 常數**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 