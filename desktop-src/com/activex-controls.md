---
title: ActiveX 控制項
description: ActiveX 控制項
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382910"
---
# <a name="activex-controls"></a>ActiveX 控制項

ActiveX 控制項技術的基礎，是由 COM、可連線物件、複合檔案、屬性頁、OLE automation、物件持續性，以及系統提供的字型和圖片物件所組成。 如下所示，每個核心技術都扮演控制項中的角色。

<dl> <dt>

<span id="COM"></span><span id="com"></span>Com
</dt> <dd>

控制項本質上是公開 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的 COM 物件，用戶端可以透過此介面取得其其他介面的指標。 控制項可透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 和自我註冊來支援授權。 如需有關 COM、授權和自我註冊的詳細資訊，請參閱 [元件物件模型](the-component-object-model.md) 。

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>可連線物件
</dt> <dd>

控制項可透過可連接的物件支援輸出介面，讓控制項可以與其用戶端進行通訊。 例如，傳出介面可以在用戶端中觸發動作，可以在控制項中通知用戶端某些變更，或者可以在控制項採取一些動作之前要求用戶端的許可權。 如需可連線物件如何運作的詳細資訊，請參閱 [COM 中的事件和](events-in-com-and-connectable-objects.md) 可連接的物件。

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>制式資料傳輸
</dt> <dd>

控制項可支援在容器內拖曳和卸載容器，以及其容器的協助。 如需拖放的詳細資訊，請參閱 [**IOleInPlaceObjectWindowless：： GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) 。

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>複合檔案
</dt> <dd>

控制項可以是可內嵌在包含用戶端中的就地作用中物件。 終端使用者啟動控制項，以在容器應用程式中起始動作。 如需就地啟用和其他複合檔案介面的詳細資訊，請參閱 [複合檔案](compound-documents.md) 。

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>屬性頁
</dt> <dd>

控制項可以提供屬性頁，讓使用者可以查看及變更控制項的屬性。 如需屬性頁如何運作的詳細資訊，請參閱 [屬性頁和屬性工作表](property-pages-and-property-sheets.md) 。

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation
</dt> <dd>

控制項可以透過 OLE automation 提供可程式性，讓用戶端可以透過用戶端所提供的程式設計語言來利用控制項的功能。 如需 OLE automation 的詳細資訊，請參閱 OLE Automation 一節。

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>持續性儲存體
</dt> <dd>

控制項可以執行數個持續性介面中的一或多個，以支援其狀態的持續性。 控制項實施者必須決定哪些類型的持續性最重要，並執行適當的持續性介面。 用戶端會決定要使用的介面。 如需所有持續性介面的詳細資訊，請參閱 [元件物件模型](the-component-object-model.md) 。

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>字型和圖片物件
</dt> <dd>

控制項可以使用這些系統提供的物件，在用戶端中提供自己的視覺標記法。 字型物件會實作為多個介面，包括 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) 和 [**>ifontdisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)。 您可以使用 [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)來建立字型物件。 Picture 物件也會實作為數個介面，包括 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 和 [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)。 您可以使用 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) 來建立圖片物件，也可以使用 [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)從資料流程載入。

</dd> </dl>

請務必瞭解這些功能可以用於任何 OLE 物件中。 其中一個控制項不需要執行控制項，就能使用這些功能。 此外，控制項上的唯一必要介面是 IUnknown。 控制項可根據支援相關功能的需求，選擇性地支援其他介面。

除了這些功能之外，下列介面和函式僅適用于控制項技術： [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)、 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)、 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)和 [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)。 此外，針對控制項或控制項容器可支援的屬性和方法，這也是控制項專屬的一組標準。

> [!Note]  
> 系統程式庫 OleAut32.dll 包含 ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe)、 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)、 [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)、 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)、 [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)和 [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)) 的函式的實作為。 此外，OleAut32.dll 包含標準字型和圖片物件的實作為，以及用於控制項的所有介面以及其他資料結構和資料類型的類型程式庫。

 

如需詳細資訊，請參閱下列主題：

-   [ActiveX 控制項架構](activex-controls-architecture.md)
-   [ActiveX 控制項介面](activex-controls-interfaces.md)
-   [屬性和方法](properties-and-methods.md)
-   [控制項事件](control-events.md)
-   [視覺標記法](visual-representation.md)
-   [控制項的鍵盤處理](keyboard-handling-for-controls.md)
-   [持續性](persistence.md)
-   [註冊和授權](registration-and-licensing.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX 控制項和控制項容器指導方針](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 