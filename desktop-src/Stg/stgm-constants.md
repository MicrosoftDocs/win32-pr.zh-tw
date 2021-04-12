---
title: 'STGM 常數 (ObjBase) '
description: 旗標，表示用來建立和刪除物件之物件和存取模式的條件。
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464484"
---
# <a name="stgm-constants"></a>STGM 常數

STGM 常數是旗標，表示用來建立和刪除物件之物件和存取模式的條件。 STGM 常數包含在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面，以及 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)、 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)、 [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)、 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)和 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函數中。

這些元素通常會使用 **OR** 運算子來合併。 它們會在下表所列的群組中加以解讀。 從單一群組使用一個以上的元素是不正確。

建立物件時，請使用建立群組中的旗標，例如使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 或 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)。

如需 transactioning 的詳細資訊，請參閱「備註」一節。



| Group                      | 旗標                         | 值       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM \_ 讀取**               | 0x00000000L |
|                            | **STGM \_ 寫入**              | 0x00000001L |
|                            | **STGM \_ READWRITE**          | 0x00000002L |
| 共用                    | **STGM \_ 共用 \_ 拒絕 \_ 無**  | 0x00000040L |
|                            | **STGM \_ 共用 \_ 拒絕 \_ 讀取**  | 0x00000030L |
|                            | **STGM \_ 共用 \_ 拒絕 \_ 寫入** | 0x00000020L |
|                            | **STGM \_ 共用 \_ 專屬**   | 0x00000010L |
|                            | **STGM \_ 優先順序**           | 0x00040000L |
| 建立                   | **STGM \_ 建立**             | 0x00001000L |
|                            | **STGM \_ 轉換**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000L |
| Transactioning             | **STGM \_ DIRECT**             | 0x00000000L |
|                            | **STGM \_ 交易**         | 0x00010000L |
| Transactioning 效能 | **STGM \_ NOSCRATCH**          | 0x00100000L |
|                            | **STGM \_ NOSNAPSHOT**         | 0x00200000L |
| 直接 SWMR 和簡單     | **STGM \_ 簡單**             | 0x08000000L |
|                            | **STGM \_ DIRECT \_ SWMR**       | 0x00400000L |
| 發行時刪除          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ 讀取**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



指出物件是唯讀的，這表示無法進行修改。 例如，如果資料流程物件是以 **STGM \_ READ** 開啟，則可能會呼叫 [**ISequentialStream：： READ**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) 方法，但是 [**ISequentialStream：： Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) 方法可能不會。 同樣地，如果以 **STGM \_ READ** 開啟的儲存物件，則可能會呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 和 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 方法，但是 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 和 [**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) 方法可能不會。


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ 寫入**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



可讓您儲存對物件所做的變更，但不允許存取其資料。 提供的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面實作為不支援這個僅限寫入模式。


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ READWRITE**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



啟用物件資料的存取和修改。 例如，如果資料流程物件是在此模式中建立或開啟，則可以呼叫 [**IStream：： Read**](/windows/desktop/api/Objidl/nn-objidl-istream) 和 **Istream：： Write**。 請注意，這個常數不是 **STGM \_ WRITE** 和 **STGM \_ READ** 專案的簡單二進位 **或** 運算。


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ 共用 \_ 拒絕 \_ 無**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



指定不拒絕讀取或寫入存取的後續物件的開頭。 如果未指定共用群組中的旗標，則會假設為此旗標。


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ 共用 \_ 拒絕 \_ 讀取**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



防止其他人在 **STGM \_ 讀取** 模式下開啟物件。 它通常用於根儲存物件。


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ 共用 \_ 拒絕 \_ 寫入**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



防止其他人針對 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 存取開啟物件。 在交易模式中，共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_** ，可能會大幅提升效能，因為它們不需要快照集。 如需 transactioning 的詳細資訊，請參閱「備註」一節。


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ 共用 \_ 專屬**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



防止其他人後續以任何模式開啟物件。 請注意，此值不是 **STGM \_ 共用 \_ 拒絕 \_ 讀取** 和 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 值的簡單位 **or** 運算。 在交易模式中，共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_** ，可能會大幅提升效能，因為它們不需要快照集。 如需 transactioning 的詳細資訊，請參閱「備註」一節。


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM \_ 優先順序**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



