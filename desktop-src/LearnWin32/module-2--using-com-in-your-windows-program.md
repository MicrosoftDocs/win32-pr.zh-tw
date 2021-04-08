---
title: 在您的 Windows 應用程式中使用 COM
description: 本系列的課程模組1顯示如何建立視窗並回應視窗訊息，例如 WM \_ 油漆和 wm \_ CLOSE。 模組2引進元件物件模型 (COM) 。
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682270"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>模組2。 在 Windows-Based 程式中使用 COM

本系列的 [課程模組 1](your-first-windows-program.md)顯示如何建立視窗並回應視窗訊息，例如 [**Wm \_ 油漆**](/windows/desktop/gdi/wm-paint)和 [**wm \_ CLOSE**](/windows/desktop/winmsg/wm-close)。 模組2引進元件物件模型 (COM) 。

COM 是建立可重複使用的軟體元件的規格。 您將在新式 Windows 程式中使用的許多功能都依賴 COM，如下所示：

-   圖形 (Direct2D) 
-   文字 (DirectWrite) 
-   Windows Shell
-   功能區控制項
-   UI 動畫

 (這份清單上的某些技術會使用 COM 的子集，因此不是 "pure" COM。 ) 

COM 具有難以學習的信譽。 撰寫新的軟體模組以支援 COM 是很棘手的。 但是，如果您的程式完全是 COM 的取用 *者* ，您可能會發現 com 比預期更容易理解。

此課程模組說明如何在您的程式中呼叫以 COM 為基礎的 Api。 它也會說明 COM 設計背後的一些原因。 如果您瞭解 COM 的設計方式，您可以更有效率地進行程式設計。 此課程模組的第二個部分描述 COM 的一些建議程式設計作法。

COM 是在1993中引進，以支援 OLE) 2.0 (的物件連結和內嵌。 有時候，人們認為 COM 和 OLE 是一樣的。 這可能是您認為 COM 難以學習的另一個原因。 OLE 2.0 是以 COM 為基礎，但您不需要知道 OLE 就能瞭解 COM。

COM 是 *二進位標準*，不是語言標準：它會定義應用程式與軟體元件之間的二進位介面。 以二進位標準而言，COM 會與語言無關，雖然它會自然地對應到某些 c + + 結構。 此課程模組將著重于 COM 的三個主要目標：

-   將物件的執行與其介面分開。
-   管理物件的存留期。
-   在執行時間探索物件的功能。

## <a name="in-this-section"></a>本節內容

-   [什麼是 COM 介面？](what-is-a-com-interface-.md)
-   [初始化 COM 程式庫](initializing-the-com-library.md)
-   [COM 中的錯誤碼](error-codes-in-com.md)
-   [在 COM 中建立物件](creating-an-object-in-com.md)
-   [範例：開啟對話方塊](example--the-open-dialog-box.md)
-   [管理物件的存留期](managing-the-lifetime-of-an-object.md)
-   [要求物件提供介面](asking-an-object-for-an-interface.md)
-   [COM 中的記憶體配置](memory-allocation-in-com.md)
-   [COM 編碼作法](com-coding-practices.md)
-   [COM 中的錯誤處理](error-handling-in-com.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[學習如何以 c + + 撰寫 Windows 程式](learn-to-program-for-windows.md)
</dt> </dl>

 

 