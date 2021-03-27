---
title: " (Direct3D 11) 的效果"
description: DirectX 效果是管線狀態的集合，由以 HLSL 撰寫的運算式所設定，以及某些特定于效果架構的語法。
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8952a35e1212f7d50956cc54e7a046db9f87b3b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682632"
---
# <a name="effects-direct3d-11"></a> (Direct3D 11) 的效果

DirectX 效果是管線狀態的集合，由以 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) 撰寫的運算式所設定，以及某些特定于效果架構的語法。

編譯效果之後，請使用效果架構 Api 來呈現。 效果功能的範圍可以像是頂點著色器一樣簡單，也就是轉換幾何和圖元著色器以輸出純色、轉換成需要多個行程的轉譯技術、使用圖形管線的每個階段，以及操作著色器狀態以及未與可程式化著色器相關聯的管線狀態。

第一個步驟是將您想要控制的狀態組織成一個效果。 這包括著色器狀態 (頂點、輪廓、網域、幾何、圖元和計算著色器) 、著色器所使用的材質和取樣器狀態，以及其他無法程式化的管線狀態。 您可以在記憶體中以文字字串的形式建立效果，但一般來說，大小夠大，因為在效果檔案中儲存效果的狀態， (一個以 fx 副檔名) 結尾的文字檔。 若要使用效果，您必須將它編譯 (以檢查 HLSL 語法以及效果架構語法) 、透過 API 呼叫初始化效果狀態，以及修改轉譯迴圈來呼叫轉譯 Api。

效果會將特定效果所需的所有轉譯狀態封裝到稱為技術的單一轉譯函數中。 Pass 是技術的子集合，其中包含呈現狀態。 若要執行多重傳遞轉譯效果，請在技術內執行一或多個階段。 例如，假設您想要使用一組深度/樣板緩衝區來轉譯某些幾何，然後在其上方繪製一些 sprite。 您可以在第一個階段中執行幾何轉譯，並在第二個階段中執行 sprite 繪製。 若要轉譯效果，您只需在轉譯迴圈中轉譯這兩個階段。 您可以在效果中執行任何數目的技巧。 當然，技術的數目愈大，結果的編譯時間就愈大。 利用這項功能的其中一種方法，就是使用專為在不同硬體上執行而設計的技術來建立效果。 這可讓應用程式根據偵測到的硬體功能，適當地將效能降級。

您可以將一組技術組成群組 (使用 "fxgroup" 語法 ) 。 您可以用任何方式將技術分組。 例如，可以建立多個群組，每個材質一個群組;每個材質可能會有每個硬體層級的技術;每個技術都會有一組可在特定硬體上定義材質的行程。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                | 描述                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [組織效果中的狀態](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | 使用 Direct3D 11 時，會依結構來組織特定管線階段的效果狀態。<br/>                                                                   |
| [效果系統介面](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | 效果系統會定義許多用於管理效果狀態的介面。<br/>                                                                                  |
| [專用介面](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 有許多方法可將介面轉換成您需要的特定介面類別型。<br/> |
| [作用中的介面和類別](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | 有許多方法可以在效果11中使用類別和介面。<br/>                                                                                         |
| [呈現效果](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | 您可以使用效果來儲存資訊，或使用一組狀態來呈現。<br/>                                                                         |
| [複製效果](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | 複製效果會建立第二個與效果幾乎相同的複本。<br/>                                                                                 |
| [資料流程輸出語法](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | 具有資料流程輸出的幾何著色器會使用特定語法來宣告。<br/>                                                                                  |
| [效果的差異10和效果11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | 本主題顯示效果10和效果11之間的差異。<br/>                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> </dl>

 

