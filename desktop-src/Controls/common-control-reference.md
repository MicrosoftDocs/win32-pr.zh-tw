---
title: 一般控制項參考
description: 本章節包含適用于多個控制項之程式設計項目的參考資訊，而不只是特定控制項的參考資訊。
ms.assetid: c8e72ae9-7c71-465d-9a6b-07e7923d4a13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f87c98f95f5cb00412b0018bda247c6ced49a6d4
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812712"
---
# <a name="general-control-reference"></a>一般控制項參考

本章節包含適用于多個控制項之程式設計項目的參考資訊，而不只是特定控制項的參考資訊。 有許多控制項都支援的函式、宏、訊息、通知和結構。 例如，大部分的控制項都使用 [NM \_ 停留](nm-hover.md) 通知來處理滑鼠點擊。

-   [概觀](#overviews)
-   [函數](#functions)
-   [巨集](#macros)
-   [訊息](#messages)
-   [通知](#notifications)
-   [結構](#structures)
-   [常數](#constants)

## <a name="overviews"></a>概觀



| 主題                                              | 目錄                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於通用控制項](common-controls-intro.md) | 通用控制項是由通用控制項程式庫所執行的一組視窗，也就是 Windows 作業系統隨附的 DLL。<br/> |
| [通用控制項常見問題](cc-faq.yml)                  | 此常見問題提供有關通用控制項的一些常見問題解答。<br/>                                                                           |



 

## <a name="functions"></a>函式



| 主題                                                        | 目錄                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoReaderMode**](doreadermode.md)                         | 在視窗中啟用讀取器模式。<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**DPA \_ 複製**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_clone)                              | 複製動態指標陣列 (DPA) 。<br/>                                                                                                                                                                                                                                                                                                                        |
| [**DPA \_ 建立**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create)                            | 建立 DPA。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**DPA \_ CreateEx**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex)                        | 使用指定的大小和堆積位置，建立 DPA。<br/>                                                                                                                                                                                                                                                                                                    |
| [**DPA \_ DeleteAllPtrs**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteallptrs)              | 移除 DPA 的所有專案，並據以縮減 DPA。<br/>                                                                                                                                                                                                                                                                                                    |
| [**DPA \_ DeletePtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteptr)                      | 從 DPA 移除專案。 必要時會壓縮 DPA 以容納移除的專案。<br/>                                                                                                                                                                                                                                                                        |
| [**DPA 損 \_ 毀**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroy)                          | 釋出動態指標陣列 (DPA) 。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**DPA \_ DestroyCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroycallback)          | 在 DPA 的每個專案上呼叫 *pfnCB* ，然後釋出 dpa。<br/>                                                                                                                                                                                                                                                                                                    |
| [**DPA \_ EnumCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_enumcallback)                | 逐一查看動態指標陣列 (DPA) ，並在每個專案上呼叫 *pfnCB* 。 <br/>                                                                                                                                                                                                                                                                                |
| [**DPA \_ GetPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptr)                            | 從 DPA 取得專案。<br/>                                                                                                                                                                                                                                                                                                                                         |
| [**DPA \_ GetPtrIndex**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrindex)                  | 取得在 DPA 中找到之相符專案的索引。<br/>                                                                                                                                                                                                                                                                                                                |
| [**DPA \_ GetSize**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getsize)                          | 取得 DPA 的大小。<br/>                                                                                                                                                                                                                                                                                                                                          |
| [**DPA \_ 成長**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_grow)                                | 變更 DPA 中的指標數目。<br/>                                                                                                                                                                                                                                                                                                                         |
| [**DPA \_ InsertPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr)                      | 在 DPA 中的指定位置插入新專案。 必要時，會展開 DPA 以容納新專案。<br/>                                                                                                                                                                                                                                                 |
| [**DPA \_ LoadStream**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream)                    | 藉由呼叫指定的回呼函式來讀取每個專案，從資料流程載入 DPA。<br/>                                                                                                                                                                                                                                                                     |
| [**DPA \_ 合併**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)                              | 結合兩個 DPAs 的內容。<br/>                                                                                                                                                                                                                                                                                                                               |
| [**DPA \_ SaveStream**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream)                    | 藉由寫出標頭，然後呼叫指定的回呼函式來寫入每個專案，將 DPA 儲存至資料流程。<br/>                                                                                                                                                                                                                                       |
| [**DPA \_ 搜尋**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search)                            | 在 DPA 中尋找專案。<br/>                                                                                                                                                                                                                                                                                                                                          |
| [**DPA \_ SetPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_setptr)                            | 指派值給 DPA 中的專案。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**DPA \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort)                                | 將動態指標陣列中的專案排序 (DPA) 。<br/>                                                                                                                                                                                                                                                                                                                |
| [**DrawShadowText**](/windows/desktop/api/Commctrl/nf-commctrl-drawshadowtext)                     | 繪製具有陰影的文字。<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DrawTextExPrivWrap**](drawtextexprivwrap.md)             | 在指定的矩形中繪製格式化的文字。 此函數會包裝對 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)的呼叫。<br/>                                                                                                                                                                                                                                                 |
| [**DrawTextWrap**](drawtextwrap.md)                         | 在指定的矩形中繪製格式化的文字。 它會根據指定的方法將文字格式化 (展開索引標籤、對齊字元、斷線等) 。 此函數會包裝對 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)的呼叫。<br/>                                                                                                                           |
| [**DSA \_ 複製**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_clone)                              |  (DSA) 複製動態結構陣列。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**DSA \_ 建立**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_create)                            | 建立 DSA。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**DSA \_ DeleteAllItems**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteallitems)            | 從 DSA 刪除所有專案。<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DSA \_ DeleteItem**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteitem)                    | 從 DSA 刪除專案。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**DSA 損 \_ 毀**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroy)                          | 釋出 DSA。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**DSA \_ DestroyCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroycallback)          | 逐一查看 DSA，並在每個專案上呼叫指定的回呼函數。 到達陣列的結尾時，就會釋放 DSA。<br/>                                                                                                                                                                                                                                |
| [**DSA \_ EnumCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_enumcallback)                | 逐一查看 DSA，並在每個專案上呼叫 *pfnCB* 。 <br/>                                                                                                                                                                                                                                                                                                        |
| [**DSA \_ GetItem**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitem)                          | 從 DSA 取得元素。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**DSA \_ GetItemPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemptr)                    | 從 DSA 取得元素的指標。<br/>                                                                                                                                                                                                                                                                                                                         |
| [**DSA \_ GetSize**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getsize)                          | 取得 DSA 的大小。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**DSA \_ InsertItem**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem)                    | 將新專案插入 DSA。 如有必要，DSA 會展開以容納新專案。<br/>                                                                                                                                                                                                                                                                        |
| [**DSA \_ SetItem**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_setitem)                          | 設定 DSA 中元素的內容。<br/>                                                                                                                                                                                                                                                                                                                        |
| [**DSA \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort)                                | 排序 DSA 中的專案。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ExtTextOutWrap**](exttextoutwrap.md)                     | 使用目前選取的字型、背景色彩和文字色彩來繪製文字。 您可以選擇性地提供要用於剪切、不透明度或兩者的維度。 此函數會包裝對 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)的呼叫。<br/>                                                                                                                                 |
| [**GetEffectiveClientRect**](/windows/desktop/api/Commctrl/nf-commctrl-geteffectiveclientrect)     | 計算工作區中包含所有指定控制項的矩形維度。 <br/>                                                                                                                                                                                                                                                           |
| [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)                     | 取得特定進程的通用控制項目前所使用的語言。 <br/>                                                                                                                                                                                                                                                                             |
| [**GetTextExtentPoint32Wrap**](gettextextentpoint32wrap.md) | 計算指定文字字串的寬度和高度。 此函數會包裝對 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)的呼叫。<br/>                                                                                                                                                                                                                   |
| [**函式**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)             | 註冊並初始化特定的通用控制項視窗類別。 此函式已過時。 新的應用程式應該使用 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數。 <br/>                                                                                                                                                                      |
| [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)         | 從通用控制項 DLL 註冊特定的通用控制項類別。 <br/>                                                                                                                                                                                                                                                                                          |
| [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)                   | 讓應用程式指定要搭配與系統語言不同的通用控制項使用的語言。 <br/>                                                                                                                                                                                                                                    |
| [**LoadIconMetric**](/windows/desktop/api/Commctrl/nf-commctrl-loadiconmetric)                     | 使用用戶端指定的系統度量載入指定的圖示資源。<br/>                                                                                                                                                                                                                                                                                           |
| [**LoadIconWithScaleDown**](/windows/desktop/api/Commctrl/nf-commctrl-loadiconwithscaledown)       | 載入圖示。 如果圖示不是標準大小，此函式會相應減少較大的影像，而不是相應放大較小的影像。<br/>                                                                                                                                                                                                                               |
| [**MirrorIcon**](mirroricon.md)                             | 反轉 (鏡像) 圖示，使其在鏡像裝置內容上正確顯示。<br/>                                                                                                                                                                                                                                                                      |
| [**PFNDACOMPARE**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare)                         | 定義 [**DSA \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort)所使用之比較函式的原型。<br/>                                                                                                                                                                                                                                                                            |
| [**PFNDACOMPARECONST**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompareconst)               | 當要比較的專案是常數物件時，為 [**DSA \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort) 所使用的比較函式定義原型。<br/>                                                                                                                                                                                                                         |
| [**PFNDAENUMCALLBACK**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback)               | 定義 DSA 和 DPA 函式所使用之回呼函數的原型。<br/>                                                                                                                                                                                                                                                                                   |
| [**PFNDAENUMCALLBACKCONST**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallbackconst)     | 當相關專案是指向常數資料的指標時，定義 DSA 和 DPA 函式所使用之回呼函數的原型。<br/>                                                                                                                                                                                                                             |
| [**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))                  | 定義 [**dpa \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort) 和 [**dpa \_ 搜尋**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search)所使用之比較函式的原型。<br/>                                                                                                                                                                                                                                      |
| [**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))        | 定義在要比較的專案是常數物件時，由 [**dpa \_ 排序**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort) 或 [**dpa \_ 搜尋**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search) 所使用的比較函式的原型。<br/>                                                                                                                                                                                    |
| [**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))        | 定義 [**DPA \_ EnumCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_enumcallback)所使用之回呼函數的原型。<br/>                                                                                                                                                                                                                                                           |
| [**PFNDPAMERGE**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge)                           | 定義 [**DPA \_ 合併**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)所使用之合併函式的原型。<br/>                                                                                                                                                                                                                                                                            |
| [**PFNDPAMERGECONST**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamergeconst)                 | 使用常數值來定義 [**DPA \_ 合併**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)所使用之合併函式的原型。<br/>                                                                                                                                                                                                                                                     |
| [**PFNDPASTREAM**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream)                         | 定義 [**dpa \_ LoadStream**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream) 和 [**dpa \_ SaveStream**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream)所使用之回呼函式的原型。<br/>                                                                                                                                                                                                                 |
| [**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))        | 定義 [**DSA \_ DestroyCallback**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroycallback)所使用之回呼函數的原型。<br/>                                                                                                                                                                                                                                                     |
| [*ReaderScroll*](readerscroll.md)                           | 應用程式定義的回呼函式，當滑鼠指標在已宣告為使用中捲動區域的讀取器強制回應視窗部分內移動時，就會使用這個函數。<br/>                                                                                                                                                                                  |
| [**ShowHideMenuCtl**](/windows/desktop/api/Commctrl/nf-commctrl-showhidemenuctl)                   | 設定或移除指定的功能表項目核取記號屬性，並顯示或隱藏對應的控制項。 函式會在指定的功能表項目中加入核取記號（如果沒有的話），然後顯示對應的控制項。 如果功能表項目已經有核取記號，則函式會移除核取記號，並隱藏對應的控制項。 <br/> |
| [**Str \_ GetPtr**](str-getptr.md)                            | 將字串從一個緩衝區複製到另一個緩衝區。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**Str \_ SetPtrW**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-str_setptrw)                          | 將 *ppszCurrent* 設定為 *pszNew* 的複本，並視需要釋出先前的值。<br/>                                                                                                                                                                                                                                                                             |
| [*TranslateDispatch*](translatedispatch.md)                 | [**DoReaderMode**](doreadermode.md)函式的用戶端使用它來攔截並明確處理以讀取器強制回應視窗的捲動區域為目標的任何 windows 訊息。 這是應用程式定義的回呼函數。<br/>                                                                                                                     |



 

