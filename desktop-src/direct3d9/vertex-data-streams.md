---
description: Direct3D 的轉譯介面包含從儲存在一或多個資料緩衝區中的頂點資料轉譯基本的方法。
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: " (Direct3D 9) 的頂點資料流程"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687728"
---
# <a name="vertex-data-streams-direct3d-9"></a> (Direct3D 9) 的頂點資料流程

Direct3D 的轉譯介面包含從儲存在一或多個資料緩衝區中的頂點資料轉譯基本的方法。 頂點資料是由結合至表單頂點元件的頂點元素所組成。 頂點元素是頂點的最小單位，代表位置、標準或色彩等實體。

頂點元件是一個或多個頂點元素，會連續儲存 (交錯的單一記憶體緩衝區中的每個頂點) 。 完整頂點是由一或多個元件所組成，其中每個元件都在不同的記憶體緩衝區中。 為了轉譯基本型別，會讀取和組合多個頂點元件，以便讓頂點處理有完整的頂點。 下圖顯示使用頂點元件呈現基本專案的程式。

![使用頂點元件呈現基本專案的程式圖](images/vertexdata.png)

轉譯基本專案是由兩個步驟所組成。 首先，設定一個或多個頂點元件資料流程;其次，叫用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法從這些資料流程轉譯。 端點著色器會指定這些元件資料流程內頂點元素的識別。

[**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)方法會指定頂點資料流程中的位移，如此一來，就可以在每個繪製調用中轉譯一組頂點資料內的任意連續子集。 這可讓您在從相同頂點緩衝區轉譯的基本群組之間變更裝置呈現狀態。

支援索引和非索引的繪圖方法。 如需詳細資訊，請參閱 [從頂點和索引緩衝區轉譯 (Direct3D 9) ](rendering-from-vertex-and-index-buffers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現基本專案](rendering-primitives.md)
</dt> </dl>

 

 
