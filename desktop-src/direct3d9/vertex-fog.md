---
description: 當系統執行頂點 fogging 時，它會在多邊形中的每個頂點上套用霧化計算，然後在點陣化期間將結果插到多邊形的臉部。
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: " (Direct3D 9) 的頂點霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108392"
---
# <a name="vertex-fog-direct3d-9"></a> (Direct3D 9) 的頂點霧化

當系統執行頂點 fogging 時，它會在多邊形中的每個頂點上套用霧化計算，然後在點陣化期間將結果插到多邊形的臉部。 頂點霧化效果是由 Direct3D 光源和轉換引擎所計算。 如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。

如果您的應用程式未使用 Direct3D 進行轉換和光源，應用程式必須執行霧化計算。 在此情況下，請放置在每個頂點之反射色彩的 Alpha 元件中計算的霧化因數。 您可以隨意使用任何想要的公式-範圍型、體積型，或其他任何公式。 Direct3D 會使用提供的霧化因數，以在每個多邊形的臉部之間進行插補。 執行自己的轉換和光源的應用程式也必須執行自己的頂點霧化計算。 如此一來，這類應用程式只需要啟用霧化混合，並透過相關聯的轉譯狀態設定霧化色彩，如 [ (direct3d 9) ](fog-blending.md) 和 [ (direct3d 9) ](fog-color.md)的霧化色彩中所述。

> [!Note]  
> 使用頂點著色器時，您必須使用頂點霧化。 這是使用頂點著色器將每個頂點的霧化濃度寫入 oFog 註冊來完成的。 圖元著色器完成後，會使用 oFog 資料以線性方式插補與霧化色彩。 圖元著色器無法使用此強度。

 

## <a name="range-based-fog"></a>Range-Based 霧化

> [!Note]  
> 只有在搭配 Direct3D 轉換和光源引擎使用頂點霧化時，Direct3D 才會使用範圍型的霧化計算。 這是因為在設備磁碟機中會實作為圖元霧化，而且目前沒有硬體可支援每個圖元範圍的霧化。 如果您的應用程式會執行自己的轉換和光源，它必須執行自己的霧化計算（以範圍為基礎或其他）。

 

有時候，使用霧化可能會導入圖形成品，以 nonintuitive 方式將物件與霧化色彩混合。 例如，假設有一個場景，其中有兩個可見的物件：一段距離足以受到霧化的影響，而另一個則接近不受影響。 如果視圖區域就地旋轉，則可能會變更明顯的霧化效果，即使物件是固定的也一樣。 下圖顯示這種情況的由上而下的觀點。

![兩個視點的圖表，以及它們對兩個物件的霧化有何影響](images/artifog.png)

以範圍為基礎的霧化是判斷霧化效果的另一個更精確的方式。 在以範圍為基礎的霧化中，Direct3D 會使用從視點到頂點的實際距離來進行霧化計算。 Direct3D 會增加霧的影響，因為這兩個點之間的距離會增加，而不是場景內頂點的深度，藉以避免旋轉成品。

如果目前的裝置支援以範圍為基礎的霧化，則 \_ 當您呼叫 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)方法時，它會在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 RasterCaps 成員中設定 D3DPRASTERCAPS FOGRANGE 值。 若要啟用以範圍為基礎的霧化，請將 D3DRS \_ RANGEFOGENABLE 轉譯狀態設為 **TRUE**。

以範圍為基礎的霧化是由 Direct3D 在轉換和光源期間計算。 未使用 Direct3D 轉換和光源引擎的應用程式也必須執行自己的頂點霧化計算。 在此情況下，請針對每個頂點，在反射元件的 Alpha 元件中提供範圍型霧化係數。

## <a name="using-vertex-fog"></a>使用頂點霧化

使用下列步驟，在您的應用程式中啟用頂點霧化。

1.  將 D3DRS \_ FOGENABLE 設定為 **TRUE**，以啟用霧化混合。
2.  設定 D3DRS FOGCOLOR 轉譯狀態中的 [霧化色彩] \_ 。
3.  將 D3DRS \_ FOGVERTEXMODE 轉譯狀態設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的成員，以選擇所需的霧化公式。
4.  在轉譯狀態中，為選取的霧化公式設定所需的霧化參數。

下列以 c + + 撰寫的範例會顯示這些步驟在程式碼中的樣子。


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



某些霧化參數是浮點值的必要參數，即使 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法只接受第二個參數中的 DWORD 值也是一樣。 這個範例會將浮點變數的位址轉換成 DWORD 指標，然後將它們取值，以成功提供這些方法的浮點值給這些方法，而不需要資料轉譯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 
