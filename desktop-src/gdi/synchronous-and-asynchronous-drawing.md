---
description: 大部分在處理 WM 油漆訊息期間所執行的繪圖 \_ 都是非同步，也就是說，時間範圍的某個部分會失效，且傳送的時間為 WM 繪製的時間之間會有延遲 \_ 。
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: 同步和非同步繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945088"
---
# <a name="synchronous-and-asynchronous-drawing"></a>同步和非同步繪圖

大部分在處理 [**WM \_ 油漆**](wm-paint.md) 訊息期間所執行的繪圖都是非同步，也就是說，時間範圍的某個部分會失效，且傳送的時間為 WM 繪製的時間之間會有延遲 \_ 。 在延遲期間，應用程式通常會從佇列中取出訊息，並執行其他工作。 延遲的原因是系統通常會將視窗中的繪圖視為低優先順序作業，而且可以像使用者輸入訊息以及可能影響視窗的位置或大小的訊息，在 WM 油漆之前處理 \_ 。

在某些情況下，應用程式必須以同步方式繪製，也就是在視窗的某個部分之後立即在視窗中繪製。 一般的應用程式會在建立視窗後立即繪製其主視窗，以通知使用者應用程式已順利啟動。 系統會以同步的方式（例如按鈕）來繪製一些控制項視窗，因為這類 windows 可作為使用者輸入的焦點。 雖然可以同步繪製具有簡單繪圖常式的任何視窗，但是所有這類繪圖都應該快速完成，而且不會干擾應用程式回應使用者輸入的能力。

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)和 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)函式允許同步繪製。 如果更新區域不是空的， **UpdateWindow** 會直接將 [**WM \_ 油漆**](wm-paint.md)訊息傳送至視窗。 **RedrawWindow** 也會傳送 **WM \_ 油漆** 訊息，但讓應用程式更能控制視窗的繪製方式，例如是否要繪製非工作區和視窗背景，或者是否要傳送訊息，而不論更新區域是否為空白。 無論應用程式訊息佇列中的其他訊息數目為何，這些函式都會直接將 **WM \_ 油漆** 訊息傳送至視窗。

任何需要耗用耗時繪圖作業的視窗，都應該以非同步方式繪製，以防止在繪製視窗時封鎖暫止的訊息。 此外，任何經常使視窗的小部分失效的應用程式，都應該允許這些不正確部分合併到單一非同步 [**wm \_ 油漆**](wm-paint.md) 訊息中，而不是一系列的同步 **wm \_ 繪製** 訊息。

 

 



