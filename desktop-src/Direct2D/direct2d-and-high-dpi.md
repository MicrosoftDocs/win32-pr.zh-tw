---
title: Direct2D 和高 DPI
description: 描述 Direct2D 如何容納高 DPI 顯示器。
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D，高 DPI
- 高 DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5c48f9a1b3552115ebbec8a54a6878716ef34675e41193ae08fb9cb8e55bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825980"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D 和高 DPI

撰寫 DPI 感知的應用程式是讓使用者介面 (UI 的關鍵，) 在各式各樣的高 DPI 顯示器設定中的外觀一致。 非 DPI 感知但在高 DPI 顯示器設定上執行的應用程式，可能會受到許多視覺構件的影響，包括不正確地調整 UI 元素、剪下文字和模糊影像。 藉由在應用程式中加入支援 DPI 感知的功能，您可以更容易預測應用程式的 UI，讓使用者更具視覺效果且更容易閱讀。 幸運的是，Direct2D 可讓您更輕鬆地撰寫在高 DPI 中運作正常的應用程式。 本主題包含下列各節。

-   [Direct2D 中的高 DPI 支援](#high-dpi-support-in-direct2d)
-   [Windows 8 和高 DPI](#windows-8-and-high-dpi)
-   [什麼是 DIP？](#what-is-a-dip)
-   [相關主題](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Direct2D 中的高 DPI 支援

Direct2D 提供下列功能來處理高 DPI 案例：

-   只要應用程式資訊清單指出應用程式正確處理 DPI，就會在建立視窗化轉譯目標時自動接受系統 DPI。  (需如何宣告應用程式為 DPI 感知的詳細資訊，請參閱 [如何確保您的應用程式在高 DPI 顯示器上正確顯示](how-to--size-a-window-properly-for-high-dpi-displays.md)。 ) 
-   它會以 Dip (與裝置無關的圖元為單位來表示座標) ，可讓應用程式在 DPI 設定變更時自動調整。
-   它可讓點陣圖具有 DPI，並藉由將 DPI 納入考慮，以正確地調整它們的規模。 這項功能也可以用來維護不同解析度的圖示。
-   它會以 Dip 表示大部分的資源，讓資源自動獨立于解析度之外。
-   它使用浮點座標空間和消除鋸齒，因此任何內容都可以調整成任意的 DPI。

Direct2D 圖形管線的設計目的是要從 96 DPI 調整為1200DPI。

## <a name="windows-8-and-high-dpi"></a>Windows 8 和高 DPI

從 Windows 8 開始，有高 DPI 支援的額外功能。

如果裝置內容 DPI 夠高，Direct2D 會變更它用來啟用文字垂直消除鋸齒的閾值。 這會導致在高 DPI 顯示器上更快速地呈現文字。 此外，您也可以使用 [**ID2D1DeviceCoNtext：： SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) 方法，將單元模式切換成圖元而不是 dip。 如果您將單位模式設定為圖元，並將裝置內容 DPI 設定為螢幕 DPI，則仍會啟用優化。

## <a name="what-is-a-dip"></a>什麼是 DIP？

與裝置無關的圖元 (DIP) 是一個邏輯圖元，會透過純量（DPI）對應至實體裝置的圖元。 DPI 代表每英寸的點，其中點代表實體裝置圖元。  (的命名法來自列印，其中的點是列印程式可產生) 的最小筆墨點。 因為標準監視器是用來在每個英寸各有96的點，所以 DPI 96 表示與裝置無關的圖元 (或 DIP) 對應1:1 與實體圖元。 例如，如果 DPI 為 96 \* 2 = 192，則單一 DIP 會包含兩個實體圖元。

應用程式不一定會正確處理此調整的原因有很多;最簡單的原因之一是它需要額外的工作，才能在轉譯時探索和使用此純量值。 在 Direct2D 中，預設會套用調整。 由於這項對應，實體裝置圖元可能會以小數 DIP 座標為單位，這是 Direct2D 使用浮點座標空間的原因之一。

<dl> 實體圖元 = (dip × DPI) /96  
</dl>

若要將實體圖元轉換為 DIP，請使用下列公式：

<dl> dip = (實體圖元× 96) /DPI  
</dl>

> [!Note]
>
> 從 Windows 8 開始，您可以使用 [**ID2D1DeviceCoNtext：： SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode)方法，將單元模式切換成圖元而不是 dip。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何確保您的應用程式在高 DPI 顯示器上正確顯示](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 