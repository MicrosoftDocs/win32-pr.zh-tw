---
title: 移植 X 視窗系統應用程式
description: 移植 X 視窗系統應用程式
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- Windows 上的 OpenGL，移植
- 移植至 OpenGL、X 視窗系統
- OpenGL 移植 X 視窗系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034758"
---
# <a name="porting-x-window-system-applications"></a>移植 X 視窗系統應用程式

就像 Windows 一樣，X 視窗系統是以事件處理，以訊息為基礎的系統，使用視窗控制項和功能表。 您 X 視窗系統應用程式中的 OpenGL 程式碼可能位於與您將它移植到 Windows 的位置大致對應的區域中。 大部分的 OpenGL 程式碼都不會變更，但是您必須重寫 X 視窗系統專屬的任何程式碼。

**使用下列一般程式，將您的 X Window 系統 OpenGL 程式移植到 Windows**

1.  使用對等的 Windows 程式碼，重寫 X 視窗系統特定的程式碼。 找出視窗建立和事件處理常式代碼。 X 視窗系統和 Windows 是事件處理、以訊息為基礎的視窗化系統，可讓您更輕鬆地判斷要在哪裡進行適當的變更。  (不過，特別是對於大型應用程式，將應用程式從一個作業系統重寫為另一個作業系統可能是複雜且困難的工作。 ) 
2.  找出使用 GLX 函數的任何程式碼。 這些是您將轉譯為其對等 Windows 函式的函式。
3.  將 GLX 像素格式函式和視覺化/可繪製函數轉譯為適當的 Windows/OpenGL 像素格式和裝置內容函式。
4.  將 GLX 轉譯內容函數轉譯成 Windows/OpenGL 轉譯內容函式。
5.  將 GLX Pixmap 函數轉譯為對等的 Windows 函式。
6.  將 GLX 畫面格緩衝區和其他 GLX 函數轉譯為適當的 Windows 函式。

 

 




