---
description: 使用 (Direct3D 9) 的壓縮紋理
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: 使用 (Direct3D 9) 的壓縮紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f506cef8147ee5ef1fb0c99cf862254564240bb112e954884cc7a2a07d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044016"
---
# <a name="using-compressed-textures-direct3d-9"></a>使用 (Direct3D 9) 的壓縮紋理

## <a name="determining-support-for-compressed-textures"></a>判斷支援壓縮的材質

若要測試介面卡，請指定任何使用 DXT1、DXT2、DXT3、DXT4 或 DXT5 的像素格式。 如果 [**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 傳回 D3D \_ OK，則裝置可以直接從使用該格式的壓縮紋理介面建立紋理。 若是如此，您可以藉由呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，直接透過 Direct3D 使用壓縮的材質介面。 下列程式碼範例顯示如何判斷介面卡是否支援壓縮的材質格式。


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



如果裝置不支援從壓縮的材質表面進行紋理，您仍然可以將材質資料儲存為壓縮格式介面，但您必須先將任何壓縮紋理轉換成支援的格式，才能將其用於紋理。

## <a name="creating-compressed-textures"></a>建立壓縮的材質

在介面卡上建立支援壓縮材質格式的裝置之後，您就可以建立壓縮的材質資源。 呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ，並針對 format 參數指定壓縮的材質格式。

將影像載入材質物件之前，請呼叫 [**IDirect3DTexture9：： GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) 方法，以取出紋理介面的指標。

現在您可以使用任何 D3DXLoadSurfacexxx 函式，將影像載入至使用 [**IDirect3DTexture9：： GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)所抓取的介面。 這些函式會處理壓縮材質格式的轉換。

您可以使用 [DirectX 材質編輯器] (Dxtex.exe) 隨附于 DirectX SDK，來建立和轉換壓縮的材質 (DDS) 檔。 您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

這種行為的優點是，應用程式可以將壓縮表面的內容複寫到檔案中，而不需要計算特定格式的特定寬度和高度的介面需要多少儲存空間。

下表顯示五種類型的壓縮紋理。 如需有關如何儲存資料的詳細資訊，請參閱 [ (Direct3D 9) 壓縮的材質格式 ](compressed-texture-formats.md)。 如果您要撰寫自己的壓縮常式，則只需要此資訊。



| FOURCC | 描述        | Alpha 預乘？ |
|--------|--------------------|----------------------|
| DXT1   | 不透明/1 位 Alpha | N/A                  |
| DXT2   | 明確 Alpha     | Yes                  |
| DXT3   | 明確 Alpha     | No                   |
| DXT4   | 插補 Alpha | Yes                  |
| DXT5   | 插補 Alpha | No                   |



 

當您將資料從 nonpremultiplied 格式傳送到預先設置的格式時，Direct3D 會根據 Alpha 值調整色彩。 不支援將資料從預乘格式傳送至 nonpremultiplied 格式。 如果您嘗試將資料從預乘的 Alpha 來源傳送至 nonpremultiplied Alpha 目的地，則此方法會傳回 D3DERR \_ INVALIDCALL。 如果您將資料從預乘的 Alpha 來源傳送至沒有 Alpha 的目的地，則會依原樣複製來源色彩元件（已透過 Alpha 調整）。

## <a name="decompressing-compressed-texture-surfaces"></a>解壓縮壓縮的材質表面

就像壓縮材質介面一樣，解壓縮壓縮的材質是透過 Direct3D 複製服務來執行。

若要將壓縮的材質介面複製到未壓縮的材質介面，請使用函數 [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)。 此函式會處理壓縮和未壓縮表面的壓縮。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[壓縮的材質資源](compressed-texture-resources.md)
</dt> </dl>

 

 
