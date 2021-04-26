---
description: 零或多個鎖定選項的組合，用來描述要執行的鎖定類型。
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999425"
---
# <a name="d3dlock"></a>D3DLOCK

零或多個鎖定選項的組合，用來描述要執行的鎖定類型。



| \#定義                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ 捨棄           | 應用程式會捨棄鎖定區域內的所有記憶體。 針對頂點和索引緩衝區，將會捨棄整個緩衝區。 只有在使用動態使用方式建立資源時，此選項才有效 (請參閱 [D3DUSAGE](d3dusage.md)) 。                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | 允許應用程式在驅動程式無法立即鎖定介面時，取回 CPU 週期。 如果設定此旗標，且驅動程式無法立即鎖定介面，則鎖定呼叫會傳回 D3DERR \_ WASSTILLDRAWING。 只有在鎖定使用 [**CreateOffscreenPlainSurface**](/windows/desktop/api)、 [**CreateRenderTarget**](/windows/desktop/api)或 [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)所建立的介面時，才能使用此旗標。 此旗標也可以與背景緩衝區一起使用。            |
| D3DLOCK \_ 沒有 \_ 中途 \_ 更新 | 根據預設，資源的鎖定會將中途區域新增至該資源。 此選項可防止變更資源的變更狀態。 當應用程式具有在鎖定操作期間變更之區域集合的其他資訊時，應使用此選項。                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | 表示在鎖定期間，不會修改在繪圖呼叫中所參考的記憶體，因為沒有此旗標的最後一個鎖定將不會修改。 當應用程式將資料附加至資源時，這可以啟用優化。 如果資源正在使用中，則指定這個旗標可讓驅動程式立即傳回，否則，驅動程式必須在從鎖定傳回之前完成使用資源。                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | 視訊記憶體鎖定的預設行為是保留整個系統的重要區段，以保證鎖定期間不會發生任何顯示模式變更。 此選項會導致鎖定期間不保留整個系統的重要區段。<br/> 鎖定作業相當耗時，但可以讓系統執行其他任務，例如移動滑鼠游標。 此選項適用于長時間持續的鎖定，例如鎖定軟體轉譯的背景緩衝區，否則會對系統回應性造成負面影響。<br/> |
| D3DLOCK \_ READONLY          | 應用程式不會寫入緩衝區。 這可讓以非原生格式儲存的資源在解除鎖定時儲存 recompression 步驟。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>常數資訊



|                          |             |
|--------------------------|-------------|
| 標頭                   | d3d9types。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**鎖定**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**鎖定**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
