---
description: 資源管理是將資源從系統記憶體儲存體升級到可存取裝置的儲存體，並從裝置可存取的儲存體中捨棄的程式。
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: 管理 (Direct3D 9) 的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728461"
---
# <a name="managing-resources-direct3d-9"></a>管理 (Direct3D 9) 的資源

資源管理是將資源從系統記憶體儲存體升級到可存取裝置的儲存體，並從裝置可存取的儲存體中捨棄的程式。 Direct3D 執行時間有自己的管理演算法，以最少最近使用的優先順序技術為基礎。 當 Direct3D 偵測到的資源超過可在裝置可存取記憶體中並存的資源時，它會切換為最新使用的優先順序技術， [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 和 [**IDirect3DDevice9：： EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) 呼叫之間會使用這些資源。

在建立時使用 [**D3DPOOL \_ 預設**](./d3dpool.md) 旗標，指定將資源放在記憶體集區中，最適合指定資源所要求的一組使用方式。 這通常是視訊記憶體，包括本機視訊記憶體和高速圖形連接埠 (AGP) 記憶體。 預設集區中的資源不會透過裝置的遺失和操作狀態之間的轉換來保存。 這些資源必須在呼叫 reset 之前釋出，然後必須重新建立。

在建立時使用 [**D3DPOOL \_ managed**](./d3dpool.md) 旗標來指定受管理的資源。 受控資源會透過裝置的遺失和操作狀態之間的轉換來保存。 這些資源都存在於影片和系統記憶體中。 當轉譯時需要 managed 資源，它會複製到視頻記憶體中。 您可以使用 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)的呼叫來還原裝置，如此一來，這類資源仍可繼續正常運作，而不需要重載資料。 但是，如果必須終結並重新建立裝置，則必須重新建立所有資源。

對於變更頻率較高的資源，不建議使用資源管理。 例如，用來跨越場景圖形的頂點和索引緩衝區，每個畫面格只轉譯使用者可以看到的幾何變更每個畫面格。 因為受管理的資源是由系統記憶體所支援，所以必須在系統記憶體中更新常數的變更，這可能會導致效能嚴重降低。 在此特定案例中，應該使用 [**D3DPOOL \_ DEFAULT**](./d3dpool.md) 以及 [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) 。

不建議 (資源管理的另一個範例，且執行時間不會明確允許) 管理使用 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)所建立的材質。 如果轉譯目標所使用的記憶體是由執行時間所管理，則在轉譯期間可能需要持續將內容複寫到系統記憶體，造成效能大幅下降。 基於這個理由，您必須在預設集區中建立呈現目標。 如果需要包含在轉譯目標中之資料的 CPU 存取，則必須將資料複製到使用 [**IDirect3DDevice9：： UpdateTexture**](/windows/desktop/api)或 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)在 [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md)中建立的資源。

如需裝置遺失狀態的詳細資訊，請參閱 [ (Direct3D 9) 的遺失裝置 ](lost-devices.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> </dl>

 

 
