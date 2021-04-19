---
title: 結構化儲存介面
description: 結構化儲存體服務分成三種類型的介面。
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- 結構化儲存介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0010a0d4dec4908111c8a5bb939f795f0a2b2eb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996562"
---
# <a name="structured-storage-interfaces"></a>結構化儲存介面

結構化儲存體服務分成三種類型的 [介面](interfaces.md)。 每個集合都代表複合檔案、它所包含的物件和儲存這些個別元件之實體媒體之間的連續間接取值層級或抽象層。

介面的第一個類別是由 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)和 [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)所組成。 前兩個介面會定義如何將物件儲存在複合檔案中。 這些介面提供開啟儲存元素、認可和還原變更、複製和移動元素，以及讀取和寫入資料流程的方法。 這些介面無法辨識個別物件的原生資料格式，因此沒有方法可將這些物件儲存至持續性儲存區。 **IRootStorage** 介面具有單一方法，可讓複合檔案與基礎檔案系統名稱產生關聯。 用戶端必須為其複合檔案執行這些介面。

第二個類別的介面是由 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) 介面所組成，這些介面的物件會執行這些介面來管理其持續性資料。 這些介面會提供方法來讀取個別物件的資料格式，進而知道如何儲存它們。 物件會負責執行這些介面，因為用戶端不知道其嵌套物件的原生資料格式。 不過，這些介面並不知道特定的實體儲存體媒體。

第三個類別是由單一介面 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)所組成，它提供將檔案寫入特定實體媒體（例如硬碟或磁帶機）的方法。 不過，大部分的應用程式都不會實 **ILockBytes** 介面，因為 COM 已經提供兩種最常見的情況，也就是以檔案為基礎的執行和以記憶體為基礎的實作為。 複合檔案儲存物件會呼叫 **ILockBytes** 方法，您不會直接在執行中呼叫它們。

## <a name="compound-file-implementation-limits"></a>複合檔案執行限制

結構化儲存體架構的 COM 實作為所謂的 *複合檔案*。 在複合檔案中執行的儲存物件包含 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行。

藉由呼叫 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 函式來建立新的複合檔案物件，或使用 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 來開啟先前建立的複合檔案，即可取得這些介面的複合檔案實指標。

取得這些介面之複合檔案執行指標的替代方法是呼叫較舊且更有限的 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 或 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) 函式。 這四個函式會被視為複合檔案執行。

複合檔案執行可以設定為使用512或4096位元組的磁區，如 [**STGOPTIONS**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) 結構中所定義。

複合檔案的複合檔案執行受限於下列實條件約束。



| 限制                                           | 複合檔案                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 檔案大小限制：                               | 512： 2 gb (GB) 4096：最高達檔案系統限制<br/>                                                                                                                    |
| 開啟元素所需的堆積大小上限：   | 512： 4 mb (MB) 4096：最多虛擬記憶體限制<br/>                                                                                                                 |
| 並行根目錄會開啟 (開啟相同檔案) ： | 如果 \_ 指定 STGM READ 和 STGM \_ SHARE \_ DENY \_ WRITE，則限制是由檔案系統限制所決定。 否則，相同檔案的限制為20個並行的根目錄開啟。 |
| 檔案中的元素數目：                   | 512：無限制，但如果上千4096：無限制的元素數，效能可能會降低<br/>                                                                         |



 

由於 4 MB 堆積大小的限制，交易模式中開啟的元素數目通常僅限於數千個元素。

 

