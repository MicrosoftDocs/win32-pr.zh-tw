---
title: 實例建立 Helper 函數
description: 實例建立 Helper 函數
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024139"
---
# <a name="instance-creation-helper-functions"></a>實例建立 Helper 函數

在舊版的 COM 中，用來建立物件實例的主要機制是 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。 此函式會封裝建立類別物件的程式，並使用該物件建立新的實例和釋放類別物件。 這種類型的另一個函式是更特定的 [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)，這是可建立類別物件並抓取所要求物件之指標的 OLE 複合檔案協助程式。

為了使在分散式系統上建立實例的程式更順暢，COM 引進四個重要的新實例建立機制：

-   類別的名字和 [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

類別的「標記」（class）可讓您識別物件的類別，而且通常會與另一個標記（例如檔案的標記）搭配使用，以指出物件的位置。 這可讓您系結至物件，並指定要為該物件啟動的伺服器。 類別的標記也可以撰寫至支援系結至 [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) 介面的名字標記右邊。 如需詳細資訊，請參閱 [類別的名字](class-monikers.md)。

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) 延伸了 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ，讓您能夠在指定的遠端電腦上建立與指定 CLSID 相關聯的單一未初始化物件。 此外，除了要求單一介面並取得該介面的單一指標之外， **CoCreateInstanceEx** 還可讓您查詢多個介面，並 (（如果有) 的話），以在單次往返中接收這些介面的指標，進而減少機器之間的來回行程。 這樣可讓遠端物件互動更加有效率。 若要這樣做，函數會使用多個 [**\_ QI**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) 結構的陣列。

透過 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) 建立物件仍然需要透過呼叫其中一個初始化 (介面來初始化物件，例如 [**IPersistStorage：： Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)) 。 Helper 函式 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) 和 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) 會封裝 **CoCreateInstanceEx** 的實例建立能力和初始化，並將前者從檔案和後者（從儲存體）封裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[透過類別物件建立物件](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 