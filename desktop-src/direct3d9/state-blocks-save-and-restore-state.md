---
description: 狀態欄塊是裝置狀態的群組。
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: '狀態欄塊儲存和還原狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935618"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>狀態欄塊儲存和還原狀態 (Direct3D 9) 

狀態欄塊是裝置狀態的群組。 裝置狀態是由呈現狀態、頂點狀態、圖元狀態或上述所有內容所組成。 狀態欄塊包含裝置目前狀態的快照，您也可以建立狀態欄塊來記錄應用程式所進行的每個狀態變更。

## <a name="capture-a-block-of-state"></a>捕捉狀態的區塊

選擇您想要捕捉的狀態類型，並建立如下的狀態欄塊：


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9：： CreateStateBlock**](/windows/desktop/api) 會建立狀態欄塊，並自動捕獲裝置狀態。 裝置狀態是由第一個引數中的狀態欄塊類型所指定。 此狀態可以是下列其中一項：所有裝置狀態 (參閱將 [所有裝置狀態儲存為 StateBlock (direct3d 9) ](saving-all-device-states-with-a-stateblock.md)) 、所有圖元狀態 (請參閱 [將圖元狀態儲存為 StateBlock (direct3d 9) ](saving-pixel-states-with-a-stateblock.md)) 或所有頂點狀態 (請參閱 [使用 StateBlock (Direct3d 9) ) 儲存頂點 ](saving-vertex-states-with-a-stateblock.md) 狀態。

效果系統會使用狀態欄塊來儲存狀態。 呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 之後，會建立狀態欄塊並捕獲狀態。 呼叫 [**ID3DXEffect：： End**](id3dxeffect--end.md) 時，會將狀態欄塊狀態重新套用至裝置。

## <a name="capture-individual-states"></a>捕捉個別狀態

若要儲存自訂狀態順序，請將您要儲存的狀態包裝在 [**IDirect3DDevice9：： BeginStateBlock**](/windows/desktop/api) 和 [**IDirect3DDevice9：： EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) 配對中。 BeginStateBlock 會告知目前裝置設定狀態欄塊，並將其新增至在呼叫 EndStateBlock 之前發生的每個狀態變更。 以下為範例：


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



這會以任何順序將任何數目的狀態變更儲存至自訂 stateblock。 稍後，當您想要使用 stateblock 來重設裝置狀態時，請呼叫 [**IDirect3DStateBlock9：： Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply)。 這只會覆寫狀態欄塊中已捕捉的裝置狀態。 未使用自訂 stateblock 所捕捉的任何其他裝置狀態都不會變更。 同樣地，由於 stateblock 物件是介面，因此您必須在完成時將它釋放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態 (Direct3D 9) ](states.md)
</dt> </dl>

 

 
