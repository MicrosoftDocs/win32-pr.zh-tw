---
description: 從頂點緩衝區轉譯頂點資料需要執行幾個步驟。 首先，您必須呼叫 IDirect3DDevice9：： SetStreamSource 方法來設定資料流程來源，如下列範例所示。
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: '從頂點緩衝區轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ee3d477fc812d2dabed765e28bb14452a6badf746a331a13283108ef46b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520069"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>從頂點緩衝區轉譯 (Direct3D 9) 

從頂點緩衝區轉譯頂點資料需要執行幾個步驟。 首先，您必須呼叫 [**IDirect3DDevice9：： SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) 方法來設定資料流程來源，如下列範例所示。


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



[**IDirect3DDevice9：： SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)的第一個參數會告訴 Direct3D 該裝置資料流程的來源。 第二個參數是要系結至資料流程的頂點緩衝區。 第三個參數是從資料流程開頭到頂點資料開頭的位移（以位元組為單位）。 第四個參數是元件的 stride （以位元組為單位）。 在上述的範例程式碼中，CUSTOMVERTEX 的大小會用於元件的 stride。

下一步是透過呼叫 [**IDirect3DDevice9：： SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 方法，通知 Direct3D 要使用哪個頂點著色器。 下列範例程式碼會設定頂點著色器的 FVF 碼。 這會通知 Direct3D 其正在處理的頂點類型。


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



設定資料流程來源和頂點著色器之後，任何繪製方法都將使用頂點緩衝區。 下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法，從頂點緩衝區轉譯頂點。


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



[**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)所接受的第二個參數是要載入之頂點緩衝區中第一個向量的索引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> <dt>

[從頂點和索引緩衝區轉譯 (Direct3D 9) ](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
