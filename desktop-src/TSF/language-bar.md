---
title: 'Language Bar (Text Services) '
description: 語言列
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- 文字服務架構 (TSF) 、language bar
- TSF (文字服務架構) 、language bar
- 文字服務，語言列
- 語言列
- 文字服務架構 (TSF) 、按鈕
- TSF (文字服務架構) 、按鈕
- 文字服務，按鈕
- 文字服務架構 (TSF) 、功能表
- TSF (文字服務架構) 、功能表
- 文字服務、功能表
- 按鈕樣式
- 功能表按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c4359c6753f5d96613435f9501036f1d5f317
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524442"
---
# <a name="language-bar-text-services"></a>Language Bar (Text Services) 

## <a name="implementing-the-language-bar-object"></a>執行語言橫條圖物件

若要支援將專案加入至語言列，文字服務必須執行支援 [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) 介面的物件，以及其中一個 [ITfLangBarItem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) 控制項元素。 當安裝專案時，語言列會藉由呼叫專案的[ITfSource：： AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink)和 IID ITfLangBarItemSink 來安裝[ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink)接收器 \_ 。 專案會使用 **ITfLangBarItemSink** 介面來通知語言列的變更，例如隱藏、顯示、啟用或停用專案。

您可以安裝四種類型的語言橫條圖，並從 **ITfLangBarItem** 建立每個必要的介面。 以下是可能的 **ITfLangBarItem** 控制項元素。



|   元素            |    描述                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 按鈕        | 語言列按鈕的功能是命令按鈕、切換控制項或語言列上的功能表。 物件必須支援 ITfLangBarItemButton 介面。                   |
| 氣球       | 語言列球形球形函式可作為語言列上的快顯通知。 物件必須支援 ITfLangBarItemBalloon 介面。                                       |
| 點陣圖        | 語言橫條圖點陣圖可作為顯示點陣圖之語言列上的靜態元素。 物件必須支援 ITfLangBarItemBitmap 介面。                       |
| 點陣圖按鈕 | 語言橫條圖點陣圖按鈕可作為顯示文字和點陣圖之語言列上的按鈕元素。 物件必須支援 ITfLangBarItemBitmapButton 介面。 |



 

## <a name="button-styles"></a>按鈕樣式

按鈕元素可做為下列任何一項。 按鈕專案的函式取決於在 [ITfLangBarItem：： GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo)方法中的 [TF \_ LANGBARITEMINFO](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo)結構之 **dwStyle** 成員中設定的旗標。



|    元素           |    描述                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 按鈕        | 按鈕會作為標準命令按鈕。 此按鈕樣式是由 TF \_ LBI \_ style \_ BTN \_ 按鈕樣式所識別。 按一下專案時，會呼叫 ITfLangBarItemButton：： OnClick。 未使用 ITfLangBarItemButton：： InitMenu 和 ITfLangBarItemButton：： OnMenuSelect。                                                                                                   |
| 切換按鈕 | 按鈕可作為切換控制項，可以維持已按下的狀態，類似于核取方塊。 此按鈕樣式是由 TF \_ LBI \_ style \_ BTN \_ 轉場樣式所識別。 按一下專案時，會呼叫 ITfLangBarItemButton：： OnClick。 未使用 ITfLangBarItemButton：： InitMenu 和 ITfLangBarItemButton：： OnMenuSelect。                                                  |
| 功能表          | 按鈕會以下拉式功能表的形式來運作。 這個按鈕樣式是由 TF \_ LBI \_ style \_ BTN \_ 功能表樣式來識別。 按一下按鈕時，會呼叫 ITfLangBarItemButton：： InitMenu。 當使用者選取功能表中的專案時，語言列會以所選功能表項目的識別碼呼叫 ITfLangBarItemButton：： OnMenuSelect。 ITfLangBarItemButton：： OnClickis 未使用。 |



 

## <a name="implementing-a-menu-button"></a>執行功能表按鈕

當使用者按一下功能表按鈕時，語言列會呼叫 [ITfLangBarItemButton：： InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu)。 專案會使用傳遞至 InitMenu 的 [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) 介面，將專案加入功能表中。

若要將子功能表加入功能表中，請呼叫 [ITfMenu：： AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) with TF \_ LBMENUF \_ 子功能表。 完成這項操作時，會在 AddMenuItem 的 *ppMenu* 參數中傳回代表子功能表的新 **ITfMenu** 物件。 這個新的功能表物件是用來將專案新增至子功能表。

