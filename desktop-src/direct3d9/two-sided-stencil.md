---
description: 利用樣板緩衝區繪製陰影時將會使用到陰影錐。
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: 'Two-Sided 範本 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bca0b960f96d1747b2b7ad51771276df2cfe1da1fa8ac9aa4d7c1ce8ea7c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290508"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided 範本 (Direct3D 9) 

利用樣板緩衝區繪製陰影時將會使用到陰影錐。 應用程式透過計算剪影的邊緣，將其往光源的反方向突出並形成一組 3D 體積的集合，進而計算遮蔽幾何物的陰影錐。 這些物體接著會在經過兩次的轉譯之後寫入樣板緩衝區。

第一次轉譯會繪製面向前端的多邊形，並遞增樣板緩衝區的值。 第二次轉譯會繪製陰影錐面向後端的多邊形，並遞減樣板緩衝區的值。 一般而言，所有遞增及遞減的值會互相抵銷。不過，當陰影錐被轉譯時，場景已經在一般幾何導致某些像素無法通過 z 衝突測試時轉譯完成。 留在樣板緩衝區的值將會對應到陰影中的像素。 這些剩餘的樣板緩衝區內容會作為遮罩使用，以將一個包括所有內容的巨大黑色四元組 Alpha 混合至場景中。 藉由將樣板緩衝區作為遮罩，陰影中的像素將會進一步加深。

這表示針對每個光源，陰影幾何都會繪製兩次，因此對 GPU 的頂點輸送量形成了壓力。 雙面樣板便是為了避免這種情況而設計出來的功能。 在這種方法之下，會有兩組樣板狀態 (命名如下)：其中一組為針對每個面向前端的三角形設定的樣板狀態，另外一組則是針對面向後端的三角形。 如此一來，針對每個光源及每個陰影錐都只會進行一階段的繪製。

API 變更會限制為一組新的呈現狀態。 新的轉譯狀態 D3DRS \_ 雙 \_ 側 \_ StencilMODE 可以設定為 **TRUE** 或 **FALSE**。 預設為 **FALSE** ，表示目前 (DirectX 8) 行為。 當這設定為 **TRUE** 時 (只有在將 D3DSTENCILCAPS TWOSIDED 設定為 [) ] 時，才會運作 \_ ，而下列轉譯狀態只會套用至正面 (順時針) 三角形。



| 轉譯狀態        | 描述                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | 如果樣板測試失敗，則為 D3DSTENCILOP。                                                |
| D3DRS \_ STENCILZFAIL | 如果樣板測試通過和 z 測試失敗，則為 D3DSTENCILOP。                              |
| D3DRS \_ STENCILPASS  | 如果樣板和 z 測試都通過，則 D3DSTENCILOP。                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC fn。 如果 ( (ref & mask) stencilfn (樣板 & mask) ) 為 true，則樣板測試會通過。 |



 

一組新的轉譯狀態會套用至反向 () 三角形的回溯方向。



| 轉譯狀態             | 描述                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | 如果樣板測試失敗，則為 D3DSTENCILOP。                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | 如果樣板測試通過和 z 測試失敗，則為 D3DSTENCILOP。                                    |
| D3DRS \_ CCW \_ STENCILPASS  | 如果樣板和 z 測試都通過，則 D3DSTENCILOP。                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | D3DCMPFUNC 函式。 如果 ( (ref & mask) stencilfn (樣板 & mask) ) 為 true，則樣板測試會通過。 |



 

其餘的樣板呈現狀態一律會套用至順時針和逆時針三角形。

D3DRS \_ \_ \_ 會忽略行和點 sprite 的雙側 StencilMODE，這表示行為與 DirectX 8 不相同。 D3DRS \_ CCW 樣板 \_ 轉譯 \* 狀態會被忽略。

新的 cap 位表示裝置是否支援此功能。 不支援這項功能的驅動程式應該忽略這些新的呈現狀態。 所有其他樣板的 cap 位都適用于兩種樣板緩衝模式。 因為兩個 \_ 側邊樣板 \_ 表示可以使用 D3DCULLMODE \_ NONE set 來繪製，所以如果它支援這個新的樣板模式，則必須由驅動程式設定對應的端點。 Microsoft Windows 硬體品質實驗室 (WHQL) 應該強制執行這種情況。

新的呈現狀態：


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



新 cap：


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[樣板緩衝區技術](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
