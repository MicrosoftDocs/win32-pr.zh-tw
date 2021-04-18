---
description: 將 IDirect3DDevice9：： CreateVertexBuffer 方法的 FVF 參數設定為非零值（必須是有效的 FVF 碼），表示緩衝區內容是以 FVF 程式碼為特徵。
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: FVF (Direct3D 9) 的頂點緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971275"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>FVF (Direct3D 9) 的頂點緩衝區

將 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/desktop/api) 方法的 FVF 參數設定為非零值（必須是有效的 FVF 碼），表示緩衝區內容是以 FVF 程式碼為特徵。 使用 FVF 程式碼建立的頂點緩衝區稱為 FVF 頂點緩衝區。 某些方法或使用 [**IDirect3DDevice9**](/windows/desktop/api) 需要 FVF 頂點緩衝區，而其他方法則需要非 FVF 的頂點緩衝區。 FVF 頂點緩衝區必須是 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)的目的地頂點緩衝區引數。

FVF 頂點緩衝區可以系結至任何資料流程編號的來源資料流。

\_FVF 頂點緩衝區上的 D3DFVF XYZRHW 元件是否存在，表示該緩衝區中的頂點已經過處理。 用於 IDirect3DDevice9 的頂點緩衝區 [**：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 目的地頂點緩衝區必須經過後置處理。 用於固定函式著色器輸入的頂點緩衝區可以是前置處理或 postprocessed。 如果頂點緩衝區經過處理後，則會有效地略過著色器，並將資料直接傳遞至基本剪切和設定模組。

FVF 頂點緩衝區可以搭配頂點著色器使用。 此外，頂點資料流程也可以代表非 FVF 頂點緩衝區可以有的相同頂點格式。 它們不需要用來輸入來自不同頂點緩衝區的資料。 新頂點資料流程的額外彈性可讓需要保持資料不同的應用程式能夠更妥善地運作，但這並不是必要的。 如果應用程式可以事先維護交錯的資料，就能提升效能。 如果應用程式只會在每次轉譯呼叫之前交錯資料，則應該啟用 API 或硬體以使用多個資料流程來進行這項作業。

頂點效能最重要的事項是使用32位元組頂點，並維護良好的快取順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
