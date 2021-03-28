---
description: 許多應用程式可讓使用者透過滑鼠拖放資料，或使用剪貼簿來將資料傳送至另一個應用程式。
title: 使用拖放和剪貼簿傳送 Shell 物件
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973245"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>使用拖放和剪貼簿傳送 Shell 物件

許多應用程式可讓使用者透過滑鼠拖放資料，或使用剪貼簿來將資料傳送至另一個應用程式。 可以傳送的許多資料類型都是 Shell 物件（例如檔案或資料夾）。 Shell 資料傳輸可以在兩個應用程式之間進行，但是使用者也可以在桌面或 Windows 檔案總管之間傳送 Shell 資料。

雖然檔案是最常傳送的 Shell 物件，但 Shell 資料傳輸可能牽涉到在 [Shell 命名空間](namespace-intro.md)中找到的各種物件。 比方說，您的應用程式可能需要將檔案傳送到虛擬資料夾，例如資源回收筒，或接受來自非 Microsoft 命名空間延伸模組的物件。 如果您正在執行命名空間延伸，它必須能夠正確地做為卸載來源和目標。

本檔討論應用程式如何使用 Shell 物件來執行拖放和剪貼簿的資料傳輸。

-   [Shell 資料物件](dataobject.md)
-   [Shell 剪貼簿格式](clipboard.md)
-   [處理命令介面資料傳輸案例](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>拖放如何搭配 Shell 物件運作

應用程式通常需要為使用者提供傳輸 Shell 資料的方式。 部分範例如下：

-   從 Windows 檔案總管或桌面拖曳檔案，然後將它放在應用程式上。
-   將檔案複製到 Windows 檔案總管中的剪貼簿，然後貼入應用程式。
-   將檔從應用程式拖曳至資源回收筒。

如需如何處理這些和其他案例的詳細討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)。 本檔著重于 Shell 資料傳輸背後的一般原則。

Windows 提供兩種可讓應用程式傳輸 Shell 資料的標準方式：

-   使用者將 Shell 資料（例如一或多個檔案）剪下或複製到剪貼簿。 另一個應用程式會從剪貼簿抓取資料。
-   使用者將代表來源應用程式之資料的圖示拖曳至目標，並將該圖示放置在目標所擁有的視窗。

在這兩種情況下，傳送的資料都會包含在 *資料物件* 中。 資料物件是元件物件模型 (COM) 物件，這些物件會公開 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面。 架構上，所有 Shell 資料傳輸必須遵循三個基本步驟：

1.  來源會建立資料物件，代表要傳送的資料。
2.  目標會接收資料物件之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的指標。
3.  目標會呼叫 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面來將資料解壓縮。

剪貼簿與拖放資料傳輸之間的差異，主要在於將 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 指標從來源傳送到目標的方式。

### <a name="clipboard-data-transfers"></a>剪貼簿資料傳輸

剪貼簿是傳輸 Shell 資料最簡單的方法。 基本程式類似于標準剪貼簿資料傳輸。 不過，因為您要傳送資料物件的指標，而不是資料本身，所以您必須使用 OLE 剪貼簿 API，而不是標準剪貼簿 API。 下列程式概述如何使用 OLE 剪貼簿 API 來傳送 Shell 資料與剪貼簿：

1.  資料來源會建立包含資料的資料物件。
2.  資料來源會呼叫 [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard)，將資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標放置在剪貼簿上。
3.  目標會呼叫 [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) ，以抓取資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標。
4.  目標會藉由呼叫 [**IDataObject：：：：（**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) ）方法來將資料解壓縮。
5.  使用某些 Shell 資料傳輸時，目標可能也需要呼叫資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，以提供資料傳輸結果的意見反應給資料物件。 如需這類作業的範例，請參閱 [處理優化的移動作業](datascenarios.md) 。

### <a name="drag-and-drop-data-transfers"></a>拖放資料傳輸

