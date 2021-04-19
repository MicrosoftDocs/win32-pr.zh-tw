---
title: IPropertySetStorage-NTFS 檔案系統執行
description: 當檔案本身不是複合檔案時，NTFS 5.0 版可針對 NTFS 磁片區上的檔案提供 IPropertySetStorage 的執行。
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd Stg.、、NTFS 檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999589"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-NTFS 檔案系統執行

當檔案本身不是複合檔案時，NTFS 5.0 版可針對 NTFS 磁片區上的檔案提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的執行。 NTFS 執行相當於 [複合檔案執行](ipropertysetstorage-compound-file-implementation.md)。 如需例外狀況的詳細資訊，請參閱備註。

**若要取得 IPropertySetStorage NTFS 執行的指標**

1.  呼叫 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)並在 *grfFlags* 參數中指定 STGFMT 檔案，以建立新的檔案。 **\_**
2.  呼叫 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)並指定 STGFMT 檔案 **， \_** 或 STGFMT *grfFlags* 參數中的 **\_ 任何** 列舉值，以開啟現有的檔案。

不過，您無法為複合檔案取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的 NTFS 實作為。 使用 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)開啟複合檔案時，指定 STGFMT 檔 **\_** 列舉值會導致錯誤。

此外，也無法交易簡單的屬性集。 也就是說，您無法在 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)和 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法的 *grfmode* 參數中指定 **STGM \_ 交易**，除非您同時在 *grfFlags* 參數中指定 **PROPSETFLAG \_ 簡單**。 屬性集的儲存物件本身不支援交易處理。

## <a name="when-to-use"></a>使用時機

呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 方法，以建立、開啟或刪除目前 NTFS 屬性集儲存區中的屬性集。 另外還有一個方法 [**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)，它會提供列舉值的指標，可用來列舉儲存區中的屬性集。

## <a name="compatibility"></a>相容性

從 Windows 2000 開始，可以使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的 NTFS 實作為。 舊版無法存取這些屬性集。

NTFS 執行會將屬性集儲存在 NTFS 檔案的替代資料流程中。 複製主要檔案時，必須複製替代資料流程。

> [!Caution]  
> 並非所有檔案系統都支援這類串流。 如果將含有屬性集的 NTFS 檔案複製到 FAT 磁片區，則只會複製檔案中的資料;屬性集遺失。 在此情況下， [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) 函數不會傳回錯誤。

 

> [!Caution]  
> 如果執行檔案複製的電腦不是在 Windows 2000 或更新版本上執行的電腦，屬性集可能會遺失。 例如，如果在 Windows 95 作業系統上執行的電腦複製了 NTFS 檔案，即使目的地檔案也在 NTFS 磁片區上，也會遺失屬性集。

 

## <a name="methods"></a>方法

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 檔案系統執行支援下列方法。

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

在目前的 NTFS 檔案儲存體中建立新的屬性集，並在傳回時提供介面指標給 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS 檔案執行。 *Grfmode* 參數中指定的共用模式必須是 **STGM \_ 共用 \_ 專屬** 的。

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

開啟目前屬性儲存區中的現有屬性集。 傳回時，它會提供介面指標給 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的 NTFS 檔案執行。 *Grfmode* 參數中指定的共用模式必須是 **STGM \_ 共用 \_ 專屬** 的。

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage：:D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

刪除目前屬性儲存區中的屬性集。

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

建立用來列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的物件。 每個 **STATPROPSETSTG** 結構都會提供單一屬性集的相關資料。

</dd> </dl>

## <a name="remarks"></a>備註

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的 NTFS 實作為檔案中的存放區屬性集，而不會影響該檔案的內容。 例如，如果您在名為 Default.htm 的 HTML 檔案中建立屬性集，該檔案仍然會在網頁瀏覽器中正確顯示。 也就是說，使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數存取檔案時，會無法偵測使用這兩個介面的檔案變更。

當使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 將屬性集寫入 ntfs 版本5.0 磁片區上的檔案時，ntfs 會提供安全的執行。 即使發生系統失敗，這些屬性集也無法由實作為損毀。 例如，如果在將屬性集排清至磁片的情況下呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 時發生系統的電源失敗，屬性集永遠不會保持在中繼狀態。 先前的屬性集版本會保留或儲存所有更新。

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 實與複合檔案執行的方式不同，如下所示：

-   從 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面取得的 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)結構包含 **clsid** 成員，其值一律為零 (**clsid \_ Null**) 。 使用複合檔案執行時，會針對非簡單 (傳回正確的 **clsid** 成員，請參閱屬性集) 屬性集的 [儲存和資料流程物件](storage-vs--stream-for-a-property-set.md) 。
-   使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函數取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面指標的 NTFS 實作為時， *grfmode* 參數必須遵循與複合檔案執行相同的規則。

    此外，可能不會使用下列旗標：

    **STGM \_SIMPLE**、 **STGM \_ 交易**、 **STGM \_ CONVERT**、 **STGM \_ PRIORITY** 和 **STGM \_ DELETEONRELEASE**。

-   當 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**STGOPENSTORAGEEX**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函數取得 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面時，共用模式主要會套用至該介面的其他實例，而不會套用至開啟檔案本身的實例。 例如，如果透過呼叫 **StgOpenStorageEx** 函式來開啟 NTFS **IPropertySetStorage** 介面，並將 *grfmode* 參數設定為 **STGM \_ READWRITE \| STGM \_ 共用 \_ 獨佔**，則可以使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函數來開啟檔案。

    開啟此介面的這類並行實例受限於下列條件約束： [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式中的 *dwShareMode* 參數必須指定檔案 **\_ 共用 \_ 讀取** 旗標，且 *dwAccess* 參數不得指定 **刪除** 旗標。 此外，您不能在這些屬性集介面開啟的檔案上呼叫 [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) 和 [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) 函式，因為這些函式需要 **刪除** 檔案的存取權。

-   如果 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 方法是以唯讀方式開啟，而且檔案目前沒有任何屬性集，則傳回的物件將不會實際保存開啟的檔案。 因此，即使原始開啟作業的共用模式會拒絕它，該檔案的其他開頭也會成功。

    範例如果 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 是以 **STGM \_ READ \| STGM \_ SHARE \_ 專有** 的模式開啟，而且檔案沒有屬性集，就可以同時開啟檔案 **STGM \_ READWRITE \| STGM \_ 共用 \_ 獨佔**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPropertyStorage-NTFS 檔案系統執行](ipropertystorage-ntfs-file-system-implementation.md)
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

 

 