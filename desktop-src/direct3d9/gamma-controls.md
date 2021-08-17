---
description: Gamma 控制項可讓您變更系統顯示介面內容的方式，而不會影響介面本身的內容。
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: " (Direct3D 9) 的 Gamma 控制項"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074f60199364ba86a0b5ad743fcc03121351cad0ac071d9231beef7c7156f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122199"
---
# <a name="gamma-controls-direct3d-9"></a> (Direct3D 9) 的 Gamma 控制項

Gamma 控制項可讓您變更系統顯示介面內容的方式，而不會影響介面本身的內容。 將這些控制項視為非常簡單的篩選器，讓 Direct3D 套用至資料，因為它會離開介面，然後在畫面上呈現。

Gamma 控制項是交換鏈的一個屬性。 Gamma 控制項可以動態地變更表面的紅色、綠色和藍色層級如何對應至系統顯示的實際層級。 藉由設定 gamma 層級，您可以在使用者的字元為快照時，讓使用者的螢幕閃爍色彩-紅色，當字元挑選新專案時為綠色，而不會將新的影像複製到框架緩衝區以達成效果。 或者，您也可以調整色彩層級，將色彩偏差套用至背景緩衝區中的影像。

由於 Direct3D 9 有一個交換鏈作為裝置的屬性，因此每個裝置一律至少有一個交換鏈 (隱含交換鏈) 。 由於 gamma 曲線是交換鏈的屬性，因此當交換鏈為視窗視窗時，可以套用 gamma 曲線。 Gamma 曲線會立即生效。 沒有等待垂直同步作業。

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)和 [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)方法可讓您操作從介面傳送至 (DAC) 的紅色、綠色和藍色色彩元件，再將其傳送至類比轉換器的遞增層級，以供顯示。

## <a name="gamma-ramp-levels"></a>Gamma 斜坡層級

在 Direct3D 中，「gamma」一詞是指一組值，這些值會將框架緩衝區中所有圖元的層級，對應至 DAC 所接收的新層級，以供顯示之用。 重新對應是透過三個查閱資料表（每個色彩元件各一個）來執行。

其運作方式如下： Direct3D 接受框架緩衝區的圖元，並評估其個別的紅色、綠色和藍色色彩元件。 每個元件都是以0到65535的值來表示。 Direct3D 會採用原始值，並使用它來編制256元素陣列 () 的索引，其中每個元素都包含一個值來取代原始值。 Direct3D 會針對框架緩衝區中每個圖元的每個色彩元件執行此查閱和取代程式，藉此變更所有螢幕圖元的最終色彩。

藉由繪製遞增的值來視覺化，是很方便的，如下列兩個圖所示。 左邊的圖形顯示的是不會修改色彩的斜坡。 右邊的圖表會顯示會對套用它的色彩元件施加負偏差的斜坡。

![gamma 遞增值的圖表](images/gammalv.png)

左邊圖形的陣列元素包含的值，與索引0（位於索引0的元素中的索引0）和索引255的65535相同。 這種類型的型別是預設值，因為它不會在顯示之前變更輸入值。 右側圖形提供更多變化;它的第一個元素中包含的值範圍從0到最後一個專案的32768，值的範圍則是一致的。 其效果是使用此曲線的色彩元件會在顯示時顯示為靜音。 您不一定要使用線性圖形;如果您的應用程式可以視需要指派任意對應。 您甚至可以將專案設定為全零，以從顯示中完全移除色彩元件。

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>設定和抓取 Gamma 遞增層級

Gamma 進階層是一種有效的查詢資料表，Direct3D 用來將框架緩衝區色彩元件對應至將顯示的新層級。 您可以藉由呼叫 [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 和 [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) 方法，來設定和取出主要表面的遞增層級。 **SetGammaRamp** 接受兩個參數，而 **GetGammaRamp** 接受一個參數。 針對 **SetGammaRamp**，第一個參數是 D3DSGR \_ 校準或 D3DSGR \_ 無 \_ 校正。 第二個參數 pRamp 是 [**D3DGAMMARAMP**](d3dgammaramp.md) 結構的指標。 **D3DGAMMARAMP** 結構包含單字的 3 256 元素陣列，每一個陣列都包含紅色、綠色和藍色的 gamma 斜坡。 **GetGammaRamp** 有一個參數，接受 **D3DGAMMARAMP** 類型的指標，而該指標將會填滿目前的 gamma 滑軌。

您可以 \_ 針對 [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 的第一個參數加入 D3DSGR 校正值，以在設定新的 gamma 層級時叫用校正器。 校準 gamma 的斜坡會產生一些處理額外負荷，不應經常使用。 設定校準的 gamma 曲線可為使用者提供一致且絕對的 gamma 值，而不論顯示器介面卡和監視為何。

並非所有系統都支援 gamma 校正。 若要判斷是否支援 gamma 校正，請在方法傳回之後，呼叫 [**GetDeviceCaps**](/windows/desktop/api)，然後檢查相關聯 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 Caps2 成員。 如果有 D3DCAPS2 \_ CANCALIBRATEGAMMA 功能旗標，則支援 gamma 校正。

設定新的遞增層級時，請記住，只有當您的應用程式處於全螢幕專用模式時，才會使用您在陣列中設定的層級。 當您的應用程式變更為一般模式時，會將遞增層級設定為在應用程式掉全螢幕模式時再次生效。

如果裝置在交換鏈目前的簡報模式中不支援 gamma 斜坡 (全螢幕或視窗型) ，則不會傳回錯誤值。 應用程式可以 \_ \_ 在 Caps2 類型的 D3DCAPS9 成員中檢查 D3DCAPS2 FULLSCREENGAMMA 和 D3DCAPS2 CANCALIBRATEGAMMA 功能位，以判斷裝置的功能以及是否已安裝校正器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 
