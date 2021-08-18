---
title: 關於剪貼簿
description: 本節討論剪貼簿。
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- 剪貼簿，關於
- 剪貼簿，格式
- 剪貼簿、命令
- 剪貼簿、windows
- 剪貼簿、序號
- 剪貼簿，檢視器
- 剪貼簿，檢視器視窗
- 剪貼簿、顯示格式
- 剪貼簿，擁有者顯示格式
- 顯示剪貼簿格式
- 擁有者顯示剪貼簿格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a3ddc96cbc1d440fda5e6484f1bc72a53b4b36b709c7ad80c77e203dadcef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128630"
---
# <a name="about-the-clipboard"></a>關於剪貼簿

*剪貼* 簿是一組可讓應用程式傳輸資料的函式和訊息。 由於所有應用程式都有存取剪貼簿的許可權，因此可以輕鬆地在應用程式之間或應用程式內傳輸資料。

剪貼簿是由使用者驅動的。 視窗應該只是為了回應使用者的命令而傳送到剪貼簿的資料。 視窗不能使用剪貼簿來傳送資料，而不需要使用者的知識。

剪貼簿上的記憶體物件可以採用任何資料格式，稱為「剪貼簿」格式。 每種格式都是以不帶正負號的整數值來識別。 針對標準 (預先定義的) 剪貼簿格式，此值是在 Winuser 中定義的常數;針對已註冊的剪貼簿格式，它是 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函式的傳回值。

除了註冊剪貼簿格式之外，個別的視窗也會執行大部分的剪貼簿作業。 一般而言，視窗程式會將資訊傳送到剪貼簿，以回應 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。

本節將討論下列各項：

-   [剪貼簿命令](#clipboard-commands)
-   [剪貼簿序號](#clipboard-sequence-number)
-   [剪貼簿檢視器](#clipboard-viewers)
    -   [剪貼簿檢視器 Windows](#clipboard-viewer-windows)
    -   [顯示格式](#display-formats)
    -   [擁有者顯示格式](#owner-display-format)
-   [相關主題](#related-topics)

## <a name="clipboard-commands"></a>剪貼簿命令

使用者通常會從應用程式的 [ **編輯** ] 功能表中選擇命令，以執行剪貼簿作業。 以下是標準剪貼簿命令的簡短描述。



|  命令        |  描述                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **剪下**    | 將目前選取範圍的複本放在剪貼簿，並從檔中刪除選取專案。 剪貼簿的先前內容已損毀。                                                          |
| **複製**   | 將目前選取範圍的複本放在剪貼簿上。 檔會維持不變。 剪貼簿的先前內容已損毀。                                                                      |
| **貼上**  | 以剪貼簿的內容取代目前的選取範圍。 剪貼簿的內容不會變更。                                                                                                    |
| **刪除** | 從檔中刪除目前的選取範圍。 剪貼簿的內容不會變更。 此命令不牽涉到剪貼簿，但它應該會在 [ **編輯** ] 功能表上顯示 [剪貼簿] 命令。 |



 

## <a name="clipboard-sequence-number"></a>剪貼簿序號

每個視窗工作站的剪貼簿都有相關聯的剪貼簿序號。 每當剪貼簿的內容變更時，這個數位就會遞增。 若要取得剪貼簿序號，請呼叫 [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) 函數。

## <a name="clipboard-viewers"></a>剪貼簿檢視器

剪貼簿檢視器是一種視窗，可顯示剪貼簿的目前內容。 [剪貼簿檢視器] 視窗是使用者的便利性，並且不會影響剪貼簿的資料交易功能。

剪貼簿檢視器視窗通常可以顯示至少三種最常見的格式： **cf \_ TEXT**、 **cf \_ BITMAP** 和 **cf \_ METAFILEPICT**。 如果視窗沒有提供這三種格式的資料，則應提供顯示格式的資料，或使用擁有者顯示格式。

*剪貼簿檢視器* 會將兩個或多個實體連結在一起，使其相依于另一個實體。 這個相互相關性 (鏈) 允許所有執行中的剪貼簿檢視器應用程式接收傳送到目前剪貼簿的訊息。

本節將討論下列主題。

-   [剪貼簿檢視器 Windows](#clipboard-viewer-windows)
-   [顯示格式](#display-formats)
-   [擁有者顯示格式](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>剪貼簿檢視器 Windows

視窗會藉由呼叫 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函式，將本身新增至剪貼簿檢視器鏈。 傳回值是鏈中下一個視窗的控制碼。 若要取得鏈中第一個視窗的控制碼，請呼叫 [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) 函數。

每個剪貼簿檢視器視窗都必須追蹤剪貼簿檢視器鏈中的下一個視窗。 當剪貼簿的內容變更時，系統會將 [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 訊息傳送至鏈中的第一個視窗。 更新其顯示之後，每個剪貼簿檢視器視窗都必須將此訊息傳遞至鏈中的下一個視窗。

在關閉之前，剪貼簿檢視器視窗必須藉由呼叫 [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) 函數，從剪貼簿檢視器鏈中移除本身。 然後系統會將 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息傳送至鏈中的第一個視窗。

如需處理 [**wm \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 和 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息的詳細資訊，請參閱 [建立剪貼簿檢視器視窗](using-the-clipboard.md)。

### <a name="display-formats"></a>顯示格式

顯示格式是用來在 [剪貼簿檢視器] 視窗中顯示資訊的剪貼簿格式。 使用私用或已註冊剪貼簿格式的剪貼簿擁有者，以及沒有最常見的標準格式，都必須提供顯示格式的資料，以便在 [剪貼簿檢視器] 視窗中進行觀看。 顯示格式僅供觀賞之用，不得貼入檔中。

四種顯示格式為： **cf \_ DSPBITMAP**、 **cf \_ DSPMETAFILEPICT**、 **cf \_ DSPTEXT** 和 **CF \_ DSPENHMETAFILE**。 這些顯示格式的轉譯方式與標準格式相同，也就是： **cf \_ BITMAP**、 **cf \_ TEXT**、 **cf \_ METAFILEPICT** 和 **cf \_ ENHMETAFILE**。

### <a name="owner-display-format"></a>擁有者顯示格式

針對不使用任何一般標準剪貼簿格式的剪貼簿擁有者，提供顯示格式的替代方式是使用擁有者顯示 (**CF \_ OWNERDISPLAY**) 剪貼簿格式。

剪貼簿擁有者可以使用擁有者顯示格式，藉由直接控制剪貼簿檢視器視窗，來避免以其他格式轉譯資料的額外負荷。 只要重新繪製視窗的一部分，或是滾動或調整視窗的大小，[剪貼簿檢視器] 視窗就會將訊息傳送給剪貼簿擁有者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[標準剪貼簿格式](standard-clipboard-formats.md)
</dt> </dl>

 

 