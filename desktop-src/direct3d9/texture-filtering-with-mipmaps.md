---
description: Mipmap 是一組紋理序列，序列中的每個影像都是相同影像漸進式降低解析度的結果。
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: 使用 Mipmap (Direct3D 9) 的材質篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570930"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>使用 Mipmap (Direct3D 9) 的材質篩選

Mipmap 是一組紋理序列，序列中的每個影像都是相同影像漸進式降低解析度的結果。 在 mipmap 中，每個影像（或層級）的高度和寬度是比上一個層級小二的高度和寬度。 Mipmap 不一定要是矩形。

高解析度的 Mipmap 影像用於接近使用者的物件。 低解析度的影像則是用於物件出現在較遠的位置時。 Mipmap 藉由消耗較多的記憶體，以達到改善轉譯紋理品質的效果。

Direct3D 以一串附加表面的鏈結來代表 Mipmap。 解析度最高的紋理位於鏈結的開頭，並且將下一層級的 Mipmap 作為附件。 接下來，該作為附件的層級又會將下一個層級的 Mipmap 作為附件，以此類推，直到最低解析度的 Mipmap。

下列圖例呈現了這些層級的範例。 點陣圖紋理代表 3D 第一人稱射擊遊戲中容器上的標誌。 作為 Mipmap 建立時，解析度最高的紋理就會是 Mipmap 組中的首位。 在 Mipmap 組中，接下來的每個紋理都會以 2 的乘冪縮小。 在此範例中，解析度最高的 Mipmap 為 256 x 256。 接下來的紋理為 128 x 128。 鏈結中最後一個紋理則為 64 x 64。

從使用者可看到該標誌開始，這個標誌擁有最遠的距離。 若使用者在距離標誌較遠的地方開始，遊戲會顯示 Mipmap 鏈結中最小的紋理。(在此一範例中即為 64 x 64。)

![64 x 64 危險標誌的圖例](images/mip1.jpg)

當使用者將視角往標誌移動時，隨著距離越來越近，遊戲就會使用解析度更高的紋理。 下列圖例的解析度是 128 x 128。

![128 x 128 危險標誌的圖例](images/mip2.jpg)

當使用者的視角位於標誌允許的最小觀看距離時，遊戲便會使用解析度最高的紋理，如下列圖例所示。

![256 x 256 危險標誌的圖例](images/mip3.jpg)

Mipmap 在模擬紋理的透視上更有效率。 相較於將單一紋理轉譯成多個解析度，直接利用多張不同解析度的紋理會更為快速。

Direct3D 可評估 Mipmap 組中哪一張紋理的解析度最接近所需要的輸出影像。 若最終影像的解析度介於 Mipmap 組中紋理的解析度之間，Direct3D 可檢查兩個 Mipmap 中的紋理並且將其色彩值混合。

若要使用 Mipmap，您的應用程式必須先建置一組 Mipmap。 應用程式透過將 Mipmap 組設定為現有紋理組中的第一個紋理來套用 Mipmap。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。

接下來，您的應用程式必須設定 Direct3D 用來取樣材質的篩選方法。 Mipmap 篩選最快的方法就是讓 Direct3D 選擇最接近的材質。 使用 D3DTEXF \_ 點列舉值來選取此值。 如果您的應用程式使用 D3DTEXF 線性列舉值，Direct3D 可以產生更佳的篩選結果 \_ 。 這會選擇最接近的 Mipmap，並且計算圍繞著紋理中現有像素對應位置的材質之加權平均數。

Mipmap 紋理在 3D 場景中作為減少轉譯場景所需時間的用途使用。 其也能強化場景的擬真度。 然而，其通常需要大量的記憶體。

## <a name="creating-a-set-of-mipmaps"></a>建立一組 Mipmap

下列範例會示範您的應用程式如何呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 方法，以建立五個 mipmap 層級的鏈：256x256、128x128、64x64、32x32 和16x16。


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



[**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)接受的前兩個參數是最上層紋理的大小和寬度。 第三個參數指定紋理中的層級數目。 如果您將此值設定為零，Direct3D 會建立一組介面，每一個表面都比上一個小兩倍，降至最小可能的1x1 大小。 第四個參數會指定此資源的使用量;在此情況下，會指定0以指出資源沒有特定的使用量。 第五個參數指定紋理的介面格式。 請使用此參數的 [D3DFORMAT](d3dformat.md) 列舉型別值。 第六個參數指定 [**D3DPOOL**](./d3dpool.md) 列舉型別的成員，指出要在其中放置所建立資源的記憶體類別。 除非您使用動態紋理，否則建議使用 D3DPOOL \_ MANAGED。 最後一個參數會接受 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面指標的位址。

> [!Note]  
> Mipmap 鏈中的每個介面都有維度，其為鏈中前一個表面的一半。 如果最上層的 Mipmap 有著 256 x 128 的維度大小，第二層 Mipmap 的維度大小即為 128 x 64，第三層則為 64 x 32，以此類推，直到 1 x 1 為止。 您無法請求可能會使鏈結中任何一個 Mipmap 的寬度或高度小於 1 的 Mipmap 級數。 簡單舉例來說，若最上層 Mipmap 表面為 4 x 2，最大容許級數即為 3。 最上層維度為 4 x 2，第二層維度為 2 x 1，第三層的維度即為 1 x 1。 由於超過第三層後即會產生第二層 Mipmap 高度的分數值，因此程式並不允許。

 

## <a name="selecting-and-displaying-a-mipmap"></a>選取和顯示 Mipmap

呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/desktop/api) 方法，將 mipmap 材質集設定為目前材質清單中的第一個材質。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。

當您的應用程式選取 mipmap 材質集之後，必須將 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 列舉類型的值指派給 D3DSAMP \_ MIPFILTER 取樣器狀態。 Direct3D 接著會自動執行 mipmap 材質篩選。 下列程式碼範例會示範如何啟用 mipmap 材質篩選。


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



您的應用程式也可以使用 [**IDirect3DTexture9：： GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) 方法，並指定要取出的 mipmap 層級，以手動方式進行一連串的 mipmap 表面。 下列範例會將 mipmap 鏈從最高到最低的解析度。


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



應用程式需要手動遍歷 mipmap 鏈，以將點陣圖資料載入至鏈中的每個介面。 這通常是跨越鏈的唯一原因。 應用程式可以藉由呼叫 [**IDirect3DBaseTexture9：： GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount)來取出 mipmap 中的層級數目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質篩選](texture-filtering.md)
</dt> </dl>

 

 
