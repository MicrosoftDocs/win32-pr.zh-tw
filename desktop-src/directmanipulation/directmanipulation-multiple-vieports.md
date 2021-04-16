---
description: 使用多個區域時，請按下連絡人的畫面位置，然後判斷連絡人叫用的位置，以 testingdetermines) 會受到使用者輸入影響的 (的區。
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: 在 DirectManipulation 中使用多個區
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104558089"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>在 DirectManipulation 中使用多個區

使用多個區域時， *點擊測試* 會藉由取得連絡人的畫面位置，並判斷連絡人所叫用的位置，來決定哪些 (的) 會受到使用者輸入影響。

[直接操作](direct-manipulation-portal.md)的常見案例是將一個區放在另一個（也稱為「*嵌套*」的區）。 如果連絡人叫用一個以上的區，則由視窗的 [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))呼叫的 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)順序，會決定嵌套的方程式之父子式關聯性。

規則：子項目應該在呼叫父系之前呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)。

![顯示點擊測試階層的圖表](images/dm-art-8.png)

連絡人會在一個區中關閉。 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 應該先在橙色 (子) 區上呼叫，然後再以綠色 (父) 區來建立正確的階層。

## <a name="targeting-the-correct-viewport"></a>以正確的視口為目標

連絡人可以與任意數目的區數相關聯，而且每個連絡人都可以指派給不同的一組區。

您可以視需要設定每個區，以支援特定的互動。

根據這些設定， [直接操作](direct-manipulation-portal.md) 會識別哪些區可處理輸入。 點擊測試階層中的子系大部分的視口都有處理輸入的第一次機會。 不過，連結和父代升級都可以變更哪些區來處理輸入。

## <a name="chaining"></a>鏈結

在操作期間到達內容的結尾時， [直接操作](direct-manipulation-portal.md) 會套用界限效果，以表示內容無法再繼續。 但是，如果子區 *連結* 至父個區，則會隱藏此效果。 相反地，點擊測試階層中最接近支援操作的上階區，會處理輸入。 如果操作方向反轉，使上階回到觸發連結的時間點，則操作 "unchains" 並將控制權轉移回子區。

![顯示連鎖操作的圖表](images/dm-art-9.png)

當使用者將子系視窗全部移動至內容的邊緣時，會將「鏈」操作系至父區，而使用者會開始改為移動父內容。

> [!Note]  
> X 和 Y 軸彼此獨立，因此如果對角平移觸及 y 界限之前的 x 界限，則操作會在 x 方向移動父系，同時繼續以 y 方向移動子系。 若要啟用或停用連結，請在子區上呼叫 [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) API。

### <a name="rails"></a>Rails

在設定區的設定中指定滑軌，會影響從區連結輸入的方式。 具體而言，輸入無法在滑軌的 "unrailed" 移動瀏覽模式中，從 railed 子區連結到其父系。 若要在設定滑軌時鏈出輸入，使用者必須以垂直或水準方式移動流覽並鎖定滑軌。

### <a name="zooming"></a>顯示比例

如果子區是在父代內進行嵌套，而且兩者都設定為縮放，則縮放操作可從子系連結到父系。 但是，如果操作繼續進行，它只會在父系上運作，而且無法將其「unchain」至子系。 如果使用者將縮放從子系連結到父系，則 [直接操作](direct-manipulation-portal.md) 會暫停子系，直到與操作相關聯的所有連絡人都從螢幕中移除為止。 此時，子系會從暫止中釋出，而使用者可以移動子系的子功能區。

## <a name="gesture-targeting-parent-promotion"></a>手勢目標：上層升級

*手勢目標* 是 [直接操作](direct-manipulation-portal.md) 將連絡人群組在一起的程式，並決定哪些區會處理輸入。 「*父代升級*」是指將輸入從子系傳送到父系的情況。 例如，當使用者在設定為僅供滾動的子區中，將兩個連絡人和 pinches 放在一起時，會將輸入升級為父代，以便進行縮放。 無論子系的子系是否啟用了連結，都會發生父代升級。

與連結不同的是，不會反轉父項升級。 父元件會繼續處理互動輸入，直到所有的連絡人都 (子視窗區停止處理輸入) 為止。