開啟具有最新認可版本之獨佔存取權的儲存體物件。 因此，當您在 [優先權] 模式中開啟物件時，其他使用者無法認可對該物件所做的變更。 您可以取得複製作業的效能優勢，但會防止其他人認可變更。 限制物件在優先順序模式中開啟的時間。 您必須指定 **STGM \_ DIRECT** 和 **STGM \_ READ** with priority 模式，而且您無法指定 **STGM \_ DELETEONRELEASE**。 **STGM \_DELETEONRELEASE** 只有在建立根物件（例如使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)）時才有效。 開啟現有的根物件（例如 with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)）時無效。 建立或開啟子項目（例如使用 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)）時，它也是不正確。


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ 建立**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



表示應該移除現有的儲存物件或資料流程，新的物件才會取代它。 只有在已成功移除現有的物件時，才會建立新的物件。

嘗試建立時，會使用此旗標：

-   磁片上的儲存物件，但該名稱的檔案已經存在。
-   儲存物件內的物件，但是具有指定名稱的物件已經存在。
-   位元組陣列物件，但有一個具有指定名稱的物件存在。

此旗標無法搭配開啟作業使用，例如 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 或 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)。


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ 轉換**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



建立新的物件，同時將現有的資料保留在名為 "內容" 的資料流程中。 在儲存物件或位元組陣列的案例中，不論現有的檔案或位元組陣列目前是否包含分層式儲存物件，舊資料都會格式化為資料流程。 只有在建立根儲存物件時，才能使用此旗標。 它不能用在儲存物件內;例如，在 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)中。 這也不是同時使用此旗標和 **STGM \_ DELETEONRELEASE** 旗標的有效方式。


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



如果具有指定名稱的現有物件存在，就會導致建立作業失敗。 在此情況下，會傳回 **Stg. \_ E \_ FILEALREADYEXISTS** 。 這是預設建立模式;也就是說，如果未指定其他 create 旗標，則會隱含 **STGM \_ FAILIFTHERE** 。


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



表示在直接模式下，儲存體或資料流程專案的每個變更都會在發生時寫入。 如果未指定 **STGM \_ DIRECT** 或 **STGM \_ 交易** ，這就是預設值。


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ 交易**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



表示在交易模式下，只有在呼叫明確認可作業時，才會緩衝處理和寫入變更。 若要忽略變更，請呼叫 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)、 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)或 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面中的 [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)方法。 **IStorage** 的 COM 複合檔案執行不支援交易資料流程，這表示資料流程只能在直接模式中開啟，而且您無法還原這些資料流程的變更，但支援交易儲存體。 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案、獨立和 NTFS 檔案系統執行，同樣不支援交易式的簡單屬性集，因為這些屬性集會儲存在資料流程中。 不過，您可以在 [**grfFlags：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *IPropertySetStorage* 參數中指定 **PROPSETFLAG \_ 簡單** 旗標，以建立簡單屬性集的 transactioning。


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOSCRATCH**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



表示在交易模式下，通常會使用暫時的暫存檔案來儲存修改，直到呼叫 **Commit** 方法為止。 指定 **STGM \_ NOSCRATCH** 可允許使用原始檔案的未使用部分做為工作空間，而不是針對該目的建立新的檔案。 這不會影響原始檔案中的資料，而且在某些情況下可能會導致效能改進。 若未同時指定 **STGM \_ 交易**，也不能指定此旗標，而且此旗標只能用於根目錄開啟。 如需 NoScratch 模式的詳細資訊，請參閱「備註」一節。


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



此旗標會在開啟具有 **STGM \_ 交易** 且沒有 **STGM \_ 共用 \_ 專屬** 或 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 的儲存物件時使用。 在此情況下，指定 **STGM \_ NOSNAPSHOT** 可防止系統提供的執行建立檔案的快照集複本。 相反地，檔案的變更會寫入檔案結尾。 除非在認可期間執行匯總，而且檔案上只有一個目前的寫入器，否則無法回收未使用的空間。 當檔案以無快照模式開啟時，若未指定 **STGM \_ NOSNAPSHOT**，則無法執行另一個開啟的操作。 此旗標只能用於根開啟作業。 如需 NoSnapshot 模式的詳細資訊，請參閱「備註」一節。


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ 簡單**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



在有限但經常使用的情況下，提供更快速的複合檔案執行。 如需詳細資訊，請參閱＜備註＞一節。


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



支援單一寫入器 multireader 檔案作業的直接模式。 如需詳細資訊，請參閱＜備註＞一節。


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



指出當根儲存物件釋放時，會自動終結基礎檔案。 這項功能最適合用來建立暫存檔案。 只有在建立根物件（例如 with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)）時，才能使用此旗標。 開啟根物件（例如 with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)）或建立或開啟子項目（例如 with [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)）時，這是不正確。 同時使用此旗標和 STGM CONVERT 旗標也是不正確 \_ 。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以結合這些旗標，但只能從每個相關旗標群組中選擇一個旗標。 您必須針對所有使用這些常數的函式和方法，指定每個存取和共用群組的一個旗標。 其他群組的旗標是選擇性的。