當使用者選取功能表中的專案時，語言列會以所選功能表項目的識別碼呼叫 [ITfLangBarItemButton：： OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) 。

## <a name="adding-items-to-the-language-bar"></a>將專案新增至語言列

文字服務應該在呼叫 [ITfTextInputProcessor：： Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) 方法時，將其專案加入至語言列，並在呼叫其 [ITfTextInputProcessor：:D eactivate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) 時將其移除。

為了將專案加入至語言列，文字服務會透過使用 IID ITfLangBarItemMgr 呼叫 ITfThreadMgr：： QueryInterface 來取得 [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) 介面 \_ 。 文字服務接著會使用語言列專案物件的指標來呼叫 [ITfLangBarItemMgr：： AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) 。

文字服務必須在停用時移除專案。 文字服務會使用用來加入專案的相同 **ITfLangBarItemMgr** 介面，或取得介面的另一個實例。 然後，文字服務會呼叫 [ITfLangBarItemMgr：： RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) ，以及要移除之專案的介面指標。

## <a name="extending-system-language-bar-items"></a>擴充 System Language Bar 專案

TSF 可讓您將功能表項目加入至現有的語言列功能表。 這可讓文字服務將專案加入至其他文字服務的功能表中，而不需要將個別按鈕新增至工具列。 這也可讓功能表項目組織成邏輯群組。 例如，將其他功能提供給標準語音文字服務的文字服務，可以將專案新增至語音文字服務功能表，而不是加入自己的最上層功能表按鈕。

文字服務會藉由執行支援 [ITfSystemLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) 介面的物件，提供語言列功能表延伸。 這個介面的運作方式與功能表按鈕的 [ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) 介面完全相同。 顯示功能表時，所擴充的文字服務會呼叫 [ITfSystemLangBarItemSink：： InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu)。 此延伸模組會使用傳遞至 **InitMenu** 的 [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu)介面，將專案新增至功能表中。 當使用者選取擴充功能所加入的專案時，所擴充的文字服務會呼叫 [ITfSystemLangBarItemSink：： OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) ，並提供所選功能表項目的識別碼。

若要安裝語言列功能表擴充功能，文字服務會完成下列步驟。

1.  藉由呼叫 [ITfLangBarItemMgr：： GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem)和要擴充之專案的 **GUID** ，來取得要延伸之專案的 **ITfLangBarItem** 介面。
2.  藉由使用 IID ITfSource 來呼叫 ITfLangBarItem：： QueryInterface，以取得要延伸之專案的 **ITfSource** 介面 \_ 。
3.  使用 [](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) IID \_ ITfSystemLangBarItemSink 和 **ITfSystemLangBarItemSink** 物件的指標呼叫 ITfSource：： AdviseSink。 如果 ITfSource：： AdviseSink 失敗，則文字服務不支援功能表延伸。

[ITfSource：： UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource：： AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>支援語言列功能表延伸模組

文字服務可以讓其他文字服務將專案新增至其語言列功能表，如上所示。 必須發行其 GUID 的文字服務，以便藉由呼叫 [ITfLangBarItemMgr：： GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem)來取得專案。

若要支援功能表延伸，文字服務必須支援 [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) 介面。 下列步驟可讓您支援一或多個功能表延伸模組。

1.  當呼叫 [ITfSource：： AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) 與 IID \_ ITfSystemLangBarItemSink 時，文字服務必須儲存 **ITfSystemLangBarItemSink** 介面，並傳回將識別延伸模組的 cookie 值。
2.  呼叫 [ITfLangBarItemButton：： InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) 時，文字服務會呼叫延伸模組的 [ITfSystemLangBarItemSink：： InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) 方法。 文字服務必須執行方法來識別擴充功能所加入的功能表項目，而不是文字服務本身加入的專案。
3.  使用屬於延伸模組的功能表項目識別碼呼叫 [ITfLangBarItemButton：： OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) 時，文字服務會呼叫延伸模組的 **ITfSystemLangBarItemSink：： OnMenuSelect** 方法。
4.  使用適當的 cookie 呼叫 [ITfSource：： UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) 時，文字服務會移除功能表延伸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何設定文字服務架構](how-to-set-up-tsf.md)
</dt> <dt>

[Language Bar (應用程式) ](language-bar-app.md)
</dt> </dl>

 

 
