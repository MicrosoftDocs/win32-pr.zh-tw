---
description: Array.blit 一詞是 &\# 0034; bit block transfer 的速記，&\# 0034; 這是將資料區塊從記憶體中的一個位置傳送到另一個位置的進程。
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: " (Direct3D 9) 複製表面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970112"
---
# <a name="copying-surfaces-direct3d-9"></a> (Direct3D 9) 複製表面

詞彙 array.blit 是「位區塊傳輸」的縮寫，這是將資料區塊從記憶體中的一個位置傳送到另一個位置的程式。 Blitting 設備磁碟機介面 (DDI) 繼續在 Direct3D 9 中用來做為每個框架移動大型矩形的主要機制，也就是複製導向 IDirect3DDevice9 背後的機制 [**：:P 重發**](/windows/desktop/api) 的方法。 Array.blit 作業中的圖稿傳輸是由 [**IDirect3DDevice9：： UpdateTexture**](/windows/desktop/api) 方法所執行。 您也可以使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) 方法（複製圖元的矩形子集），在 Direct3D 9 中複製作品。

> [!Note]  
> Direct3D 9 提供 D3DX 函式，可讓您從檔案載入圖片、套用色彩轉換，以及調整圖形大小。 如需可用函式的詳細資訊，請參閱 [D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
