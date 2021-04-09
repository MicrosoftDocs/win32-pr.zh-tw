---
description: 深度緩衝區是裝置的屬性。 若要建立由 Direct3D 管理的深度緩衝區，請設定 D3DPRESENT 參數結構的適當成員， \_ 如下列程式碼範例所示。
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: " (Direct3D 9) 建立深度緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110273"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a> (Direct3D 9) 建立深度緩衝區

深度緩衝區是裝置的屬性。 若要建立由 Direct3D 管理的深度緩衝區，請設定 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 結構的適當成員，如下列程式碼範例所示。


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



藉由將 EnableAutoDepthStencil 成員設定為 **TRUE**，您可以指示 Direct3D 來管理應用程式的深度緩衝區。 請注意，AutoDepthStencilFormat 必須設定為有效的深度緩衝區格式。 D3DFMT \_ D16 旗標會指定16位的深度緩衝區（如果有的話）。

下列 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 方法呼叫會建立接著建立深度緩衝區的裝置。


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



深度緩衝區會自動設定為裝置的呈現目標。 當裝置重設時，會自動終結深度緩衝區，並重新建立新的大小。

若要建立新的深度緩衝區介面，請使用 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) 方法。

若要為裝置設定新的深度緩衝區介面，請使用 [**IDirect3DDevice9：： SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) 方法。

若要在您的應用程式中使用深度緩衝區，您必須啟用深度緩衝區。 如需詳細資訊，請參閱 [啟用 (Direct3D 9) 的深度緩衝 ](enabling-depth-buffering.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
