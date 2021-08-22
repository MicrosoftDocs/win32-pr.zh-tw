---
title: 剪貼簿作業
description: 當您剪下、複製或貼上資料時，視窗應該使用剪貼簿。 視窗會將資料放在剪貼簿上，以進行剪下和複製作業，並從剪貼簿取得貼上作業的資料。
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows消費者介面，剪貼簿
- 剪貼簿、windows
- 剪貼簿，資料剪下
- 剪貼簿，複製資料
- 剪貼簿，貼上資料
- 剪貼簿，擁有者視窗
- 剪貼簿，延遲轉譯
- 剪貼簿、記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545432"
---
# <a name="clipboard-operations"></a>剪貼簿作業

當您剪下、複製或貼上資料時，視窗應該使用剪貼簿。 視窗會將資料放在剪貼簿上，以進行剪下和複製作業，並從剪貼簿取得貼上作業的資料。 下列各節將說明這些作業和相關問題。

若要將資料放在剪貼簿中或從中取出資料，視窗必須先使用 [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) 函式來開啟剪貼簿。 一個視窗一次只能開啟一個 [剪貼簿]。 若要找出開啟 [剪貼簿] 的視窗，請呼叫 [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) 函式。 完成時，視窗必須藉由呼叫 [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) 函數來關閉剪貼簿。

本節將討論下列主題。