## <a name="macros"></a>巨集



| 主題                                                   | 目錄                                                                                                                                                    |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DPA \_ AppendPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_appendptr)                 | 在 DPA 的結尾插入新專案。<br/>                                                                                                          |
| [**DPA \_ FastDeleteLastPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_fastdeletelastptr) | 刪除 DPA 的最後一個指標。<br/>                                                                                                             |
| [**DPA \_ FastGetPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_fastgetptr)               | 取得 DPA 中指定之指標的值。<br/>                                                                                              |
| [**DPA \_ GetPtrCount**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrcount)             | 取得 DPA 中的指標數目。 <br/>                                                                                                           |
| [**DPA \_ GetPtrPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrptr)                 | 取得 DPA 內部指標陣列的指標。<br/>                                                                                         |
| [**DPA \_ SetPtrCount**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_setptrcount)             | 設定 DPA 中的指標數目。<br/>                                                                                                            |
| [**DPA \_ SortedInsertPtr**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sortedinsertptr)     | 在指定的現有專案之前或之後插入新專案。<br/>                                                                                    |
| [**DSA \_ AppendItem**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_appenditem)               | 將新專案附加至 DSA 的結尾。<br/>                                                                                                          |
| [**DSA \_ GetItemCount**](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemcount)           | 取得 DSA 中的專案數。<br/>                                                                                                               |
| [**轉寄 \_ WM \_ 通知**](/windows/desktop/api/Commctrl/nf-commctrl-forward_wm_notify)        | 傳送或張貼 [**WM \_ 通知**](wm-notify.md) 訊息。 <br/>                                                                                     |
| [**處理 \_ WM \_ 通知**](/windows/desktop/api/Commctrl/nf-commctrl-handle_wm_notify)          | 呼叫處理 [**WM \_ 通知**](wm-notify.md) 訊息的函式。 <br/>                                                                    |
| [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask)  | 準備狀態影像的索引，讓樹狀檢視控制項或清單視圖控制項可以使用索引來取得專案的狀態影像。 <br/> |



 

