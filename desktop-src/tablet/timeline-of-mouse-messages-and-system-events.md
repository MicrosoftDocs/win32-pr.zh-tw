---
description: 執行指定的動作時， \_ 應用程式幾乎會立即傳送和接收系統事件 (前面加上 ISG) 。
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: 滑鼠訊息和系統事件的時間軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635147b3f30b8746c75901de78336102ac8d1b41a685919c27f990496f5f225d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819600"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>滑鼠訊息和系統事件的時間軸

執行指定的動作時， \_ 應用程式幾乎會立即傳送和接收系統事件 (前面加上 ISG) 。 在執行動作時，會傳送以 WM) 為首碼 (的滑鼠訊息 \_ ，而且應用程式會在事件由 Microsoft Windows 訊息服務處理所需的時間之後收到。 此外， **CursorDown** 和 **CursorUp** 是從畫筆硬體接收的畫筆事件。 當 tablet 畫筆觸及螢幕，以及從螢幕中移除時，就會傳送它們。

畫筆事件和滑鼠訊息不會進行同步處理。 不保證對應的滑鼠訊息和畫筆事件會以特定順序發生。 下圖顯示所傳送之系統和滑鼠事件的預期（但不一定是可預測的）順序。 請注意，在圖表中偵測到系統手勢事件時會延遲滑鼠事件。

![畫筆輸入的系統和滑鼠事件的預期順序](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>重要的實作為考慮

在開發滑鼠訊息和系統事件時，請考慮下列事項：

-   無論畫筆或滑鼠是否使用，畫筆事件和滑鼠訊息都會傳送至應用程式。
-   如果您的應用程式同時接聽畫筆和滑鼠訊息，則很難預測訊息的關聯性，因此是最終行為。 畫筆事件和滑鼠訊息不會進行同步處理。 不保證對應的滑鼠訊息和畫筆事件 (例如，WM \_ LBUTTONDOWN、 **\_ ISG** 點、wm \_ LBUTTONDBLCLK 和 **ISG \_ DBLTAP**) 將依特定順序進行。 這些訊息之間的關聯性相當複雜。
-   建議您不要在相同的應用程式功能中混用和比對滑鼠和畫筆事件。 例如，回應 **CursorDown** 和 **MouseUp** 的應用程式功能可能不會如預期般運作，或是與未來的 Tablet PC SDK 版本一樣。
-   針對 [按住] 事件順序，如果使用者在序列完成之前拖曳 tablet 畫筆，則會傳送的事件對應至左方拖曳。 例如，當拖曳開始時，會傳送 **ISG \_ 拖曳** 和 WM \_ LBUTTONDOWN。 當畫筆最後會提起時，會傳送 **CursorUp** 和 WM \_ LBUTTONUP。 系統筆勢事件可能不會立即引發，因為它必須判斷發生何種類型的事件。
-   使用 tablet 畫筆的點一下，通常比按兩下滑鼠的方式更不精確。 這是利用 tablet 畫筆來執行兩點的固有本質。 由於使用者必須提起 tablet 畫筆以執行點一下，所以點擊之間的時間通常會大於按兩下時的對應時間。 此外，這兩個 tablet 畫筆的點擊率很可能會在螢幕座標上發生，而不是在兩次按下滑鼠的情況下執行。 為了因應這種情況，Windows XP Tablet PC Edition 具有設定，可讓您在兩個點間的間隔點之間，與滑鼠按兩下分開的點點。 這些設定可以在主控台中的 Tablet 和 Pen 設定中調整。

基於這些考慮，應用程式應該只接聽一組訊息，而非兩者。 如果您要建立已啟用畫筆的應用程式，只需聆聽系統和畫筆訊息。 這些訊息是可預測的，且適用于 tablet 畫筆。 如果您要建立的應用程式未啟用畫筆，請只聆聽滑鼠訊息。

 

 



