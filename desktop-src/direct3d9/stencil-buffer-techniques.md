---
description: 應用程式會使用樣板緩衝區來遮罩影像中的圖元。 遮罩控制是否繪製像素。 一些比較常見的效果如下所示。
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: " (Direct3D 9) 的樣板緩衝區技巧"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385836"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a> (Direct3D 9) 的樣板緩衝區技巧

應用程式會使用樣板緩衝區來遮罩影像中的圖元。 遮罩控制是否繪製像素。 一些比較常見的效果如下所示。

-   [合成](compositing.md)
-   [Decaling](decaling.md)
-   [溶解、淡化和撥動](dissolves--fades--and-swipes.md)
-   [大綱和 Silhouettes](outlines-and-silhouettes.md)
-   [雙側範本](two-sided-stencil.md)

樣板緩衝區啟用或停用依據個別像素的轉譯目標表面繪圖。 在最基本層級，它可以讓應用程式遮罩轉譯影像的區段，讓它們不會顯示。 應用程式通常會將樣板緩衝區用於特殊效果，例如溶解、印花，以及外框。

樣板緩衝區資訊內嵌於 z 緩衝資料。 您的應用程式可以使用 [**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 方法來檢查硬體範本支援，如下列程式碼範例所示。


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 可讓您根據裝置的功能，選擇要建立的裝置。 在此情況下，不支援8位樣板緩衝區的裝置將會遭到拒絕。 請注意，這只是 **IDirect3D9：： CheckDeviceFormat**; 的一個可能用途如需詳細資訊，請參閱 [判斷 (Direct3D 9) 的硬體支援](determining-hardware-support.md)。

## <a name="how-the-stencil-buffer-works"></a>樣板緩衝區的運作方式

Direct3D 依據個別像素在樣板緩衝區的內容執行測試。 對於目標表面的每一個像素，它會使用樣板緩衝區中的對應值、樣板參考值，以及樣板遮罩值來執行測試。 如果通過測試，Direct3D 執行動作。 使用下列步驟執行測試。

1.  執行樣板參考值與樣板遮罩的位元 AND 運算。
2.  執行目前像素之樣板緩衝區值與樣板遮罩的位元 AND 運算。
3.  使用比較函式，比較步驟 1 的結果與步驟 2 的結果。

下列程式碼範例會顯示這些步驟。


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



這是目前圖元的樣板緩衝區內容。 這個程式碼範例會使用 & 符號 (&) 符號來表示位 AND 運算。


```
StencilMask
```



表示樣板遮罩的值，以及


```
StencilRef
```



表示樣板參考值。


```
CompFunc
```



這是比較函數。

如果樣板測試通過，目前像素會寫入目標表面，否則會略過。 預設的比較行為是撰寫圖元，不論每位位運算的結果為何 (D3DCMP \_ 一律) 。 您可以變更此行為，方法是變更 D3DRS STENCILFUNC 轉譯 \_ 狀態的值，傳遞 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別的成員，以識別所需的比較函數。

您的應用程式可自訂樣板緩衝區的作業。 它可以設定比較函式、樣板遮罩和樣板參考值。 它也可以控制樣板測試通過或失敗時，Direct3D 採取的動作。 如需詳細資訊，請參閱 [ (Direct3D 9 的樣板緩衝區狀態) ](stencil-buffer-state.md)。

## <a name="examples"></a>範例

下列程式碼範例示範如何設定樣板緩衝區。


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



範本參考值預設為零。 任何整數值都有效。 Direct3D 會執行樣板參考值的位 and，以及樣板測試之前的樣板遮罩值。

您可以根據樣板的比較，來控制要寫出的圖元資訊。


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



您可以針對要寫入樣板緩衝區的值撰寫自己的公式，如下列範例所示。


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 