## <a name="messages"></a>訊息



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CCM \_ DPISCALE**](ccm-dpiscale.md)                 | 在 [樹狀檢視控制項](tree-view-controls.md)、 [清單視圖控制項](list-view-control-reference.md)、 [ComboBoxEx 控制項](comboboxex-controls.md)、 [標題控制項](header-controls.md)、 [按鈕](buttons.md)、 [工具列控制項](toolbar-controls-overview.md)、 [動畫控制項](animation-control-overview.md)和 [影像清單](image-lists.md)中，啟用每英寸的自動大點 (DPI) 縮放比例。 <br/> |
| [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) | 取得控制項的 Unicode 字元格式旗標。 <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**CCM \_ GETVERSION**](ccm-getversion.md)             | 取得最新的 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息之控制項集的版本號碼。<br/>                                                                                                                                                                                                                                                                                                          |
| [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/>                                                                                                                                                                                                                               |
| [**CCM \_ SETVERSION**](ccm-setversion.md)             | 此訊息是用來通知控制項您預期會有與特定版本相關聯的行為。<br/>                                                                                                                                                                                                                                                                                                       |
| [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md)     | 設定控制項的視覺化樣式。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ 通知**](wm-notify.md)                       | 當事件發生時，由通用控制項傳送至其父視窗，或控制項需要一些資訊。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md)           | 判斷視窗是否接受 [**WM \_ 通知**](wm-notify.md) 通知訊息中的 ANSI 或 Unicode 結構。 [**WM \_NOTIFYFORMAT**](wm-notifyformat.md) 訊息會從通用控制項傳送至其父視窗，以及從父視窗傳送至通用控制項。<br/>                                                                                                                                        |



 

