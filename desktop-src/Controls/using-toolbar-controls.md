---
title: 使用工具列控制項
description: 本主題包含在應用程式中使用工具列控制項的執行詳細資料與範例程式碼。
ms.assetid: 5e52049c-58b4-478c-92ee-ea2f16534f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a41c5842547e0b342657b6c694e38f59a38538
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812324"
---
# <a name="using-toolbar-controls"></a>使用工具列控制項

本主題包含在應用程式中使用工具列控制項的執行詳細資料與範例程式碼。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何建立工具列](create-toolbars.md)<br/>                                           | 若要建立工具列，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 [**TOOLBARCLASSNAME**](common-control-window-classes.md) 視窗類別。 產生的工具列一開始不會包含任何按鈕。 使用 [**tb \_ ADDBUTTONS**](tb-addbuttons.md) 或 [**tb \_ INSERTBUTTON**](tb-insertbutton.md) 訊息，將按鈕新增至工具列。 在所有專案和字串都插入控制項之後，您必須傳送 [**TB 的 \_ AUTOSIZE**](tb-autosize.md) 訊息，讓工具列根據其內容重新計算其大小。 <br/>        |
| [如何建立垂直工具列](create-vertical-toolbars.md)<br/>                         | 建立垂直工具列的關鍵是在視窗樣式中 [**包含 \_ 垂直 CCS**](common-control-styles.md) ，以及為每個按鈕設定 [**TBSTATE \_ 換行**](toolbar-button-states.md) 樣式。 <br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [如何動態標記工具列按鈕](dynamically-label-toolbar-buttons.md)<br/>       | 您可以使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 訊息，將文字指派給現有的按鈕。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [如何顯示按鈕的工具提示](display-tooltips-for-buttons.md)<br/>                 | 當您指定 [**TBSTYLE \_ 工具提示**](toolbar-control-and-button-styles.md) 樣式時，工具列會建立和管理工具提示控制項。 工具提示控制項是隱藏的，只有在使用者將指標移到工具列按鈕上方，並將其保留大約一秒時才會出現。 <br/>                                                                                                                                                                                                                                                                                     |
| [如何處理下拉按鈕](handle-drop-down-buttons.md)<br/>                         | 下拉式按鈕可以提供選項清單給使用者。 若要建立此按鈕樣式，請指定 [ [**BTNS \_ ] 下拉式**](toolbar-control-and-button-styles.md) 樣式 (也稱為 [ [**TBSTYLE \_ ] 下拉式清單**](toolbar-control-and-button-styles.md) ，以相容于舊版的通用控制項) 。 若要以箭號顯示下拉式按鈕，您也必須透過傳送 [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)訊息來設定 [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md)工具列樣式。 <br/> |
| [如何自訂工具列](customize-toolbars.md)<br/>                                     | 大部分以 Windows 為基礎的應用程式都使用工具列控制項，讓使用者能夠輕鬆存取程式功能。 不過，靜態工具列有一些缺點，像是空間太少，無法有效顯示所有可用的工具。 解決此問題的方法是讓應用程式的工具列成為使用者可自訂的。 然後，使用者可以選擇只顯示所需的工具，並以適合其個人工作型態的方式來組織它們。 <br/>                                                                                                                      |
| [如何在工具列中內嵌 Nonbutton 控制項](embed-nonbutton-controls-in-toolbars.md)<br/> | 工具列僅支援按鈕;因此，如果您的應用程式需要不同類型的控制項，您必須建立子視窗。 下圖顯示具有內嵌編輯控制項的工具列。 <br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| [如何搭配使用熱追蹤與工具列](use-hot-tracking-with-toolbars.md)<br/>             | 當滑鼠指標停留在專案上時，專案會變成經常性存取。 如果啟用熱追蹤，則會反白顯示熱專案。 使用 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式建立的工具列，或使用 [視覺化樣式](themes-overview.md)的工具列，預設支援熱追蹤。 <br/>                                                                                                                                                                                                                                                                  |
| [如何建立 Internet Explorer 樣式的工具列](cc-faq-ietoolbar.yml)<br/>                | Windows Internet Explorer 的主要使用者介面功能之一，就是工具列。 它不僅可讓使用者存取廣泛的功能，還可讓使用者根據個人喜好來自訂版面配置。 <br/>                                                                                                                                                                                                                                                                                                                                                                |
| [如何建立 Internet Explorer 樣式的功能表列](cc-faq-iemenubar.yml)<br/>               | 乍看之下，Microsoft Internet Explorer 5 和更新版本中的功能表列看起來類似于標準功能表。 但是，當您開始使用它時，它看起來會非常不同。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

 

