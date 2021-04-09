---
title: 架構概觀
description: 此架構總覽提供適用于平板電腦和觸控技術的 Windows Touch API 內容，並說明其如何融入較大的 Windows 7 架構。
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch，架構總覽
- Windows Touch，操作
- Windows Touch，訊息
- Windows Touch，慣性
- Windows Touch，手勢
- 手勢，關於
- 操作，關於
- 慣性，關於
- 操作處理器，架構總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807113211d77f0aad0ed01fc24570d033063474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933255"
---
# <a name="architectural-overview"></a>架構概觀

此架構總覽提供適用于平板電腦和觸控技術的 Windows Touch API 內容，並說明其如何融入較大的 Windows 7 架構。

## <a name="messages-for-windows-touch-input-and-gestures"></a>Windows Touch 輸入和手勢的訊息

Windows Touch 的訊息功能是在執行期間接聽和解讀訊息而啟用。 下圖顯示如何從硬體產生訊息，然後由 Windows 7 傳送至應用程式。

![圖例顯示 windows 7 如何從多點觸控硬體將訊息傳送至應用程式](images/wm-multitouch-messaging.png)

在圖的最左邊的資料行中，觸控式硬體會接收來自使用者的輸入。 然後，驅動程式會在硬體和作業系統之間進行通訊。 接著，OS 會產生一個 [**wm \_ 觸控**](wm-touchdown.md) 或 [**wm \_ 手勢**](wm-gesture.md) 訊息，然後傳送至應用程式的 HWND。 然後，應用程式會根據訊息中封裝的資訊來更新 UI。

應用程式預設會接收手勢。 除非應用程式使用 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) 函式註冊 Windows Touch 輸入訊息，否則 ([**WM \_ 手勢**](wm-gesture.md) 訊息) 的手勢通知會由 Windows 建立並傳送至該應用程式視窗。 如果應用程式視窗註冊接收觸控訊息，Windows Touch 輸入 ([**WM \_ 觸控**](wm-touchdown.md) 訊息的通知) 會傳送至該應用程式視窗。 Windows Touch 和軌跡訊息在執行觸控或從應用程式視窗開始時的意義上是貪婪的，所有訊息都會傳送至該應用程式，直到手勢完成或主要觸控完成為止。

針對舊版支援，Windows 會在進行反升，然後傳送或張貼對應至手勢的適當訊息時，解讀 [**WM \_ 手勢**](wm-gesture.md) 訊息。 為了避免中斷舊版支援，請務必使用 DefWindowProc 轉送 WM \_ 手勢訊息。 [](/windows/win32/api/winuser/nf-winuser-defwindowproca) 如需舊版支援的詳細資訊，請參閱 [Windows Touch 手勢總覽](windows-touch-gestures-overview.md)。

## <a name="manipulations-and-inertia"></a>操作和慣性

Windows Touch 程式設計人員必須能夠以對手勢有意義的方式，從多個來源解讀手勢。 Microsoft 提供操作 API 來執行這些計算。 操作基本上是具有與其相關聯之值的手勢，這些值會描述整個手勢。 將輸入資料連線至操作處理器之後，您可以取得使用者在物件上進行的動作相關資訊。 下圖顯示您可以使用操作的其中一種方式。

![圖例顯示傳遞至物件操作處理器的 windows 觸控訊息，此處理程式會使用 imanipulationevents 介面來處理事件 \-](images/manipulation-arch.png)

在圖例左上方，使用者已接觸到畫面，這會建立觸控訊息。 這些訊息包含 x 座標和 y 座標，可用來判斷焦點物件。 焦點物件包含操作處理器。 接下來，在具有 **TOUCHEVENTF \_ UP** 旗標的 [**WM \_ 觸控**](wm-touchdown.md)訊息上，會選取使用者焦點的物件，並參考操作處理器，並將訊息傳送至操作處理器。 與此連絡人相關聯的後續 **wm \_ 觸控** 訊息會傳送至操作處理器，直到收到具有 **TOUCHEVENTF \_ UP** 旗標的 **wm \_ 觸控** 訊息，且已對選取的物件進行取值為止。 在圖例的右下方區段中，會使用實 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的操作事件接收器來處理在建立觸控訊息時所引發的操作事件。 事件接收可以根據執行中的操作事件，對介面執行更新。

在 Windows Touch 的應用程式中，通常會納入簡單物理，讓物件順暢地進入停止，而不是在不再觸及它們時突然停止。 Microsoft 提供慣性 API 來執行這些簡單物理的計算，讓您的應用程式能夠以類似于其他應用程式的方式運作。 這也可讓您省下建立強大物理功能所需的工作。 下圖顯示您可以如何使用慣性。

![圖例顯示傳遞至物件 iinertiaprocessor 介面的 windows 觸控訊息，此介面會使用 \- imanipulationevents 介面引發事件](images/inertia-arch.png)

請注意慣性與操作之間的相似之處。 兩者之間唯一的差異在於，如果是慣性，則會將解讀的訊息遞交給慣性處理器，而不是操作處理器，而慣性處理器會引發事件。 在圖例左上方的 **TOUCHEVENTF \_ UP** 旗標上 [**， \_**](wm-touchdown.md)觸控訊息是用來識別焦點中包含慣性處理器和操作處理器的物件。 後續的 **WM \_ 觸控** 訊息會傳送至操作處理器，而操作處理器會對應用程式 UI 執行更新。 操作完成後，會使用操作中的速度值來設定慣性處理器。 如中間的資料 [**行所示**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)，在個別執行緒中使用計時器或其他迴圈來呼叫 [**進程**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)或 [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)方法，直到呼叫表示處理器已完成處理。 進行這些呼叫時，會引發操作事件，這些事件是由以 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面為基礎的操作事件接收器所處理。 在圖的右下方區段中，此事件接收接著會根據操作事件，在事件接收中透過事件處理常式執行更新，以更新應用程式 UI。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 