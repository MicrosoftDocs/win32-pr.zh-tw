---
title: 架構與元件
description: 本主題說明組成 Microsoft DirectComposition 的元件。
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023910"
---
# <a name="architecture-and-components"></a>架構與元件

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題說明組成 Microsoft DirectComposition 的元件。 其中包含下列各節。

-   [軟體元件](#software-components)
-   [應用程式程式庫](#application-library)
-   [撰寫引擎](#composition-engine)
-   [相關主題](#related-topics)

## <a name="software-components"></a>軟體元件

DirectComposition 包含下列主要軟體元件。

-   使用者模式應用程式程式庫 (dcomp.dll) ，它會執行 (COM) 型公用 API 的元件物件模型。
-   使用者模式組合引擎 (dwmcore.dll) 裝載于桌面視窗管理員 (DWM) 處理常式 (dwm.exe) ，並執行實際的桌面組合。
-   核心模式物件資料庫 (win32k.sys) 的一部分，可將命令從應用程式封送處理至撰寫引擎。

組合引擎的單一實例會處理所有應用程式的 DirectComposition 組合樹狀結構，以及代表整個桌面的 DWM 組合樹狀結構。 在每個會話中，核心模式物件資料庫和使用者模式組合引擎都會具現化一次，因此具有多個使用者的終端機伺服器電腦會有這兩個元件的多個實例。

下圖顯示主要 DirectComposition 元件，以及它們彼此之間的關聯性。

![directcomposition 最上層架構](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>應用程式程式庫

DirectComposition 應用程式程式庫是一個公用的 COM 型 API，其具有從 dcomp.dll 匯出的單一一般進入點，並傳回裝置物件的介面指標。 然後，裝置物件有方法可建立其他所有物件，每個物件都是由介面指標表示。 所有的 DirectComposition 介面都會繼承自並完全執行 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面。 所有接受 DirectComposition 介面的方法都會檢查介面是否在 dcomp.dll 內部執行，或是否由另一個元件所實。 因為 DirectComposition 不可延伸，所以將介面視為參數的方法會傳回 E \_ INVALIDARG （如果介面未在 dcomp.dll 中執行）。 API 不需要任何特殊許可權;它可由在最低存取層級執行的進程呼叫。 不過，因為 API 不會在會話0中運作，所以不適合服務。 在這些方面，DirectComposition API 類似于其他 Microsoft DirectX Api，最值得注意的是 Direct2D、Microsoft Direct3D 和 Microsoft DirectWrite。

由於撰寫引擎是專門針對非同步執行而設計的，因此 DirectComposition API 中的物件屬性是唯讀的。 所有屬性都有 setter 方法，而不是 getter 方法。 讀取屬性不僅需要耗用大量資源，也可能不正確，因為組合引擎傳回的任何值都可以立即變成無效。 舉例來說，如果獨立的動畫系結至正在讀取的屬性，就會發生這種情況。

API 是安全線程。 應用程式隨時都可以從任何執行緒呼叫任何方法。 不過，因為許多 API 方法都必須以特定順序呼叫，所以如果沒有任何同步處理，則應用程式可能會因執行緒的交錯方式而遇到無法預期的行為。 例如，如果兩個執行緒同時將相同物件的相同屬性變更為不同的值，應用程式就無法預測兩個值中的哪一個是屬性的最終值。 同樣地，如果兩個執行緒呼叫相同裝置上的 [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) ，則這兩個執行緒都不會取得真正的交易行為，因為在某個執行緒上的 **commit** 呼叫將會提交兩個執行緒所發出之所有命令的批次，而不只是呼叫 **commit** 的執行緒。

系統會維護每個裝置物件的所有內部狀態。 如果應用程式建立兩個或多個 DirectComposition 的裝置物件，應用程式可以維護獨立批次，以及兩者之間的其他狀態。

所有 DirectComposition 物件都具有裝置物件親和性;特定裝置物件所建立的物件只能用於該裝置物件，且只能與相同裝置物件所建立的其他物件相關聯。 換句話說，每個裝置物件都是分開的獨立功能島。 其中一個例外狀況是視覺效果類別，允許建立視覺樹狀結構，其中的視覺效果可以屬於與其父系不同的裝置物件。 這可讓應用程式和控制項管理單一組合樹狀結構，而不需要共用單一 DirectComposition 裝置物件的情況。

## <a name="composition-engine"></a>撰寫引擎

DirectComposition 組合引擎會在專用的進程上執行，與任何應用程式進程不同。 單一撰寫程式（dwm.exe）支援會話中的每個應用程式。 每個應用程式都可以針對它所擁有的每個視窗建立兩個視覺化樹狀結構。 所有的樹狀結構實際上都實作為較大型視覺化樹狀結構的子樹，也包含 DWM 的組合結構。 DWM 會針對會話中的每個桌面，各建立一個大型的視覺化樹狀結構。 以下是這個架構的主要優點：

-   組合引擎可以存取所有應用程式點陣圖和視覺化樹狀結構，以啟用跨進程視窗互通性和組合。
-   撰寫引擎會在與任何應用程式程式不同的信任系統進程中執行，讓具有低存取權限的應用程式可以安全地撰寫受保護的內容。
-   撰寫引擎可以偵測特定視窗完全 pixels occluded 的時間，並避免浪費 CPU 和圖形處理器單位 (GPU) 資源為視窗組成。
-   撰寫引擎可以直接組成螢幕背景緩衝區，而不需要個別進程組合引擎所需的額外複本。
-   所有應用程式都會共用單一 Direct3D 裝置以進行組合，可節省可觀的記憶體

視覺化樹狀結構是保留的結構。 DirectComposition API 公開以不可部分完成處理的變更批次編輯結構的方法。 DirectComposition API 中的根物件是裝置物件，可作為所有其他 DirectComposition 物件的 factory，並包含稱為 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)的方法。 撰寫引擎不會反映應用程式對視覺化樹狀結構所做的任何變更，直到應用程式呼叫 **Commit** 為止，屆時最後一次 **認可** 之後的所有變更都會處理為單一交易。

呼叫 [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 的需求與「框架」的概念類似，不同之處在于，因為組合引擎會以非同步方式執行，所以可能會在呼叫 **認可** 之間呈現數個不同的畫面格。 在 DirectComposition 中， *框架* 是組合引擎的單一反復專案，而應用程式在兩個 **認可** 呼叫之間花費的間隔稱為 *批次*。

DirectComposition 會將所有應用程式呼叫批次到 DirectComposition API。 在 win32k.sys 會話驅動程式中所執行的核心物件資料庫會儲存與 API 呼叫相關聯的所有狀態資訊。

組合引擎會為顯示中的每個垂直空白產生一個畫面格。 畫面格會以垂直的空白啟動，並以後續垂直空白為目標。 當框架啟動時，組合引擎會挑選所有暫止的批次，並在該框架中包含其命令。 當應用程式呼叫 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)時，會將批次放在暫止的佇列中，而暫止的佇列會在框架的開頭以原子方式進行清除。 因此，有一個會標示框架開頭的時間點。 在此時間點之前提交的任何批次都會包含在框架中，而在之後提交的任何批次必須等到下一個畫面格才能處理。 完整撰寫迴圈如下所示：

1.  估計下一個垂直空白的時間。
2.  取出所有暫止的批次。
3.  處理已取出的批次。
4.  使用步驟1中估計的時間更新所有動畫。
5.  判斷需要重新撰寫的螢幕區域。
6.  重新撰寫中途區域。
7.  藉由為每個畫面翻轉背面和前端緩衝區來呈現畫面格。
8.  如果未在步驟6和7中撰寫任何內容並加以呈現，請等候批次認可。
9.  等候下一個垂直空白。

如果有多個監視器連接到單一視訊卡，組合引擎會使用主要監視器的垂直空白來驅動組合迴圈，並設定動畫取樣時間。 每個監視器都會以個別的全螢幕翻轉鏈表示;撰寫引擎會使用單一 Direct3D 裝置，以迴圈配置資源的方式，為每個監視器重複步驟6和7。 如果也有多張視訊卡，組合引擎會針對步驟6和7中的每個視訊卡使用個別的 Direct3D 裝置。

下拉式列示方塊架的排程一律是從垂直空白開始，如下圖所示。

![下拉式列示方塊架排程](images/composition-frame-scheduling.png)

如果組合引擎沒有任何要執行的工作，因為組合樹狀結構未變更，撰寫執行緒會在等候新的批次時進入睡眠狀態。 當提交新批次時，組合執行緒會喚醒，但會立即回到睡眠狀態，直到下一個垂直空白為止。 此行為可確保應用程式和組合引擎的可預測框架開始和結束時間。

組合引擎會發佈框架呈現時間和目前的畫面播放速率。 發佈這項資訊可讓應用程式針對自己的批次預估呈現時間，進而啟用動畫的同步處理。 尤其是，應用程式可以使用組合引擎的框架統計資料組合，以及 UI 執行緒產生批次所需的歷程記錄模型，以判斷其本身動畫的取樣時間。

例如，在上圖所示的應用程式批次開始時，應用程式可以查詢組合引擎以判斷下一個畫面格的精確呈現時間。 然後，應用程式可以使用目前的時間，以及它所產生的先前批次的相關資訊，以判斷應用程式是否可以在下一個垂直空白之前完成目前的批次。 因此，應用程式會使用框架呈現時間作為其本身動畫的取樣時間。 如果應用程式判斷不太可能在目前的垂直空白中完成工作，則應用程式可以改為使用後續的畫面格時間做為取樣時間，方法是使用組合引擎所傳回的畫面播放速率資訊來計算該時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 