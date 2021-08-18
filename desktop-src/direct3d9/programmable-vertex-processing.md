---
description: 使用程式設計頂點著色器時，在目的地頂點緩衝區中更新的元素是由著色器函式程式所控制。
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: " (Direct3D 9) 的可程式化頂點處理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118588"
---
# <a name="programmable-vertex-processing-direct3d-9"></a> (Direct3D 9) 的可程式化頂點處理

使用程式設計頂點著色器時，在目的地頂點緩衝區中更新的元素是由著色器函式程式所控制。 當應用程式寫入其中一個目的地頂點暫存器時，會更新目的地頂點緩衝區中每個頂點內的對應元素。 不會修改目的地頂點緩衝區中不是由應用程式寫入的元素。 [**IDirect3DDevice9：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 如果應用程式寫入的專案不存在於目的地頂點緩衝區中，:P rocessvertices 將會失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
