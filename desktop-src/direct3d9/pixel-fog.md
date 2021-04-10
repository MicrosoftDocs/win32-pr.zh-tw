---
description: 圖元霧化會從設備磁碟機中以每圖元為基礎計算的事實取得其名稱。
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: " (Direct3D 9) 的圖元霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845735"
---
# <a name="pixel-fog-direct3d-9"></a> (Direct3D 9) 的圖元霧化

圖元霧化會從設備磁碟機中以每圖元為基礎計算的事實取得其名稱。 這與頂點霧化不同，它是在轉換和光源計算期間由管線所計算。 圖元霧化有時稱為資料表霧化，因為某些驅動程式會使用預先計算的查閱資料表來決定霧化因數，並使用每個圖元的深度來套用混合計算。 您可以使用 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別成員所識別的任何霧化公式來套用它。 這些公式的實作為特定驅動程式。 如果驅動程式不支援複雜的霧化公式，它應該會降級為較不復雜的公式。

## <a name="eye-relative-vs-z-based-depth"></a>Eye-Relative 與以 Z 為基礎的深度

若要減少深度緩衝區中不平均分佈的霧化相關圖形成品，大部分的硬體裝置都會使用眼睛相對深度，而非以 z 為基礎的深度值進行圖元霧化。 眼睛相對深度基本上就是來自同質座標集合的 w 元素。 Microsoft Direct3D 會從裝置空間座標設定 RHW 元素，以重現 true w。 如果裝置支援眼睛相關的霧化，則當您呼叫 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)方法時，它會在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 RasterCaps 成員中設定 **D3DPRASTERCAPS \_ WFOG** 旗標。 除了參考轉譯器之外，軟體裝置一律會使用 z 來計算圖元霧化效果。

當支援眼睛相關的霧化時，如果提供的投射矩陣在世界空間中產生的 z 值相當於裝置空間中的 w 值，系統會自動使用眼睛相關深度，而不是以 z 為基礎的深度。 您可以藉由呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 方法來設定投影矩陣，並使用 D3DTS \_ 投射值並傳遞代表所需矩陣的 [**D3DMATRIX**](d3dmatrix.md) 結構。 如果投射矩陣不符合這項需求，則不會正確套用霧化效果。 如需有關產生相容矩陣的詳細資訊，請參閱 [ (Direct3D 9) 的投射轉換 ](projection-transform.md)。

Direct3D 使用目前以 w 型深度計算的投影矩陣。 如此一來，應用程式就必須設定符合規範的投射矩陣，才能收到所需的 w 型功能，即使它不使用 Direct3D 轉換管線也一樣。

Direct3D 會檢查投射矩陣的第四個數據行。 如果係數為 \[ 0、0、0、1 \] (用於仿射投影) 系統將使用以 z 為基礎的深度值進行霧化。 在此情況下，您也必須指定裝置空間中線性模糊效果的開始和結束距離，範圍從0.0 到最接近使用者的位置，以及最遠的1.0。

## <a name="using-pixel-fog"></a>使用圖元霧化

使用下列步驟，在您的應用程式中啟用圖元霧化。

1.  將 D3DRS \_ FOGENABLE 轉譯狀態設為 **TRUE**，以啟用霧化混合。
2.  在 D3DRS FOGCOLOR 轉譯狀態中設定所需的霧化色彩 \_ 。
3.  將 D3DRS \_ FOGTABLEMODE 轉譯狀態設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的對應成員，以選擇要使用的霧化公式。
4.  在相關聯的轉譯狀態中，為選取的霧化模式設定所需的霧化參數。 這包括線性霧化的開始和結束距離，以及指數霧化模式的霧化密度。

下列範例會顯示這些步驟在程式碼中的樣子。


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



由於 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法只接受第二個參數中的 DWORD 值，因此某些霧化參數必須是浮點值。 上述範例會將浮點變數的位址轉換為 DWORD 指標，然後將其取值，以將浮點值提供給 **IDirect3DDevice9：： graphicsdevice** 而不需要資料轉譯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 
