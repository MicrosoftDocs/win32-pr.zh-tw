---
description: 使用 IDirect3DDevice9：： UpdateSurface 時，請在來源介面上傳遞矩形，或使用 Null 來指定整個表面。
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: 複製到 (Direct3D 9) 的表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28a8518f0792948af7aabda269fffe9679de2c6fc704ee93e2cf05381176b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989288"
---
# <a name="copying-to-surfaces-direct3d-9"></a>複製到 (Direct3D 9) 的表面

使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)時，請在來源介面上傳遞矩形，或使用 **Null** 來指定整個表面。 您也可以在目的地介面上傳遞點，以複製來源影像上的矩形左上角位置。 這個方法不支援裁剪。 除非來源矩形和對應的目的矩形分別包含在來源和目的介面內，否則作業將會失敗。 這個方法不支援 Alpha 混色、色彩按鍵或格式轉換。 請注意，目的地和來源表面必須是相異的。

如需使用 UpdateSurface 的其他限制，請參閱 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)。

C + +/C 也提供下列方法，可將影像複製到 Direct3D 介面。

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>UpdateSurface 範例

下列範例會將兩個矩形從來源介面複製到目的介面。 第一個矩形會從來源介面上的 (0、0、50、50) 複製到目的地介面上的相同位置，而第二個矩形會從來源介面上 (50、50、100、100) 複製到目的介面上的 (150、150、200、200) 。


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
