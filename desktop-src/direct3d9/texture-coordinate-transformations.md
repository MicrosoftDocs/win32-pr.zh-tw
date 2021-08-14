---
description: Direct3D 裝置可以套用4x4 矩陣來轉換頂點的材質座標。
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: " (Direct3D 9) 的材質座標轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984788"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a> (Direct3D 9) 的材質座標轉換

Direct3D 裝置可以套用4x4 矩陣來轉換頂點的材質座標。 系統會以與幾何相同的方式，將轉換套用至材質座標。 任何轉換 (縮放、旋轉、轉譯、投射、切變或這些) 的任何組合都可以使用4x4 矩陣來完成。

> [!Note]  
> Direct3D 不會修改轉換和亮頂點。 因此，使用已轉換和亮頂點的應用程式無法使用 Direct3D 來轉換頂點的材質座標。

 

支援硬體加速轉換和燈光作業 (T&L HAL 裝置的裝置) 也會加速紋理座標的轉換。 當轉換的硬體加速無法使用時，Direct3D 幾何管線中的平臺特定優化會套用至材質座標轉換。

材質座標轉換適用于產生特殊效果，而不需要直接修改幾何的材質座標。 您可以使用簡單的平移或旋轉矩陣來建立物件的材質動畫，也可以轉換由 Direct3D 自動產生的材質座標，以簡化並加速先進的效果，例如投影紋理和動態燈光對應。 此外，您也可以使用紋理座標轉換，在多個紋理階段中，重複使用一組紋理座標來進行多個用途。

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>設定和取出紋理座標轉換

如同應用程式用於幾何的矩陣，您可以藉由呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 和 [**IDirect3DDevice9：： GetTransform**](/windows/desktop/api) 方法來設定和取出紋理座標轉換。 這些方法會 \_ 透過 \_ [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 列舉型別的 D3DTS TEXTURE7 成員接受 D3DTS TEXTURE0，分別識別紋理階段0到7的轉換矩陣。

下列程式碼會設定要套用至材質階段0材質座標的矩陣。


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>啟用材質座標轉換

D3DTSS \_ TEXTURETRANSFORMFLAGS 材質階段狀態會控制材質座標轉換的應用。 這個紋理階段狀態的值是由 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 列舉類型所定義。

當 D3DTSS \_ TEXTURETRANSFORMFLAGS 設定為 D3DTTFF \_ DISABLE (預設值) 時，會停用材質座標轉換。 假設已針對階段0啟用紋理座標轉換，則下列程式碼會停用它們。


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



在 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 中定義的其他值會用來啟用材質座標轉換，以及控制將多少產生的材質座標元素傳遞給轉譯器。 例如，請採用下列程式碼。


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



D3DTTFF \_ COUNT2 值會指示系統套用紋理階段0的轉換矩陣集合，然後將修改過的材質座標的前兩個元素傳遞給轉譯器。

D3DTTFF \_ 投射的材質轉換旗標表示投射紋理的座標。 當指定這個旗標時，轉譯器會將傳入的元素除以最後一個元素。 例如，請採用下列程式碼。


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



此範例會通知系統將三個材質座標元素傳遞給轉譯器。 轉譯器會將前兩個專案除以第三個元素，以產生定址材質所需的2D 材質座標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質座標處理](texture-coordinate-processing.md)
</dt> </dl>

 

 
