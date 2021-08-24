---
description: 您可以藉由呼叫 CreateCubeTexture 方法來建立三個環境的地圖紋理。 三種環境對應紋理必須是正方形，而維度則是2的乘冪。
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: " (Direct3D 9) 建立三個環境的地圖表面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b37321978a40170d47718318e4b3f6898ba04d5fa229e97ada47e08e589fdcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608018"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a> (Direct3D 9) 建立三個環境的地圖表面

您可以藉由呼叫 [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) 方法來建立三個環境的地圖紋理。 三種環境對應紋理必須是正方形，而維度則是2的乘冪。

下列程式碼範例會示範 c + + 應用程式如何建立簡單的三立方環境對應。


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>存取三立方環境地圖臉部

您可以使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 方法，在三個平面環境圖的臉部之間流覽。

下列程式碼範例會使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 來抓取適用于正 y 臉部 (臉部 2) 的立方體地圖介面。


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



[**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)所接受的第一個參數是 [**D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md)列舉值，可描述方法應取得的附加介面。 第二個參數會告訴 Direct3D 要取出的 mipmapped cube 材質層級。 所接受的第三個參數是 [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) 介面的位址，代表傳回的 cube 紋理介面。 因為此 cube 對應不是 mipmapped，所以在這裡使用0。

> [!Note]
>
> 呼叫這個方法之後， [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) 介面上的內部參考計數會增加。 當您使用此介面完成時，請務必在這個 **IDirect3DSurface9** 介面上呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法，否則會發生記憶體流失。

 

## <a name="rendering-to-cubic-environment-maps"></a>轉譯為立方環境地圖

您可以將影像複製到 cube 地圖的個別臉部，就像是任何其他材質或 surface 物件一樣。 轉譯為臉部之前，最重要的一件事是設定轉換矩陣，讓相機正確定位，並以適當的方向指向該臉部：向前 (+ z) 、向後 (-z) 、左方 ( x) 、右 (+ x) 、向上 (+ y) ，或向下 (-y) 。

下列 c + + 程式碼範例會根據所呈現的臉部來準備和設定視圖矩陣。


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



請記住，每個三面的環境對應都代表一個90度的觀點。 除非您的應用程式需要不同的視圖角度欄位-例如特殊效果，否則請小心地設定投影矩陣。

這個程式碼範例會建立並設定最常見案例的投射矩陣。


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



當相機在位置，以及投影矩陣集時，您可以呈現場景。 場景中的每個物件都應該以您通常放置它們的位置來定位。 下列程式碼範例（針對完整性提供）會概述這項工作。


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



請注意 [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) 方法的呼叫。 當轉譯為立方體地圖臉部時，您必須將臉部指派為目前的呈現目標介面。 使用深度緩衝區的應用程式可以明確地建立呈現目標的深度緩衝區，或將現有的深度緩衝區重新指派給呈現目標介面。 上述程式碼範例使用第二種方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[三次環境對應](cubic-environment-mapping.md)
</dt> </dl>

 

 
