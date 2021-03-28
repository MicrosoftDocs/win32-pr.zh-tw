---
description: 本主題討論建立預覽處理常式所需的特定介面和方法。
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: 建立預覽處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318116"
---
# <a name="building-preview-handlers"></a>建立預覽處理常式

本主題討論建立預覽處理常式所需的特定介面和方法。

預覽處理常式必須執行下列介面：

-   [IInitializeWithStream：： Initialize](#iinitializewithstreaminitialize) (強慣用) 、 [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)或 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

如果您的預覽處理常式支援主控制項（例如背景色彩和字型）所提供的視覺效果設定，它也必須執行下列介面：

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

本主題假設預覽處理常式是以資料流程初始化，並且已註冊特定的副檔名。

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream：： Initialize

儲存 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 和 mode 參數，讓您可以在準備好預覽專案時讀取專案的資料。 請勿在 [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize)中載入資料。 載入 IPreviewHandler 中的資料 [**：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 。

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite：： SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite：： GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite：： SetSite

儲存 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標以供稍後存取。

如果您目前有 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 物件的參考，請加以釋放。 使用儲存的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標來呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得新的 **IPreviewHandlerFrame** 參考。

如果您目前有快速鍵對應表，請將它終結。 呼叫 [**IPreviewHandlerFrame：： GetWindowCoNtext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) 以取得新的快速鍵對應表。 儲存此資料表。 請注意，它只會用來做為框架所支援的快速鍵清單。 加速器專案中的命令會被忽略。

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite：： GetSite

傳回網站指標，不管是什麼。

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow：： CoNtextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow：： GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow：： CoNtextSensitiveHelp

傳回 \_ 這個方法的 E >notimpl。

### <a name="iolewindowgetwindow"></a>IOleWindow：： GetWindow

如果預覽處理常式的視窗目前存在，則傳回該視窗的 **HWND** 和 s \_ 確定。 如果視窗不存在，則傳回 E \_ 會失敗。

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler：： SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler：： SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler：:D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler：： SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler：： QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler：： TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler：： Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler：： SetWindow

將這個方法的 *hwnd* 參數設定為預覽處理常式 **hwnd** 的父系。 您可以多次呼叫這個方法。 調整您的預覽大小，使其只在 *prc* 參數所描述的區域中轉譯。

如果預覽程式正在轉譯中，請使用 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) 方法來變更預覽程式的父系。 也請變更預覽程式的呈現區域。

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler：： SetRect

調整您的預覽大小，使其只在此方法的 *中國* 所描述的區域內轉譯。

如果預覽程式正在轉譯中，請變更您的預覽器呈現區域。

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler：:D oPreview

這是實際工作的完成位置。 因為預覽版是動態的，所以只有在需要時才會載入預覽內容。 請勿在初始化中載入內容。

如果預覽處理常式視窗不存在，請加以建立。 預覽處理常式的視窗應該是 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)所提供視窗的子系。 它們應該是 **IPreviewHandler：： SetWindow** 和 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) 所提供的大小， (最近呼叫過的) 。

當您擁有視窗之後，請從已初始化預覽處理常式的 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 載入資料，並將該資料轉譯為您的預覽處理常式視窗。

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler：： SetFocus

當焦點透過索引標籤動作進入讀取窗格時，就會呼叫這個方法。 因為它可以輸入為 [轉寄] 索引標籤或 [反向] 索引標籤，所以請使用 SHIFT 鍵的目前狀態，來決定讀取窗格中的第一個或最後一個索引標籤是否應該接收焦點。

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler：： QueryFocus

這個方法應該呼叫 [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) 函式，並在 *phwnd* 參數中傳回該呼叫的結果。

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler：： TranslateAccelerator

預覽處理常式的進程會呼叫這個方法， (是否 prevhost.exe 或自訂本機伺服器) 來回應使用者擊鍵。 預覽處理常式應該根據下面詳述的演算法來處理這些按鍵，或將它們轉送到其主機。

不過，因為預覽是唯讀的，所以鍵盤輸入應該是最小和優化，例如在許多情況下都不需要這麼做。

如果透過訊息提取傳遞給這個方法的鍵盤快速鍵是預覽處理常式接受的加速器，則處理它，並傳回 S \_ OK。 如果您的處理常式不接受該加速器，則可以將快速鍵訊息傳回給要處理的畫面格。

有兩個選項可將鍵盤快速鍵轉送回框架：

最簡單的模型是使用 [**IPreviewHandlerFrame：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator)將所有擊鍵轉送至主機。 這是在 Windows 軟體開發套件 (SDK) 提供的預覽處理常式範例中完成。 所有低完整性預覽處理常式都必須使用此模型。 如果您的預覽處理常式未處理此加速器，請呼叫 **IPreviewHandlerFrame：： TranslateAccelerator** 並傳回其結果。

另一個模型是使用快速鍵對應表作為優化，以避免跨進程界限傳送太多按鍵：

1.  在預覽處理常式上呼叫 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 時，透過 [**IPreviewHandlerFrame：： GetWindowCoNtext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext)取得快速鍵對應表。  (在您的預覽程式終結時，請務必釋放快速鍵對應表的控制碼。 ) 
2.  如果您的預覽處理常式處理此加速器，請進行處理，並傳回 S \_ OK。
3.  如果您的預覽處理常式未處理此加速器，請針對取得的快速鍵對應表，使用 [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) 來比較訊息。
4.  如果快速鍵符合該快速鍵對應表中的專案，請呼叫 [**IPreviewHandlerFrame：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) 並傳回其結果。
5.  如果快速鍵不符合快速鍵對應表中的任何專案，則傳回 \_ FALSE。

### <a name="ipreviewhandlerunload"></a>IPreviewHandler：： Unload

當呼叫這個方法時，請停止任何轉譯、釋放從資料流程讀取資料所配置的任何資源，然後釋放 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 本身。

一旦呼叫這個方法，就必須重新初始化處理常式，然後再嘗試呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 。

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals::SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

當您導向預覽處理常式來回應主機的色彩和字型配置時，應該執行這些方法。 主機會查詢 [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals)的處理常式。 如果發現支援，主機會提供色彩、字型和文字色彩。

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

當您想要提供背景色彩時，請儲存此色彩，並在轉譯期間使用它。 例如，當處理常式轉譯至小於 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) 和 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)提供之區域的區域時，就會填滿視窗。 不過請注意，您不應該在這些方法所提供的區域之外繪製。

如果在呈現預覽版時呼叫這個方法，則應該使用此背景色彩重新開機轉譯。

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals::SetFont

當您想要顯示與目前 Windows Vista 設定一致的文字時，請儲存此字型資訊，並在轉譯期間使用它。

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

當您想要顯示與目前 Windows Vista 設定一致的文字時，請儲存此文字色彩資訊，並在轉譯期間使用它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預覽處理常式和 Shell 預覽主機](preview-handlers.md)
</dt> <dt>

[如何註冊預覽處理常式](how-to-register-a-preview-handler.md)
</dt> <dt>

[預覽處理常式指導方針](preview-handler-guidelines.md)
</dt> </dl>

 

 
