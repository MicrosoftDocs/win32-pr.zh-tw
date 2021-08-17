---
title: 關於 ComboBoxEx 控制項
description: ComboBoxEx 控制項是下拉式方塊控制項，可提供專案影像的原生支援。
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831834"
---
# <a name="about-comboboxex-controls"></a>關於 ComboBoxEx 控制項

ComboBoxEx 控制項是下拉式方塊控制項，可提供專案影像的原生支援。 為了讓專案影像易於存取，控制項提供影像清單支援。 藉由使用這個控制項，您可以提供下拉式方塊的功能，而不需要手動繪製專案圖形。

本主題包含下列各節。

-   [建立 ComboBoxEx 控制項](#creating-comboboxex-controls)
-   [ComboBoxEx 控制項樣式](#comboboxex-control-styles)
-   [ComboBoxEx 控制項專案](#comboboxex-control-items)
-   [回呼專案](#callback-items)
-   [ComboBoxEx 控制項影像清單](#comboboxex-control-image-lists)
-   [關於 ComboBoxEx 控制通知訊息](#about-comboboxex-control-notification-messages)
-   [ComboBoxEx 控制訊息轉送](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>建立 ComboBoxEx 控制項

實際上，ComboBoxEx 控制項會建立子下拉式方塊，並根據指派的影像清單，為您執行擁有者繪製工作。 因此， [**\_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式是隱含的，而且在建立控制項時並不需要使用它。 因為影像清單是用來提供專案圖形，所以無法使用 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式。

ComboBoxEx 控制項必須透過呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來初始化， \_ \_ 在隨附的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定 ICC USEREX 類別。

您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立 ComboBoxEx 控制項，並指定 [**WC \_ ComboBoxEx**](common-control-window-classes.md) 做為視窗類別。 如上面所述呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式時，會註冊類別。

系統會建立不含預設影像清單的 ComboBoxEx 控制項。 若要使用專案影像，您必須建立 ComboBoxEx 控制項的影像清單，並使用 [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) 訊息將它指派給控制項。 如果您未將影像清單指派給 ComboBoxEx 控制項，控制項只會顯示專案文字。

## <a name="comboboxex-control-styles"></a>ComboBoxEx 控制項樣式

ComboBoxEx 控制項僅支援下列 ComboBox 樣式：

-   CBS \_ 簡單
-   CBS \_ 下拉式清單
-   CBS \_ DROPDOWNLIST
-   WS \_ 子系

另外還有數個 [ComboBoxEx 控制項延伸樣式](comboboxex-control-extended-styles.md) ，只供 ComboBoxEx 使用。

> [!Note]  
> 在某些情況下， [**CBS \_ 簡單**](combo-box-styles.md) 樣式可能無法正常運作。

 

由於 ComboBoxEx 控制項會根據指派的影像清單，為您執行「擁有者」繪製工作，因此會隱含 [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式; 您在建立控制項時不需要使用它。 因為影像清單是用來提供專案圖形，所以無法使用 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式。 ComboBoxEx 控制項也支援 [ComboBoxEx 控制項擴充樣式](comboboxex-control-extended-styles.md) ，以提供額外的功能。

## <a name="comboboxex-control-items"></a>ComboBoxEx 控制項專案

ComboBoxEx 控制項會使用 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構來維護專案資訊。 此結構包含專案索引、影像索引 (正常、選取狀態和重迭) 、縮排值、文字字串和專案特定值的成員。

ComboBoxEx 控制項可讓您輕鬆地透過訊息存取和操作專案。 若要加入或刪除專案，請傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 或 [**CBEM \_ DELETEITEM**](cbem-deleteitem.md) 訊息。 您可以使用 [**CBEM \_ SETITEM**](cbem-setitem.md) 訊息來修改目前在控制項中的專案。

## <a name="callback-items"></a>回呼專案

ComboBoxEx 控制項支援回呼專案屬性。 當您使用 [**CBEM \_ INSERTITEM**](cbem-insertitem.md)將專案新增至控制項時，您可以將它指定為回呼專案。 當您將值指派給專案的 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構時，您必須指定適當的回呼旗標值。 以下是 **COMBOBOXEXITEM** 結構成員及其對應的回呼旗標值。



| 成員             | 回呼值      |
|--------------------|---------------------|
| **pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | 我 \_ IMAGECALLBACK    |
| **iSelectedImage** | 我 \_ IMAGECALLBACK    |
| **iOverlay**       | 我 \_ IMAGECALLBACK    |
| **iIndent**        | 我 \_ INDENTCALLBACK   |



 

控制項將會透過傳送 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 通知碼來要求回呼專案的相關資訊。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 當您的應用程式處理此訊息時，它必須提供控制項要求的資訊。 如果您將隨附 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **mask** 成員設定為 CBEIF \_ DI \_ SETITEM，控制項將會儲存專案資料，而且不會再次要求它。

## <a name="comboboxex-control-image-lists"></a>ComboBoxEx 控制項影像清單

如果您想要讓 ComboBoxEx 控制項顯示具有專案的圖示，您必須提供影像清單。 ComboBoxEx 控制項最多支援三個專案的影像-一個用於其選取狀態、一個用於其 nonselected 狀態，另一個用於重迭影像。 使用 [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) 訊息，將現有的影像清單指派給 ComboBoxEx 控制項。

[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構包含成員，這些成員代表每個影像清單 (選取、未選取和重迭) 的影像索引。 針對每個專案，設定這些成員以顯示所需的影像。 不需要為每個影像類型指定影像索引。 您可以依需要混合和比對影像類型，但請一律設定 **COMBOBOXEXITEM** 結構的 **遮罩** 成員，以指出正在使用哪些成員。 控制項會忽略未標示為有效的成員。

> [!Note]  
> 如果您使用 [**CBS \_ 簡單**](combo-box-styles.md) 樣式，則不會顯示圖示。

 

## <a name="about-comboboxex-control-notification-messages"></a>關於 ComboBoxEx 控制通知訊息

ComboBoxEx 控制項會傳送通知訊息，以在本身或要求回呼專案資訊中報告變更。 控制項的父系會從包含在 ComboBoxEx 控制項內的下拉式方塊接收所有的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。 ComboBoxEx 控制項會使用 [**WM \_ 通知**](wm-notify.md) 訊息傳送自己的通知。 因此，控制項的擁有者必須準備好處理這兩種形式的通知訊息。

以下是透過 [**WM \_ 通知**](wm-notify.md) 訊息傳送的 ComboBoxEx 特定通知碼。



| 通知                              | **說明**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | 通知使用者已啟動下拉式清單，或按一下控制項的編輯方塊。                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | 表示使用者已從下拉式清單中選取專案，或已結束編輯方塊中的編輯作業。 |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | 報告已刪除專案。                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | 要求專案屬性的相關資訊。                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | 指出專案已插入控制項中的信號。                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>ComboBoxEx 控制訊息轉送

以下是 ComboBoxEx 控制項轉送至其子下拉式方塊的標準下拉式方塊訊息。 在轉送訊息之前或之後，ComboBoxEx 控制項可能會處理其中某些訊息。

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
-   [**CB \_ GETCURSEL**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ RESETCONTENT**](cb-resetcontent.md)
-   [**CB \_ SETCURSEL**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

以下是 ComboBoxEx 控制項轉送至其父視窗的 windows 訊息：

-   [**WM \_命令**](/windows/desktop/menurc/wm-command) (其中包含所有 CBN \_ 通知。 ) 
-   [**WM \_ 通知**](wm-notify.md)

 

 