## <a name="notifications"></a>通知



| 主題                                                   | 目錄                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ 字元](nm-char.md)                                 | 當處理字元鍵時，控制項會傳送 [NM \_ 字元](nm-char.md) 通知碼。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                 |
| [NM \_ CUSTOMDRAW](nm-customdraw.md)                     | 通知控制項的父視窗有關自訂繪圖作業的相關資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                    |
| [NM \_ CUSTOMTEXT](nm-customtext.md)                     | 通知控制項的父視窗有關自訂文字作業的相關資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                       |
| [NM \_ FONTCHANGED](nm-fontchanged.md)                   | 當控制項變更字型時，由清單視圖控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                      |
| [NM \_ GETCUSTOMSPLITRECT](nm-getcustomsplitrect.md)     | 由按鈕控制項傳送至其父系，以取得組成分割按鈕的兩個矩形的度量。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                      |
| [NM \_ 停留](nm-hover.md)                               | 當滑鼠停留在專案上時，由控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                 |
| [NM \_ KEYDOWN](nm-keydown.md)                           | 當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                 |
| [NM \_ KILLFOCUS](nm-killfocus.md)                       | 通知控制項的父視窗，控制項已遺失輸入焦點。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                         |
| [NM \_ LDOWN](nm-ldown.md)                               | 通知控制項的父視窗，滑鼠左鍵已按下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                       |
| [NM \_ NCHITTEST](nm-nchittest.md)                       | 當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                               |
| [NM \_ OUTOFMEMORY](nm-outofmemory.md)                   | 通知控制項的父視窗，控制項無法完成作業，因為沒有足夠的可用記憶體。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>    |
| [NM \_ RDOWN](nm-rdown.md)                               | 目前不支援。<br/>                                                                                                                                                                                                        |
| [NM \_ RELEASEDCAPTURE](nm-releasedcapture.md)           | 通知控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                       |
| [NM \_ RETURN](nm-return.md)                             | 通知控制項的父視窗，控制項具有輸入焦點，而且使用者已按下 ENTER 鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                  |
| [NM \_ SETCURSOR](nm-setcursor.md)                       | 通知控制項的父視窗，控制項正在設定資料指標以回應 [NM \_ SETCURSOR](nm-setcursor.md) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [NM \_ SETFOCUS](nm-setfocus.md)                         | 通知控制項的父視窗，控制項已收到輸入焦點。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                     |
| [NM \_ THEMECHANGED](nm-themechanged.md)                 | 通知控制項的父視窗，主題已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                         |
| [NM \_ TOOLTIPSCREATED](nm-tooltipscreated.md)           | 通知控制項的父視窗，控制項已建立工具提示控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                    |
| [NM \_ TVSTATEIMAGECHANGING](nm-tvstateimagechanging.md) | 由樹狀檢視控制項傳送至其父視窗，表示狀態影像正在變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                     |



 

