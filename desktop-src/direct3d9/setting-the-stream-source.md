---
description: IDirect3DDevice9：： SetStreamSource 方法會將頂點緩衝區系結至裝置資料流程，建立頂點資料與饋送基本處理函式的數個數據流埠之一之間的關聯。
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: '設定串流來源 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510139"
---
# <a name="setting-the-stream-source-direct3d-9"></a>設定串流來源 (Direct3D 9) 

[**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api)方法會將頂點緩衝區系結至裝置資料流程，建立頂點資料與饋送基本處理函式的數個數據流埠之一之間的關聯。 在呼叫 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)之類的繪圖方法之前，不會發生資料流程資料的實際參考。

資料流程定義為元件資料的統一陣列，其中每個元件都包含一個或多個代表單一實體的元素，例如位置、正常、色彩等等。 Stride 參數指定元件的大小（以位元組為單位）。

下列程式碼示範如何設定資料流程來源和繪製其內容。 G \_ pVB 變數是包含頂點資料的 LPDIRECT3DVERTEXBUFFER9。


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



如需此程式碼的詳細資訊，請參閱下列教學課程： [教學課程3：使用矩陣](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現基本專案](rendering-primitives.md)
</dt> </dl>

 

 
