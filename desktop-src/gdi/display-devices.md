---
description: 在繪製之前，系統必須為繪圖作業準備顯示裝置。
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: 顯示裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972701"
---
# <a name="display-devices"></a>顯示裝置

在繪製之前，系統必須為繪圖作業準備顯示裝置。 顯示裝置內容會定義一組繪圖物件和其相關聯的屬性，以及影響輸出的圖形模式。 系統會準備每個顯示裝置內容，以便輸出至視窗、設定視窗的繪圖物件、色彩和模式，而不是顯示裝置。 當應用程式透過呼叫 GDI 函式提供顯示裝置內容時，GDI 會使用內容中的資訊在指定的視窗中產生輸出，而不侵其他視窗或螢幕的其他部分。

系統提供五種類型的顯示裝置內容。



| 類型                                           | 意義                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [常見](common-display-device-contexts.md)   | 允許在指定視窗的工作區中繪製。                                                                                                        |
| [class](class-display-device-contexts.md)     | 允許在指定視窗的工作區中繪製。                                                                                                        |
| [parent](parent-display-device-contexts.md)   | 允許在視窗中的任何位置繪製。 雖然父裝置內容也允許在父視窗中繪製，但無法以這種方式使用。 |
| [私人](private-display-device-contexts.md) | 允許在指定視窗的工作區中繪製。                                                                                                        |
| [視窗](window-display-device-contexts.md)   | 允許在視窗中的任何位置繪製。                                                                                                                          |



 

系統會根據該視窗類別樣式中所指定的顯示裝置內容類型，提供通用、類別、父系或私用裝置內容至視窗。 系統只會在應用程式明確要求時（例如，藉由呼叫 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式），提供視窗裝置內容。 在所有情況下，應用程式都可以使用 [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) 函式來判斷顯示 DC 目前表示的視窗。

本節提供下列主題的相關資訊。

-   [顯示裝置內容快取](display-device-context-cache.md)
-   [顯示裝置內容預設值](display-device-context-defaults.md)
-   [一般顯示裝置內容](common-display-device-contexts.md)
-   [私用顯示裝置內容](private-display-device-contexts.md)
-   [父代顯示裝置內容](parent-display-device-contexts.md)
-   [類別顯示裝置內容](class-display-device-contexts.md)
-   [視窗顯示裝置內容](window-display-device-contexts.md)
-   [父代顯示裝置內容](parent-display-device-contexts.md)

 

 



