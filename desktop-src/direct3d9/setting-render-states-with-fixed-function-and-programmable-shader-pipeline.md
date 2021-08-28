---
title: 設定固定函式、著色器管線上的裝置狀態
description: 本節提供使用固定函式和可程式化著色器管線來設定裝置狀態兩者之間的主要差異。
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d0ddc6b6a58e7bee3e141d84e79328a911f152a3536aa1696c73a503db4db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092255"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>設定固定函式、著色器管線上的裝置狀態

本節提供使用固定函式和可程式化著色器管線來設定裝置狀態兩者之間的主要差異。

以下是您可以僅針對固定函式管線設定的裝置狀態：

-   固定函式轉換和光源： [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)與 D3DRS \_ SHADEMODE、D3DRS \_ SPECULARENABLE、D3DRS \_ 光源、D3DRS \_ 環境、D3DRS \_ COLORVERTEX、D3DRS LOCALVIEWER \_ 、D3DRS \_ NORMALIZENORMALS、D3DRS \_ DIFFUSEMATERIALSOURCE、D3DRS SPECULARMATERIALSOURCE、D3DRS \_ \_ AMBIENTMATERIALSOURCE \_ \_ \_ \_ [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 、D3DRS EMISSIVEMATERIALSOURCE、D3DRS VERTEXBLEND、D3DRS INDEXEDVERTEXBLENDENABLE、D3DRS TWEENFACTOR、IDirect3DDevice9：： LightEnable、IDirect3DDevice9：： MultiplyTransform、IDirect3DDevice9：： SetFVF、IDirect3DDevice9：： SetLight、IDirect3DDevice9：： SetMaterial、IDirect3DDevice9：： SetTransform
-   Fixed 函式圖元著色器： [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) with D3DRS \_ TEXTUREFACTOR， [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   霧化： [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 與 D3DRS \_ FOGENABLE、D3DRS \_ FOGCOLOR、D3DRS \_ FOGTABLEMODE、D3DRS \_ FOGSTART、D3DRS \_ FOGEND、D3DRS \_ FOGDENSITY、D3DRS \_ RANGEFOGENABLE、D3DRS \_ FOGVERTEXMODE

以下是您可以使用 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 為固定函式和可程式化著色器管線設定的裝置轉譯狀態：

-   轉譯目標狀態： D3DRS \_ COLORWRITEENABLE、D3DRS \_ COLORWRITEENABLE1、D3DRS \_ COLORWRITEENABLE2、D3DRS \_ COLORWRITEENABLE3、D3DRS \_ SRGBWRITEENABLE
-   深度狀態： D3DRS \_ ZENABLE、D3DRS \_ ZWRITEENABLE、D3DRS \_ ZFUNC、D3DRS \_ SLOPESCALEDEPTHBIAS、D3DRS \_ DEPTHBIAS
-   樣板狀態： D3DRS \_ STENCILENABLE、D3DRS \_ STENCILFAIL、D3DRS \_ STENCILZFAIL、D3DRS \_ STENCILPASS、D3DRS \_ STENCILFUNC、D3DRS \_ STENCILREF、D3DRS \_ STENCILMASK、D3DRS \_ STENCILWRITEMASK、D3DRS \_ TWOSIDEDSTENCILMODE、D3DRS \_ ccw \_ STENCILFAIL、D3DRS \_ ccw STENCILZFAIL \_ 、D3DRS \_ ccw \_ STENCILPASS、D3DRS \_ ccw \_ STENCILFUNC
-   Alpha 混色： D3DRS \_ SRCBLEND、D3DRS \_ DESTBLEND、D3DRS \_ BLENDOP、D3DRS \_ BLENDFACTOR、D3DRS \_ SEPARATEALPHABLENDENABLE、D3DRS \_ SRCBLENDALPHA、D3DRS \_ DESTBLENDALPHA、D3DRS \_ BLENDOPALPHA
-   Alpha 測試： D3DRS \_ ALPHATESTENABLE、D3DRS \_ ALPHAREF、D3DRS \_ ALPHAFUNC
-   轉譯器狀態： D3DRS \_ FILLMODE、D3DRS \_ LASTPIXEL、D3DRS \_ DITHERENABLE (16 位表面) 
-   剔除： D3DRS \_ CULLMODE
-   裁剪： D3DRS \_ 剪切、D3DRS \_ CLIPPLANEENABLE
-   剪刀： D3DRS \_ SCISSORTESTENABLE
-   紋理取樣器： D3DRS \_ WRAP0、D3DRS \_ WRAP1、D3DRS \_ WRAP2、D3DRS \_ WRAP3、D3DRS \_ WRAP4、D3DRS \_ WRAP5、D3DRS \_ WRAP6、D3DRS WRAP7、 \_ D3DRS \_ WRAP8 \_ \_ \_ \_ \_ \_ \_ 、D3DRS WRAP9、D3DRS WRAP10、D3DRS WRAP11、D3DRS WRAP12、D3DRS WRAP13、D3DRS WRAP14、D3DRS WRAP15
-   消除鋸齒： D3DRS \_ MULTISAMPLEANTIALIAS、D3DRS \_ MULTISAMPLEMASK、D3DRS \_ ANTIALIASEDLINEENABLE
-   點 sprite： D3DRS \_ dialog、D3DRS \_ dialog \_ MIN、D3DRS \_ POINTSPRITEENABLE、D3DRS \_ dialog \_ MAXD3DRS \_ POINTSCALEENABLE、D3DRS \_ POINTSCALE \_ A、D3DRS \_ POINTSCALE \_ B、D3DRS \_ POINTSCALE \_ C
-   N 修補程式： D3DRS \_ PATCHEDGESTYLE、D3DRS \_ POSITIONDEGREE、D3DRS \_ NORMALDEGREE、D3DRS \_ MINTESSELLATIONLEVEL、D3DRS \_ MAXTESSELLATIONLEVEL、D3DRS \_ ADAPTIVETESS \_ X、D3DRS \_ ADAPTIVETESS \_ Y、D3DRS \_ ADAPTIVETESS \_ Z、D3DRS \_ ADAPTIVETESS \_ W、D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 