### <a name="transacted-mode"></a>交易模式

指定 **STGM \_ DIRECT** 旗標時，只能從存取和共用群組指定下列其中一個旗標組合。

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

請注意，直接模式是因為缺少 **STGM \_ 交易** 而隱含的。 亦即，如果未指定 **STGM \_ Direct** 或 **STGM \_ 交易** ，則會假設為 **STGM \_ direct** 。

當指定 **STGM \_ 交易** 旗標時，會在交易模式中建立或開啟物件。 在此模式中，物件的變更將不會保存，直到認可為止。 例如，在呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 方法之前，不會保存交易儲存物件的變更。 如果在呼叫 **Commit** 方法之前 (最終發行) 發行儲存物件，或呼叫 [**IStorage：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) 方法，則這種儲存物件的變更將會遺失。

在交易模式中建立或開啟物件時，實作為必須將原始資料和更新保留給這項資料，如此一來，就可以在必要時還原更新。 這通常是藉由將變更寫入臨時區域，直到認可為止，或建立一個稱為快照集的最新認可資料所執行。

在交易模式中開啟根儲存物件時，可以控制臨時資料和快照集複本的位置和行為，以使用 **STGM \_ NOSCRATCH** 和 **STGM \_ NOSNAPSHOT** 旗標將效能優化。 例如， (從 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函式取得根儲存物件;從 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 方法取得的儲存物件是 substorage 物件。 ) 通常會將暫存資料和快照集儲存在與儲存體不同的暫存檔案中。

這些旗標的影響取決於讀取器和/或存取根儲存體的寫入器數目。

在「單一寫入器」案例中，會開啟交易模式儲存物件以供寫入存取，而不會有檔案的其他存取權。 也就是說，檔案會以 **STGM \_ 交易**、 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 的存取權來開啟，以及共用 **STGM \_ 共用 \_ 獨佔**。 在此情況下，會將儲存物件的變更寫入臨時區域。 當這些變更認可時，它們會複製到原始儲存體。 因此，如果沒有實際對儲存物件進行任何變更，就不會有不必要的資料傳輸。

在「多個寫入器」案例中，會開啟交易儲存物件以供寫入存取，但是在這類 asway 中會共用以允許其他寫入器。 也就是說，儲存物件是使用 **STGM \_ 交易**、 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 讀取** 來開啟。 如果改為指定 **STGM \_ 共用 \_ 拒絕 \_** 的共用，則案例為「多重寫入器、多個讀取器」。 在這些情況下，將會在開啟作業期間進行原始資料的快照集。 因此，即使沒有實際對儲存體進行任何變更，而且也不會同時由另一個寫入器同時開啟，在開啟期間仍需要進行資料傳輸。 如此一來，您可以在 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_ 獨佔** 模式中開啟儲存物件，以取得最佳的開啟時間效能。 如需有關如何在有多個寫入器時認可變更的詳細資訊，請參閱 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)。

在「單一寫入器、多重讀取器」案例中，會開啟交易儲存物件以供寫入存取，但會與讀取器共用。 也就是說， **STGM \_ 交易** 的寫入器會開啟儲存物件、 **STGM \_ READWRITE** 或 **STGM \_ 寫入** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入**。 儲存體是由具有 **STGM \_ 交易** 的讀取器開啟、 **STGM \_ 讀取** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 無**。 在此情況下，寫入器會使用臨時區域來儲存未認可的變更。 如同上述案例，讀取器會在建立資料的快照集複本時，產生開放時間的效能負面影響。

臨時區域通常是暫存檔案，與原始資料分開。 將變更認可至原始檔案時，必須從暫存檔案傳輸資料。 若要避免這種資料傳輸，可能會指定 **STGM \_ NOSCRATCH** 旗標。 當指定這個旗標時，會將部分的儲存目的檔用於臨時區域，而不是個別的暫存檔案。 如此一來，就可以快速地執行認可變更，因為需要進行資料傳輸。 缺點是儲存體檔案可能會變得大於原本的大小，因為它必須成長到足以容納原始資料和臨時區域。 若要合併資料並移除此不必要的區域，請在交易模式中重新開啟根儲存體，但不設定 **STGM \_ NOSCRATCH** 旗標。 然後，使用 **STGC \_ 合併** 旗標集合來呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 。