-   [剪下和複製作業](#cut-and-copy-operations)
-   [貼上作業](#paste-operations)
-   [剪貼簿擁有權](#clipboard-ownership)
-   [延遲轉譯](#delayed-rendering)
-   [記憶體和剪貼簿](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>剪下和複製作業

為了將資訊放置在剪貼簿上，視窗會先使用 [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) 函式來清除任何先前的剪貼簿內容。 此函式會將 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息傳送至先前的剪貼簿擁有者、釋出與剪貼簿上的資料相關聯的資源，以及將剪貼簿擁有權指派給開啟 [剪貼簿] 的視窗。 若要找出哪個視窗擁有剪貼簿，請呼叫 [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) 函數。

清除剪貼簿之後，視窗會盡可能將剪貼簿格式的資料放在剪貼簿中，並以最描述性的剪貼簿格式排序，以最不描述性的方式排序。 針對每一種格式，視窗都會呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式，並指定格式識別碼和全域記憶體控制碼。 記憶體控制碼可以是 Null，表示視窗會依要求呈現資料。 如需詳細資訊，請參閱 [延遲](#delayed-rendering)轉譯。

## <a name="paste-operations"></a>貼上作業

為了抓取剪貼簿中的貼上資訊，視窗會先決定要取出的剪貼簿格式。 通常，視窗會使用 [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) 函式來列舉可用的剪貼簿格式，並使用它所辨識的第一種格式。 這個方法會根據將資料放在剪貼簿上時所設定的優先順序，來選取最佳的可用格式。

或者，視窗也可以使用 [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) 函式。 此函式會根據指定的優先順序，識別最佳的可用剪貼簿格式。 只能辨識一個剪貼簿格式的視窗，可以使用 [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) 函式來判斷該格式是否可供使用。

判斷要使用的剪貼簿格式後，視窗會呼叫 [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) 函數。 此函式會傳回全域記憶體物件的控制碼，該物件包含指定之格式的資料。 視窗可以短暫地鎖定記憶體物件，以便檢查或複製資料。 不過，視窗不應該釋出物件或讓它保持鎖定一段很長的時間。

## <a name="clipboard-ownership"></a>剪貼簿擁有權

*剪貼簿擁有* 者是與剪貼簿資訊相關聯的視窗。 當視窗將資料放在剪貼簿上時（特別是在呼叫 [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) 函式時），視窗就會變成剪貼簿擁有者。 視窗會維持剪貼簿擁有者，直到它關閉或另一個視窗清空剪貼簿。

當剪貼簿清空時，剪貼簿擁有者會收到 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息。 以下是視窗可能處理此訊息的一些原因：

-   視窗延遲呈現一或多個剪貼簿格式。 為了回應 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息，視窗可能會釋放已配置的資源，以便在要求時呈現資料。 如需資料呈現的詳細資訊，請參閱 [延遲](#delayed-rendering)轉譯。
-   視窗會以私用剪貼簿格式將資料放在剪貼簿上。 當剪貼簿清空時，系統不會釋放私人剪貼簿格式的資料。 因此，剪貼簿擁有者應該在收到 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息時釋出資料。 如需私用剪貼簿格式的詳細資訊，請參閱 [剪貼簿格式](clipboard-formats.md)。
-   視窗會使用 **CF \_ OWNERDISPLAY** 剪貼簿格式將資料放在剪貼簿上。 為了回應 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息，視窗可能會在 [剪貼簿檢視器] 視窗中釋放用來顯示資訊的資源。 如需此替代格式的詳細資訊，請參閱 [擁有者顯示格式](about-the-clipboard.md)。

## <a name="delayed-rendering"></a>延遲轉譯

將剪貼簿格式放在剪貼簿上時，視窗可以延遲轉譯該格式的資料，直到需要資料為止。 若要這樣做，應用程式可以針對 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)函數的 *HData* 參數指定 **Null** 。 如果應用程式支援數個剪貼簿格式，部分或全部都是需要花費的時間來轉譯，這會很有用。 藉由傳遞 **Null** 控制碼，視窗只會在需要時呈現複雜的剪貼簿格式。

如果視窗延遲轉譯剪貼簿格式，只要是剪貼簿擁有者，就必須做好準備，以便在要求時呈現格式。 當針對尚未轉譯的特定格式收到要求時，系統會傳送 [**WM \_ RENDERFORMAT**](wm-renderformat.md) 訊息給剪貼簿擁有者。 收到此訊息時，視窗應該呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式，以要求的格式將全域記憶體控制碼放置在剪貼簿上。

應用程式必須在呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 之前開啟剪貼簿，以回應 [**WM \_ RENDERFORMAT**](wm-renderformat.md) 訊息。 開啟剪貼簿並不是必要的，而且嘗試這麼做會失敗，因為剪貼簿目前正由要求轉譯格式的應用程式開啟。

如果剪貼簿擁有者即將終結，且延遲轉譯部分或所有剪貼簿格式，則會收到 [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息。 收到這則訊息時，視窗應該會開啟剪貼簿，檢查它是否仍是具有 [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) 功能的剪貼簿擁有者，然後將有效的記憶體控制碼放置在剪貼簿上，以取得它所提供的所有剪貼簿格式。 這可確保這些格式在剪貼簿擁有者終結之後仍可供使用。

不同于 [**wm \_ RENDERFORMAT**](wm-renderformat.md)，回應 [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) 的應用程式應該先開啟剪貼簿，然後再呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) ，以將任何全域記憶體控點放置在剪貼簿上。

未轉譯以回應 [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息的任何剪貼簿格式都會停止供其他應用程式使用，且不會再由剪貼簿功能列舉。

## <a name="memory-and-the-clipboard"></a>記憶體和剪貼簿

要放置在剪貼簿上的記憶體物件，應該使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函式搭配 **GMEM \_ 可移動** 旗標進行配置。

將記憶體物件放到剪貼簿之後，就會將該記憶體控制碼的擁有權傳送至系統。 當剪貼簿已清空，且記憶體物件具有下列其中一種剪貼簿格式時，系統會藉由呼叫指定的函式來釋出記憶體物件：



| 釋放物件的函式                             | 剪貼簿格式                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **CF \_ 點陣圖**<br/> **CF \_ DSPBITMAP**<br/> **CF \_ 調色板**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **CF \_ 文字**<br/> **CF \_ UNICODETEXT**<br/>   |
| 無<br/>                                     | **CF \_ OWNERDISPLAY**<br/> 當剪貼簿清空 **CF \_ OWNERDISPLAY** 物件時，應用程式本身必須釋放記憶體物件。<br/> |



 

 

