---
description: ID3DXSprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: 'ID3DXSprite 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d5786096fb9c38188d73d613fd11efd97c2401e9f8ae9c7eb4a05dfe1dc1e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729244"
---
# <a name="id3dxsprite-interface"></a>ID3DXSprite 介面

ID3DXSprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。

## <a name="members"></a>成員

**ID3DXSprite** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXSprite** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXSprite** 介面具有這些方法。



| 方法                                                | 描述                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**開始**](id3dxsprite--begin.md)                   | 準備裝置以繪製 sprite。<br/>                                                                                                                                                                            |
| [**Draw**](id3dxsprite--draw.md)                     | 將 sprite 新增至批次 sprite 的清單。<br/>                                                                                                                                                                     |
| [**結束**](id3dxsprite--end.md)                       | 呼叫 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md) ，然後將裝置狀態還原為 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md) 之前的狀態。<br/>                                            |
| [**清除**](id3dxsprite--flush.md)                   | 強制將所有批次中的 sprite 提交至裝置。 裝置狀態會維持在最後一次呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)之後。 然後會清除批次中的子後 sprite 清單。<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | 捕獲與 sprite 物件相關聯的裝置。<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | 取得 sprite 轉換。<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | 設定 sprite 轉換。<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | 為 sprite 設定左手的世界視圖轉換。 在 billboarding 或排序 sprite 之前，需要呼叫此方法。<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | 為 sprite 設定右手的世界視圖轉換。 在 billboarding 或排序 sprite 之前，需要呼叫此方法。<br/>                                                                                |



 

## <a name="remarks"></a>備註

**ID3DXSprite** 介面是藉由呼叫 [**D3DXCreateSprite**](d3dxcreatesprite.md)函數來取得。

應用程式通常會先呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)，以便控制裝置轉譯狀態、Alpha 混色和 sprite 轉換和排序。 然後，針對每個要顯示的 sprite，呼叫 [**ID3DXSprite：:D raw**](id3dxsprite--draw.md)。 **ID3DXSprite：:D raw** 可以重複呼叫，以儲存任何數目的 sprite。 若要對裝置顯示批次的分次，請呼叫 [**ID3DXSprite：： End**](id3dxsprite--end.md) 或 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md)。

LPD3DXSPRITE 型別定義為 **ID3DXSprite** 介面的指標。


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
