---
description: 下列旗標是用來將 sprite 轉譯選項指定至 Begin 方法中的 flags 參數：
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e2247f414636039906277f882fb9dfc95f6b6b33aa29de2ac51a722c045901
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749758"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

下列旗標是用來將 sprite 轉譯選項指定至 [**Begin**](id3dxsprite--begin.md) 方法中的 flags 參數：



| \#定義                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | 呼叫 [**Begin**](id3dxsprite--begin.md) 或 [**End**](id3dxsprite--end.md) 時，不會儲存或還原裝置狀態。                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | 呼叫 [**Begin**](id3dxsprite--begin.md) 時，不會變更裝置呈現狀態。 裝置會假設為有效的狀態，以在 D3DDECLUSAGE \_ 位置、D3DDECLUSAGE \_ TEXCOORD 和 D3DDECLUSAGE 色彩資料中繪製包含 UsageIndex = 0 的頂點 \_ 。                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | 不會修改世界、觀點和投射轉換。 目前設定為裝置的轉換是用來在)  (排 [**清或結束時繪製**](id3dxsprite--flush.md) 批次後 [**端**](id3dxsprite--end.md) 時，用來轉換 sprite。 如果未指定此旗標，則會修改 [world]、[view] 和 [投射] 轉換，以便在螢幕空間座標中繪製 sprite。              |
| D3DXSPRITE \_ 佈告欄                | 每個 sprite 都會旋轉其中心，使其面對檢視器。 必須先呼叫 [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md)或 [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) 。                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | 啟用 \_ 將 D3DRS ALPHATESTENABLE 設定為 **TRUE** (非零 Alpha) 的 Alpha 混色。 D3DBLEND \_ SRCALPHA 將會是來源 blend 狀態，而 D3DBLEND \_ INVSRCALPHA 將是呼叫 [**graphicsdevice**](/windows/desktop/api)時的目的地 blend 狀態。 請參閱 [ (Direct3D 9) 的 Alpha 混色狀態 ](alpha-blending-state.md)。 [**ID3DXFont**](id3dxfont.md) 需要在繪製文字時設定此旗標。 |
| D3DXSPRITE \_ 排序 \_ 材質            | 在繪圖之前依材質排序子動畫。 這可在繪製非重迭的統一深度 sprite 時改善效能。 您也可以結合 D3DXSPRITE \_ 排序 \_ 材質與 D3DXSPRITE \_ 排序 \_ 深度 \_ FRONTTOBACK 或 D3DXSPRITE \_ 排序 \_ 深度 \_ BACKTOFRONT。 這會依深度的第一層和材質秒排序子清單。<br/>                                                                           |
| D3DXSPRITE \_ 排序 \_ 深度 \_ FRONTTOBACK | 在繪圖之前，會依深度以深度順序來排序 sprite。 當您繪製不同深度的不透明 sprite 時，建議使用此程式。 您可以結合 D3DXSPRITE \_ 排序 \_ 深度 \_ FRONTTOBACK 與 D3DXSPRITE \_ 排序 \_ 材質，以依深度和第二個材質進行排序。<br/>                                                                                                                                   |
| D3DXSPRITE \_ 排序 \_ 深度 \_ BACKTOFRONT | 在繪圖之前，會依深度以深度順序排序 sprite。 當您繪製不同深度的透明 sprite 時，建議使用此程式。 您可以結合 D3DXSPRITE \_ 排序 \_ 深度 \_ BACKTOFRONT 與 D3DXSPRITE \_ 排序 \_ 材質，以依深度和第二個材質進行排序。<br/>                                                                                                                              |
| D3DXSPRITE \_ 不 \_ \_ ADDREF \_ 材質 | 在每次繪製時停用呼叫 AddRef () ，並在排清 () 釋放 () ，以獲得更好的效能。                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值            |
|--------------------------|-------------|
| 標頭                   | d3dx9core。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 常數](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




