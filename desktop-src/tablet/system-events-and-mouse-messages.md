---
description: 您的應用程式藉由傳送 Microsoft Windows 滑鼠訊息和系統事件來合併 tablet 畫筆的最佳設計和使用。
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: 系統事件和滑鼠訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971633"
---
# <a name="system-events-and-mouse-messages"></a>系統事件和滑鼠訊息

您的應用程式藉由傳送 Microsoft Windows 滑鼠訊息和系統事件來合併 tablet 畫筆的最佳設計和使用。 應用程式會接收每個畫筆移動或動作的兩組事件。 然後，應用程式會根據動作的內容，選擇要使用的適當事件。 Windows 滑鼠訊息適用于指向和選取活動，您應該將它們用於涉及使用者介面 (UI) 專案互動的活動。 畫筆事件適用于即時筆跡應用程式、畫筆動作和手寫。

> [!Note]  
> 無論畫筆或滑鼠是否使用，畫筆事件和滑鼠訊息都會傳送至應用程式。

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>區分畫筆輸入與滑鼠和觸控

當您的應用程式收到 (的滑鼠訊息時 \_ ，例如 WM LBUTTONDOWN) ，它可能會呼叫 [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) 函式來評估訊息是否源自畫筆或滑鼠裝置。

從 [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) 傳回的值必須針對0xFFFFFF00 進行遮罩檢查，然後再與0xFF515700 比較。 下列定義可以更清楚地提供：


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



如果比較結果為 true，則表示此滑鼠訊息是由 Tablet PC 畫筆或觸控式螢幕所產生。 在所有其他情況下，您可以假設此訊息是由滑鼠裝置所產生。

從 [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) 傳回的較低8位是變數。 在這些位中，7 (較低的7個) 用來表示資料指標識別碼、滑鼠為零，或畫筆識別碼的變數值。 此外，在 Windows Vista 中，第八個位（以0x80 遮罩）是用來區分觸控輸入與手寫筆輸入 (0 = 畫筆，1 = 觸控) 。

## <a name="supported-system-gestures"></a>支援的系統手勢

下表列出目前包含在 Windows XP Tablet PC Edition 中的系統手勢、詳述對應的畫筆動作和系統事件，以及顯示它們與傳統滑鼠動作之間的關聯性。



