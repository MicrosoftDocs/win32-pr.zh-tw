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
# <a name="activex-controls"></a><span data-ttu-id="1afca-103">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="1afca-103">ActiveX Controls</span></span>

<span data-ttu-id="1afca-104">ActiveX 控制項技術的基礎，是由 COM、可連線物件、複合檔案、屬性頁、OLE automation、物件持續性，以及系統提供的字型和圖片物件所組成。</span><span class="sxs-lookup"><span data-stu-id="1afca-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="1afca-105">如下所示，每個核心技術都扮演控制項中的角色。</span><span class="sxs-lookup"><span data-stu-id="1afca-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="1afca-106"><span id="COM"></span><span id="com"></span>Com</span><span class="sxs-lookup"><span data-stu-id="1afca-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="1afca-107">控制項本質上是公開 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的 COM 物件，用戶端可以透過此介面取得其其他介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1afca-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="1afca-108">控制項可透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 和自我註冊來支援授權。</span><span class="sxs-lookup"><span data-stu-id="1afca-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="1afca-109">如需有關 COM、授權和自我註冊的詳細資訊，請參閱 [元件物件模型](the-component-object-model.md) 。</span><span class="sxs-lookup"><span data-stu-id="1afca-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>可連線物件</span><span class="sxs-lookup"><span data-stu-id="1afca-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="1afca-111">控制項可透過可連接的物件支援輸出介面，讓控制項可以與其用戶端進行通訊。</span><span class="sxs-lookup"><span data-stu-id="1afca-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="1afca-112">例如，傳出介面可以在用戶端中觸發動作，可以在控制項中通知用戶端某些變更，或者可以在控制項採取一些動作之前要求用戶端的許可權。</span><span class="sxs-lookup"><span data-stu-id="1afca-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="1afca-113">如需可連線物件如何運作的詳細資訊，請參閱 [COM 中的事件和](events-in-com-and-connectable-objects.md) 可連接的物件。</span><span class="sxs-lookup"><span data-stu-id="1afca-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>制式資料傳輸</span><span class="sxs-lookup"><span data-stu-id="1afca-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="1afca-115">控制項可支援在容器內拖曳和卸載容器，以及其容器的協助。</span><span class="sxs-lookup"><span data-stu-id="1afca-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="1afca-116">如需拖放的詳細資訊，請參閱 [**IOleInPlaceObjectWindowless：： GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="1afca-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>複合檔案</span><span class="sxs-lookup"><span data-stu-id="1afca-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="1afca-118">控制項可以是可內嵌在包含用戶端中的就地作用中物件。</span><span class="sxs-lookup"><span data-stu-id="1afca-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="1afca-119">終端使用者啟動控制項，以在容器應用程式中起始動作。</span><span class="sxs-lookup"><span data-stu-id="1afca-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="1afca-120">如需就地啟用和其他複合檔案介面的詳細資訊，請參閱 [複合檔案](compound-documents.md) 。</span><span class="sxs-lookup"><span data-stu-id="1afca-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>屬性頁</span><span class="sxs-lookup"><span data-stu-id="1afca-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="1afca-122">控制項可以提供屬性頁，讓使用者可以查看及變更控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="1afca-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="1afca-123">如需屬性頁如何運作的詳細資訊，請參閱 [屬性頁和屬性工作表](property-pages-and-property-sheets.md) 。</span><span class="sxs-lookup"><span data-stu-id="1afca-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span><span class="sxs-lookup"><span data-stu-id="1afca-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="1afca-125">控制項可以透過 OLE automation 提供可程式性，讓用戶端可以透過用戶端所提供的程式設計語言來利用控制項的功能。</span><span class="sxs-lookup"><span data-stu-id="1afca-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="1afca-126">如需 OLE automation 的詳細資訊，請參閱 OLE Automation 一節。</span><span class="sxs-lookup"><span data-stu-id="1afca-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>持續性儲存體</span><span class="sxs-lookup"><span data-stu-id="1afca-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="1afca-128">控制項可以執行數個持續性介面中的一或多個，以支援其狀態的持續性。</span><span class="sxs-lookup"><span data-stu-id="1afca-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="1afca-129">控制項實施者必須決定哪些類型的持續性最重要，並執行適當的持續性介面。</span><span class="sxs-lookup"><span data-stu-id="1afca-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="1afca-130">用戶端會決定要使用的介面。</span><span class="sxs-lookup"><span data-stu-id="1afca-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="1afca-131">如需所有持續性介面的詳細資訊，請參閱 [元件物件模型](the-component-object-model.md) 。</span><span class="sxs-lookup"><span data-stu-id="1afca-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>字型和圖片物件</span><span class="sxs-lookup"><span data-stu-id="1afca-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="1afca-133">控制項可以使用這些系統提供的物件，在用戶端中提供自己的視覺標記法。</span><span class="sxs-lookup"><span data-stu-id="1afca-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="1afca-134">字型物件會實作為多個介面，包括 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) 和 [**>ifontdisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)。</span><span class="sxs-lookup"><span data-stu-id="1afca-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="1afca-135">您可以使用 [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)來建立字型物件。</span><span class="sxs-lookup"><span data-stu-id="1afca-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="1afca-136">Picture 物件也會實作為數個介面，包括 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 和 [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)。</span><span class="sxs-lookup"><span data-stu-id="1afca-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="1afca-137">您可以使用 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) 來建立圖片物件，也可以使用 [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)從資料流程載入。</span><span class="sxs-lookup"><span data-stu-id="1afca-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="1afca-138">請務必瞭解這些功能可以用於任何 OLE 物件中。</span><span class="sxs-lookup"><span data-stu-id="1afca-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="1afca-139">其中一個控制項不需要執行控制項，就能使用這些功能。</span><span class="sxs-lookup"><span data-stu-id="1afca-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="1afca-140">此外，控制項上的唯一必要介面是 IUnknown。</span><span class="sxs-lookup"><span data-stu-id="1afca-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="1afca-141">控制項可根據支援相關功能的需求，選擇性地支援其他介面。</span><span class="sxs-lookup"><span data-stu-id="1afca-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="1afca-142">除了這些功能之外，下列介面和函式僅適用于控制項技術： [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)、 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)、 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)和 [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)。</span><span class="sxs-lookup"><span data-stu-id="1afca-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="1afca-143">此外，針對控制項或控制項容器可支援的屬性和方法，這也是控制項專屬的一組標準。</span><span class="sxs-lookup"><span data-stu-id="1afca-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="1afca-144">系統程式庫 OleAut32.dll 包含 ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe)、 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)、 [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)、 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)、 [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)和 [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)) 的函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="1afca-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="1afca-145">此外，OleAut32.dll 包含標準字型和圖片物件的實作為，以及用於控制項的所有介面以及其他資料結構和資料類型的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="1afca-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="1afca-146">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="1afca-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1afca-147">ActiveX 控制項架構</span><span class="sxs-lookup"><span data-stu-id="1afca-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="1afca-148">ActiveX 控制項介面</span><span class="sxs-lookup"><span data-stu-id="1afca-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="1afca-149">屬性和方法</span><span class="sxs-lookup"><span data-stu-id="1afca-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="1afca-150">控制項事件</span><span class="sxs-lookup"><span data-stu-id="1afca-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="1afca-151">視覺標記法</span><span class="sxs-lookup"><span data-stu-id="1afca-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="1afca-152">控制項的鍵盤處理</span><span class="sxs-lookup"><span data-stu-id="1afca-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="1afca-153">持續性</span><span class="sxs-lookup"><span data-stu-id="1afca-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="1afca-154">註冊和授權</span><span class="sxs-lookup"><span data-stu-id="1afca-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="1afca-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="1afca-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1afca-156">ActiveX 控制項和控制項容器指導方針</span><span class="sxs-lookup"><span data-stu-id="1afca-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 