快照集區域（像是臨時區域）也是暫存檔案，而這也會受到 STGM 旗標的影響。 藉由指定 **STGM \_ NOSNAPSHOT** 旗標，並不會建立個別的暫存快照集檔案。 相反地，即使每個物件有一或多個寫入器，仍不會修改原始資料。 認可變更時，這些變更會新增至檔案，但原始資料會維持不變。 這種模式會提高效率，因為它可避免在開啟作業期間建立快照集的需求，而縮短執行時間。 不過，使用此模式可能會產生非常大的儲存體檔案，因為無法覆寫檔案中的資料。 這對以 NoSnapshot 模式開啟的檔案大小沒有任何限制。

### <a name="direct-single-writer-multiple-reader-mode"></a>直接單一寫入器，Multiple-Reader 模式

如所述，如果該物件是在交易模式中開啟，則可以有一個儲存物件的單一寫入器和多個讀取器。 您也可以藉由指定 **STGM \_ direct \_ SWMR** 旗標，以直接模式達成單一寫入器的 multireader 案例。

在 **STGM \_ DIRECT \_ SWMR** 模式中，一個呼叫端可以開啟物件以進行讀取/寫入存取，而其他呼叫端同時開啟檔案以供唯讀存取。 搭配 **STGM \_ 交易** 旗標使用此旗標是不正確。 在此模式中，寫入器會開啟具有下列旗標的物件：

**STGM \_DIRECT \_ SWMR** \| **STGM \_ READWRITE** \| **STGM \_ 共用 \_ DENYWRITE**

而且每個讀取器都會使用下列旗標來開啟物件：

**STGM \_DIRECT \_ SWMR** \| **STGM \_ READ** \| **STGM \_ SHARE \_ DENY \_ NONE**

在此模式中，若要修改儲存物件，寫入器必須取得物件的獨佔存取權。 當所有讀取器都已關閉時，就可能發生這種情況。 寫入器會使用 [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) 介面來取得此獨佔存取權。

### <a name="simple-mode"></a>簡單模式

簡單模式 (**STGM \_ 簡單** 的) 適用于執行完整儲存作業的應用程式。 它很有效率，但具有下列限制：

-   Substorages 不存在任何支援。
-   無法封送處理儲存物件和從中取得的資料流程物件。
-   每個資料流程都有最小的大小。 當資料流程釋出時，如果將最小的位元組寫入資料流程，資料流程就會延伸至最小的大小。 例如，特定 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實值的最小大小為 4 KB。 資料流程會建立，並寫入 1 KB。 在該 **IStream** 的最終版本中，資料流程大小會自動延伸至 4 KB。 接著，開啟資料流程並呼叫 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法會顯示 4 KB 的大小。
-   並非所有 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 的方法都將受到實作為支援。 如需詳細資訊，請參閱 [IStorage 複合檔案執行](istorage-compound-file-implementation.md)和 [IStream 複合檔案執行](istream-compound-file-implementation.md)。

[封送處理](/windows/desktop/Midl/marshaling-ole-data-types) 是封裝、解除封裝和傳送介面方法參數的程式，會在遠端程序呼叫內的執行緒或進程界限內， (RPC) 。 如需詳細資訊，請參閱 [封送處理詳細資料](../com/marshaling-details.md) 和 [介面封送處理](../com/interface-marshaling.md)。

使用簡單模式的建立作業取得儲存體物件時：

-   可以建立資料流程元素，但無法開啟。
-   藉由呼叫 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)來建立 stream 元素時，在釋放資料流程物件之前，無法建立另一個資料流程。
-   寫入所有資料流程之後，請呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 以排清變更。

以簡單模式的開啟作業取得儲存體物件時：

-   一次只能開啟一個資料流程元素。
-   您無法藉由呼叫 [**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) 方法，或在資料流程結尾以外搜尋或寫入，來變更資料流程的大小。 不過，因為所有資料流程的大小都是最小值，所以即使原始資料的寫入量較少，也可以將資料流程使用到該大小。 若要判斷資料流程的大小，請使用 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法。

請注意，如果儲存物件是由非簡單模式的儲存物件所修改，則無法再以簡單模式開啟該儲存元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ObjBase。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISequentialStream：： Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

