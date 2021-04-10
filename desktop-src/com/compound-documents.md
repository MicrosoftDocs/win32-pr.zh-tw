---
title: 複合檔案
description: OLE 複合檔案可讓使用者在單一應用程式中運作，以操作以各種格式撰寫並衍生自多個來源的資料。
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093407"
---
# <a name="compound-documents"></a>複合檔案

OLE 複合檔案可讓使用者在單一應用程式中運作，以操作以各種格式撰寫並衍生自多個來源的資料。 例如，使用者可能會在第二個應用程式中建立的圖形和在第三個應用程式中建立的音效物件插入文字處理檔中。 啟用圖形會導致第二個應用程式載入其使用者介面，或至少包含編輯物件所需工具的元件。 啟用音效物件會導致第三個應用程式播放它。 在這兩種情況下，使用者都可以從單一檔的內容中，操作來自外部來源的資料。

OLE 複合檔案技術是在由 COM、結構化儲存體和制式資料傳輸所組成的基礎上。 如下所示，每個核心技術在 OLE 複合檔案中扮演著重要的角色：

<dl> <dt>

<span id="COM"></span><span id="com"></span>Com
</dt> <dd>

複合檔案物件基本上是可內嵌或連結至現有檔的 COM 物件。 複合檔案物件是 COM 物件，它會公開 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面，讓用戶端可以透過此介面取得其其他介面的指標，包括數個，例如 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)、 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)和 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)，以提供複合檔案物件特有的特殊功能。

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>結構化儲存體
</dt> <dd>

複合檔案物件必須執行 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) 或（選擇性） [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 介面來管理本身的儲存體。 用來建立複合檔案的容器必須提供 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面，物件可透過這些介面儲存和取出資料。 容器幾乎一律會提供從 OLE 的複合檔案執行所取得的 **IStorage** 實例。 容器也必須使用物件的 **IPersistStorage** 和/或 **IPersistStream** 介面。

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>制式資料傳輸
</dt> <dd>

支援複合檔案的應用程式必須執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ，因為嵌入的物件和連結的物件是以使用特殊 OLE 剪貼簿格式（而非標準 Microsoft Windows 剪貼簿格式）傳輸的資料作為開頭。 換句話說，以內嵌或連結化物件的格式設定資料，只是 OLE 的制式資料傳輸模型提供的另一個選項。

</dd> </dl>

OLE 的複合檔案技術同時也受益軟體發展人員和使用者。 軟體發展人員如果想要將每個可想像的功能 cram 到單一應用程式，而不是想要開發更小且更具焦點的應用程式，而這些應用程式依賴其他應用程式來提供其他功能。 如果軟體發展人員決定提供的應用程式的功能超出其核心功能，開發人員可以將這些額外的服務實作為個別的 Dll，而這些 Dll 只有在需要服務時才會載入到記憶體中。 使用者可受益于更小、更快速、更強大的軟體，這些軟體可以視需要混合和比對，從單一主檔案內操作所有必要的元件。

如需詳細資訊，請參閱下列主題：

-   [容器和伺服器](containers-and-servers.md)
-   [連結和內嵌](linking-and-embedding.md)
-   [物件處理常式](object-handlers.md)
-   [同進程伺服器](in-process-servers.md)
-   [連結的物件和名字](linked-objects-and-monikers.md)
-   [通知](notifications.md)
-   [複合檔案介面](compound-document-interfaces.md)
-   [物件狀態](object-states.md)
-   [執行 In-Place 啟用](implementing-in-place-activation.md)
-   [從現有資料建立連結和內嵌物件](creating-linked-and-embedded-objects-from-existing-data.md)
-   [視圖快取](view-caching.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料轉送](data-transfer.md)
</dt> <dt>

[結構化儲存體](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 