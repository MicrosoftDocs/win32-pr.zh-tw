---
title: 類別名字標記
description: 雖然類別通常會直接以 Clsid （例如 CoCreateInstance 或 CoGetClassObject）的 Clsid 來識別，但是類別現在也可以使用稱為類別標記的標記來識別。
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499a117372cd7364fc52b3503b30175a4be11afb9e28e3dd32adbf1007185f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048688"
---
# <a name="class-monikers"></a>類別名字標記

雖然類別通常會直接以 Clsid （例如 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)）的 clsid 來識別，但是類別現在也可以使用稱為 *類別標記* 的標記來識別。 類別標記系結至其所建立之類別的類別物件。

找出具有標記之類別的能力，可支援無法使用的實用作業。 例如，檔案的標記通常只支援將 rich binding 系結至與所參考之檔案類別相關聯的類別;Excel 檔案的標記會系結至 Excel 物件的實例，而 GIF 影像的標記會系結至目前註冊之 gif 處理常式的實例。 類別的「標記」（class）可讓您指定要用來透過包含檔案標記的組合來操作檔案的類別。 以名字標記組成 Excel 檔案的3d 圖表類別類別的類別標記會產生會系結至3d 圖表物件實例的標記，並使用 Excel 檔案的內容來初始化物件。

因此，類別名字標記最適合用來與其他類型的專案組合（例如檔案的副檔名或專案的名字標記）組合。

類別的標記也可以撰寫至支援系結至 [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) 介面的名字標記右邊。 以這種方式撰寫時， **IClassActivator** 只會透過 [**IClassActivator：： GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject)提供類別物件和類別實例的存取權。 類別的標記可透過 [**IMoniker：： IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker)來識別，其會傳回 \_ *pdwMksys* 中的 MKSYS CLASSMONIKER。

程式設計人員通常會使用 [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) 函式或透過 [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname)來建立類別標記。  (參閱 [**IMoniker：:P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) ，以取得詳細資料。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[反標記](anti-monikers.md)
</dt> <dt>

[複合的名字](composite-monikers.md)
</dt> <dt>

[檔案名字](file-monikers.md)
</dt> <dt>

[專案的名字](item-monikers.md)
</dt> <dt>

[指標標記](pointer-monikers.md)
</dt> </dl>

 

 




