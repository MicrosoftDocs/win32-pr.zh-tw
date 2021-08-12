---
description: 狀態欄塊可以用來捕捉所有裝置狀態 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: 以 StateBlock (Direct3D 9) 儲存所有裝置狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520079"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>以 StateBlock (Direct3D 9) 儲存所有裝置狀態

狀態欄塊可以用來捕捉所有裝置狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。 裝置狀態包含下列狀態元素：

-   頂點狀態 (請參閱 [使用 StateBlock (Direct3D 9) ) 儲存頂點狀態 ](saving-vertex-states-with-a-stateblock.md) 。
-   圖元狀態 (請參閱 [使用 StateBlock (Direct3D 9) ) 儲存圖元狀態 ](saving-pixel-states-with-a-stateblock.md) 。
-   每個指派給取樣器的材質。
-   每個頂點材質。
-   每個置換地圖材質。
-   目前的材質調色板。
-   針對每個頂點資料流程：指向頂點緩衝區的指標、來自 [**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api)的每個引數，以及從 [**IDirect3DDevice9：： SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq)取得的任何) 的分隔 (。
-   索引緩衝區的指標。
-   視口。
-   剪刀矩形。
-   世界、視野和投射矩陣。
-   紋理轉換。
-   如果有任何) ，裁剪平面就 (。
-   目前的材質。

若要使用狀態欄塊來捕捉所有裝置狀態，請 \_ 在呼叫 [**IDirect3DDevice9：： CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)時指定 D3DSBT all。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態欄塊儲存與還原狀態](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