更複雜的做法是，拖放資料傳輸在剪貼簿中有一些重要的優點：

-   拖放傳輸可以透過簡單的滑鼠移動來完成，讓作業更具彈性且直覺地使用於剪貼簿。
-   拖放可為使用者提供操作的視覺標記法。 使用者可以在從來源移至目標時追蹤圖示。
-   當資料可供使用時，拖放會通知目標。

拖放作業也會使用資料物件來傳送資料。 不過，卸載來源必須提供剪貼簿傳送所需的功能：

-   Drop source 也必須建立公開 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面的物件。 當作業正在進行時，系統會使用 **IDropSource** 與來源進行通訊。
-   拖放資料物件負責追蹤資料指標移動，並顯示代表資料物件的圖示。

卸載目標也必須提供比處理剪貼簿傳輸所需的更多功能：

-   放置目標必須公開 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面。 當游標在目標視窗上時，系統會使用 **IDropTarget** 來提供目標資訊（例如游標位置），並在卸載資料時通知它。
-   放置目標必須藉由呼叫 [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop)，向系統註冊其本身。 這個函式會為系統提供目標視窗的控制碼，以及目標應用程式之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面的指標。

> [!Note]  
> 針對拖放作業，您的應用程式必須使用 [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize)（而非 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize)）來初始化 COM。

 

下列程式概述通常用來傳送 Shell 資料與拖放的基本步驟：

1.  目標會呼叫 [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) ，為系統提供其 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面的指標，並將視窗註冊為放置目標。
2.  當使用者啟動拖放作業時，來源會建立資料物件，並藉由呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)來起始 *拖曳迴圈*。
3.  當游標在目標視窗上時，系統會呼叫其中一個目標的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 方法，以通知目標。 當游標進入目標視窗時，系統會呼叫 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) ，而當資料指標在目標視窗上傳遞時，則會呼叫 [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 。 這兩種方法都會以目前的游標位置和鍵盤輔助按鍵的狀態（例如 CTRL 或 ALT）提供放置目標。 當資料指標離開目標視窗時，系統會呼叫 [**IDropTarget：:D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave)來通知目標。 當這些方法傳回時，系統會呼叫 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面，將傳回值傳遞給來源。
4.  當使用者放開滑鼠按鍵來捨棄資料時，系統會呼叫目標的 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 方法。 在方法的參數中，是資料物件之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的指標。
5.  目標會呼叫資料物件的 [**IDataObject：：：：：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 的方法來將資料解壓縮。
6.  使用某些 Shell 資料傳輸時，目標可能也需要呼叫資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，以提供對資料傳輸結果來源的意見反應。
7.  當目標完成資料物件時，它會從 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)傳回。 系統會傳回來源的 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 呼叫，以通知來來源資料傳輸已完成。
8.  根據特定的 [資料傳輸案例](datascenarios.md)，來源可能需要根據 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 所傳回的值，以及目標傳遞給資料物件的值，採取額外的動作。 比方說，當移動檔案時，來源必須檢查這些值，以判斷它是否必須刪除原始檔案。
9.  來源會釋放資料物件。

雖然上述程式為 Shell 資料傳輸提供良好的一般模型，但 Shell 資料物件中可包含許多不同類型的資料。 此外，您的應用程式可能需要處理一些不同的資料傳輸案例。 每種資料類型和案例都需要在程式中有稍微不同的方法來處理三個主要步驟：

-   來源如何建立資料物件以包含 Shell 資料。
-   目標如何從資料物件中解壓縮 Shell 資料。
-   來源如何完成資料傳輸作業。

[Shell 資料物件](dataobject.md)提供來源如何建立 Shell 資料物件的一般討論，以及該資料物件可由目標處理的方式。 [處理 Shell 資料傳輸案例](datascenarios.md) 會詳細討論如何處理一些常見的 Shell 資料傳輸案例。

 

 
