---
description: 頂點緩衝區物件可讓應用程式直接存取配置給頂點資料的記憶體。
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: '存取頂點緩衝區的內容 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973580"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>存取頂點緩衝區的內容 (Direct3D 9) 

頂點緩衝區物件可讓應用程式直接存取配置給頂點資料的記憶體。 您可以藉由呼叫 [**IDirect3DVertexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) 方法來取得頂點緩衝區記憶體的指標，然後視需要存取記憶體，以使用新的頂點資料填滿緩衝區，或讀取它已包含的任何資料。 **IDirect3DVertexBuffer9：： Lock** 方法接受四個參數。 第一個 *OffsetToLock* 是頂點資料中的位移。 第二個參數是頂點資料的大小（以位元組為單位）。 如果呼叫成功，則接受的第三個參數是指向頂點資料之指標的位址。

最後一個參數 *旗標* 會告知系統應該如何鎖定記憶體。 根據將存取頂點資料的方式，指定 *旗標* 參數的常數。 請確定為 [**D3DUSAGE**](d3dusage.md) 選擇的值符合為 [D3DLOCK](d3dlock.md)選擇的值。 例如，如果您要建立僅具有寫入存取權的頂點緩衝區，請指定 D3DLOCK READONLY 來嘗試讀取資料並不合理 \_ 。 明智地使用這些旗標，可讓驅動程式鎖定記憶體，並提供最佳效能，並提供所要求的存取類型。

當您完成填滿或讀取頂點資料之後，請呼叫 [**IDirect3DVertexBuffer9：： Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) 方法，如下列程式碼範例所示。


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



如果您使用 D3DUSAGE WRITEONLY 旗標建立頂點緩衝區 \_ ，請勿使用 D3DLOCK \_ READONLY 鎖定旗標。 \_如果您的應用程式只會從頂點緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。 包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。

如 [](performance-optimizations.md)需針對 \_ \_ [**IDirect3DVertexBuffer9：： LOCK**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)的 FLAGS 參數使用 D3DLOCK 捨棄或 D3DLOCK NOOVERWRITE 的相關資訊，請參閱使用動態頂點和索引緩衝區。

在 c + + 中，因為您直接存取配置給頂點緩衝區的記憶體，請確定您的應用程式能正確地存取配置的記憶體。 否則，您會面臨轉譯記憶體不正確風險。 使用您的應用程式用來從配置緩衝區中的一個頂點移至另一個頂點的頂點格式跨距。 頂點緩衝區記憶體是在 FVF 中指定的簡單頂點陣列。 使用您定義的任何頂點格式結構的 stride。 您可以藉由檢查頂點緩衝區描述中包含的 [D3DFVF](d3dfvf.md) ，在執行時間計算每個頂點的 stride。 下表顯示每個頂點元件的大小。



| 頂點格式旗標 | 大小              |
|--------------------|-------------------|
| D3DFVF \_ 擴散    | sizeof (DWORD)      |
| D3DFVF \_ 正常     | sizeof (float) x 3 |
| D3DFVF \_ 反光   | sizeof (DWORD)      |
| D3DFVF \_ TEXn       | sizeof (float) x n |
| D3DFVF \_ XYZ        | sizeof (float) x 3 |
| D3DFVF \_ XYZRHW     | sizeof (float) x 4 |



 

頂點格式所呈現的材質座標數目是由 D3DFVF \_ TEX n 旗標所描述， (其中 n 是介於0到 8) 的值。 將材質座標集合的數目乘以一組材質座標的大小，其範圍從一到四個浮點數，以計算該紋理座標數目所需的記憶體。

使用總頂點跨距來視需要遞增和遞減記憶體指標，以存取特定頂點。

## <a name="retrieving-vertex-buffer-descriptions"></a>正在抓取頂點緩衝區描述

您可以藉由呼叫 [**IDirect3DVertexBuffer9：： GetDesc**](/windows/desktop/api) 方法，來取得頂點緩衝區的相關資訊。 這個方法會以頂點緩衝區的相關資訊來填滿 [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) 結構的成員。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