| 畫筆手勢                                  | 滑鼠動作                                                    | 畫筆手勢描述                                                                                                                                                                                                             | 事件訊息                                                                                                                       | 滑鼠訊息                                                                                                                        | 以 Windows 為基礎的應用程式行為                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 點選<br/>                               | 按滑鼠左鍵<br/>                                           | 使用畫筆來點擊畫面一次。<br/>                                                                                                                                                                                        | \_當畫筆被提起時，ISG 攻送。<br/>                                                                                         | \_當畫筆提起時，會傳送 wm LBUTTONDOWN 和 wm \_ LBUTTONUP。<br/>                                                                    | 從功能表或工具列選擇 [命令]，如果選擇命令，請採取動作、設定插入點 (IP) 、顯示選取的意見反應。<br/>                                                |
| 點兩下<br/>                        | 按兩下<br/>                                         | 快速連續按兩次畫面。<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP 會在第二點點下傳送， (向下) 。 ISG \_ 攻點一下傳送的事件。<br/>                                           | 每 \_ 秒傳送的 WM LBUTTONDBLCLK 會)  (下。 每 \_ 次只傳送 wm LBUTTONDOWN 和 wm \_ LBUTTONUP 時，只要點一下就會傳送 () 。<br/> | 選取 [word]、[開啟檔案] 或 [資料夾]。<br/>                                                                                                                                     |
| 長按<br/>                    | 以滑鼠右鍵按一下<br/>                                          | 點一下畫面並按住直到滑鼠圖示出現，然後提起畫筆以顯示快捷方式功能表。 應用程式可以選擇執行不同的動作，而不是在提起畫筆時顯示右鍵功能表。<br/> | \_當畫筆的長度已夠長時傳送 ISG HOLDENTER。 ISG \_ RIGHTTAP 會在畫筆被提起時傳送，然後按一下滑鼠右鍵。<br/> | 當 \_ \_)  (時，會在按一下滑鼠右鍵時，傳送 wm RBUTTONDOWN 和 wm RBUTTONUP。<br/>                                       | 顯示快捷方式功能表。<br/>                                                                                                                                                   |
| 保存<br/>                      | 按滑鼠左鍵<br/>                                           | 點一下畫面並按住滑鼠，直到滑鼠圖示出現並消失為止。 使用者很可能會在意外的情況下按下並按住，並且想要還原成隻需要點一下。<br/>                                                 | \_當畫筆被提起時，ISG 攻送。<br/>                                                                                         | \_ \_ 當畫筆被提起時，會傳送 wm LBUTTONDOWN 和 wm LBUTTONUP。<br/>                                                                 | 以滑鼠左鍵按一下很長的時間。 沒有滑鼠對等存在。 這是當使用者執行長時間的按住不放時。 事件會還原為點擊。<br/> |
| 拖曳<br/>                              | 左拖曳<br/>                                            | 點擊畫面以選取要移動的物件，然後在選取物件之後拖曳。<br/>                                                                                                                     | \_拖曳開始時，ISG 拖曳傳送。<br/>                                                                                          | \_當拖曳開始時傳送了 WM LBUTTONDOWN，後面接著一系列的滑鼠移動訊息，後面接著有 WM 的 \_ LBUTTONUP 事件。<br/> | 拖曳-select （如同在 Microsoft Word 中以 IP 開頭時）;選取多個單字;拖曳，如同在 Windows 中拖曳物件時一樣。滾動。<br/>                            |
| 按住 ctrl 鍵，然後拖曳<br/> | 以滑鼠右鍵拖曳<br/>                                           | 點擊螢幕以選取要移動的物件。 按住滑鼠圖示，然後拖曳以移動物件。 提起畫筆以顯示快捷方式功能表。<br/>                                                   | \_當畫筆已關閉一段時間時，會傳送 ISG HOLDENTER。 ISG \_ RIGHTDRAG 會在拖曳開始時傳送。<br/>                           | \_當拖曳開始時傳送了 wm RBUTTONDOWN，後面接著一系列的滑鼠移動訊息，後面接著一個 wm \_ RBUTTONUP 事件。<br/>     | 拖曳，如同在拖曳物件或選取專案之後，再按下內容功能表。<br/>                                                                                             |
| 畫筆停留<br/>                         | 滑鼠停留<br/>                                          | 將畫筆保持在與螢幕之間的距離穩定。<br/>                                                                                                                                                                 | 一 \_ 開始傳送的 ISG HOVERENTER 事件。 當停留間隔完成時，會 \_ 傳送 ISG HOVERLEAVEis。<br/>                           | 沒有對等的滑鼠訊息。<br/>                                                                                               | 顯示工具提示、向前復原效果，以及其他滑鼠停留行為。<br/>                                                                                                     |
| 空中搖動<br/>                      | 顯示 **TABLET PC 輸入面板**。 沒有滑鼠對等專案。<br/> | 從側邊快速移動畫筆，並在畫面的範圍內保存上述提示。<br/>                                                                                                                          | 事件不會傳遞至應用程式。<br/>                                                                                   | 沒有對等的滑鼠訊息。<br/>                                                                                               | 新的，適用于 Tablet PC。<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>指定手寫筆和觸控互動

根據預設，您的視窗將會接收所有系統手勢事件，並使用預設的互動模型。 此模型的某些部分可能會干擾您的應用程式，因此您可以藉由回應 WndProc 中的 [**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS 訊息**](wm-tablet-querysystemgesturestatus-message.md) ，選擇性地停用它們。

 

 
