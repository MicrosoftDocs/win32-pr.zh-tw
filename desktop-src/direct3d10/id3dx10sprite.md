---
description: ID3DX10Sprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。 這個介面可以在許多 sprite 的集合上運作。
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: 'ID3DX10Sprite 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301926"
---
# <a name="id3dx10sprite-interface"></a>ID3DX10Sprite 介面

ID3DX10Sprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。 這個介面可以在許多 sprite 的集合上運作。

## <a name="members"></a>成員

**ID3DX10Sprite** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10Sprite** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10Sprite** 介面具有這些方法。



| 方法                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**開始**](id3dx10sprite-begin.md)                                   | 準備用來繪製 sprite 的裝置。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | 將 sprite 的陣列新增至要轉譯的 sprite 批次。 您必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： end**](id3dx10sprite-end.md)之間呼叫這一點，而且必須在結束之前呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) ，才能將所有批次內建的子內容傳送到裝置以進行轉譯。 這種繪製方法最適合用來繪製少量的 sprite，而您想要將它緩衝至大型批次，例如字型。<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | 繪製 sprite 的陣列。 這會立即將 sprite 傳送至裝置以進行轉譯，這與 ID3DX10Sprite 不同 [**：:D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) ，這會在呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) 時，只將 sprite 的陣列新增至要轉譯的一批 sprite。 此繪製方法最適合用來繪製已在 CPU (上排序的大量 sprite，或不需要) 的排序，例如在物件中。 必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md)之間呼叫這項功能。<br/> |
| [**結束**](id3dx10sprite-end.md)                                       | 在 ID3DX10Sprite：： Flush 之後呼叫此動作。 如果 \_ \_ \_ 在呼叫 ID3DX10Sprite：： begin 時指定了 D3DX10 SPRITE SAVE 狀態，此 API 會將裝置狀態還原為在呼叫 ID3DX10Sprite：： begin 之前的狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**清除**](id3dx10sprite-flush.md)                                   | 強制將所有批次的子層提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DX10Sprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | 取出與 sprite 物件相關聯的裝置。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | 取得套用至所有 sprite 的 sprite 投影矩陣。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | 取得套用至所有 sprite 的視圖轉換。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | 設定所有 sprite 的投射矩陣。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | 設定適用于所有 sprite 的視圖轉換。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>備註

ID3DX10Sprite 介面是藉由呼叫 [**D3DX10CreateSprite**](d3dx10createsprite.md) 函數來取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