## <a name="structures"></a>結構



| 主題                                                     | 目錄                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)                        | 包含在工具列或 Rebar 中繪製按鈕的資訊。 <br/>                                                                                                                      |
| [**DPASTREAMINFO**](/windows/desktop/api/dpa_dsa/ns-dpa_dsa-dpastreaminfo)                    | 包含 [**PFNDPASTREAM**](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream) 回呼函數使用的資料流程專案。 <br/>                                                                                                  |
| [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) | 攜帶用來從動態連結程式庫載入通用控制項類別 (DLL) 的資訊。 此結構會與 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數搭配使用。 <br/> |
| [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)                                  | 包含用於字元通知訊息的資訊。 <br/>                                                                                                                             |
| [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo)    | 包含分割按鈕的兩個矩形的相關資訊。 與 [NM \_ GETCUSTOMSPLITRECT](nm-getcustomsplitrect.md) 通知一起傳送。<br/>                                             |
| [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext)                      | 包含用於自訂文字通知的資訊。 <br/>                                                                                                                                    |
| [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)                                    | 包含通知訊息的相關資訊。<br/>                                                                                                                                           |
| [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey)                                    | 包含用於金鑰通知訊息的資訊。 <br/>                                                                                                                                   |
| [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)                                | 包含用於滑鼠通知訊息的資訊。 <br/>                                                                                                                                 |
| [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)                  | 包含與 [TBN \_ getobject](tbn-getobject.md)、 [TCN \_ getobject](tcn-getobject.md)和 [PSN \_ getobject](psn-getobject.md) 通知碼搭配使用的資訊。 <br/>                    |
| [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated)            | 包含與 [NM \_ TOOLTIPSCREATED](nm-tooltipscreated.md) 通知程式碼搭配使用的資訊。 <br/>                                                                                             |
| [**READERMODEINFO**](readermodeinfo.md)                  | 包含初始化 [**DoReaderMode**](doreadermode.md) 函數所需的資訊。<br/>                                                                                               |



 

## <a name="constants"></a>常數



| 主題                                               | 目錄                                                                                                                                               |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CDRF 常數](cdrf-constants.md)                | 這些常數會由控制項用來作為傳回值，以回應 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。<br/>             |
| [樣式](common-control-styles.md)                 | 本節列出常見的控制項樣式。 除非有注明，否則這些樣式適用于標題控制項、工具列控制項和狀態視窗。 <br/> |
| [視窗類別](common-control-window-classes.md) | 此區段會列出通用控制項程式庫所提供的視窗類別名稱。 <br/>                                                          |



 

 

